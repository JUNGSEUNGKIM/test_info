# 🛡️ Python 코드 보호 및 리눅스 실행파일 생성 전략 보고서

---

## 1. 개요

Python은 소스코드가 노출되기 쉬운 인터프리터 언어입니다.  
리눅스에서 배포 가능한 실행파일을 만들면서도 코드 유출을 막기 위해, 다양한 패키징 및 난독화 방법이 필요합니다.  
본 문서는 대표적인 3가지 방식(PyInstaller, PyArmor, Cython)을 비교 정리합니다.

---

## 2. 방법별 비교 요약

| 항목                   | PyInstaller                | PyInstaller + PyArmor      | Cython + GCC               |
|------------------------|----------------------------|----------------------------|----------------------------|
| 보안성                | ⭐⭐                        | ⭐⭐⭐⭐                      | ⭐⭐⭐⭐⭐                     |
| 실행파일 형태          | Python 기반 바이너리       | 난독화된 Python 바이너리    | C로 컴파일된 네이티브 바이너리 |
| 리버스 엔지니어링 저항 | 낮음                        | 중간~높음                   | 매우 높음                  |
| 소스코드 포함 여부     | `.pyc` 포함 (노출 위험 있음) | 난독화 `.pyc` 포함 (분석 어려움) | 소스 제거, `.c` → ELF      |
| 실행 환경             | Python 필요                 | Python 필요                 | Python 없이도 가능 (embed) |
| 개발 난이도            | 매우 쉬움                   | 보통                        | 어려움                     |

---

## 3. 각 방법 상세 설명

### ✅ 3.1 PyInstaller

- Python 코드를 `.pyc` 형태로 포함한 단일 실행파일로 패키징  
- 명령어 예시:

```bash
pyinstaller --onefile your_script.py
```

#### 🔑 주요 옵션 설명

| 옵션 | 설명 |
|------|------|
| `--onefile` | 단일 실행파일로 생성 |
| `--noconsole` | 콘솔창 숨김 (GUI용) |
| `--icon=icon.ico` | 아이콘 설정 |
| `--name=appname` | 실행파일 이름 지정 |
| `--add-data "src:dest"` | 리소스 포함 |
| `--key yourkey` | 바이트코드 암호화용 키 (보안 강화) |
| `--cipher AES` | 암호화 알고리즘 지정 (기본: AES) |

> `--key` 옵션은 `.pyc` 내부 바이트코드를 지정한 키로 암호화하여, 추출해도 복호화 없이는 분석이 어렵습니다.  
> 단, 실행파일이 키를 내부에 포함하므로 **완벽한 보호는 아님**.

#### 📁 생성 구조

```
your_project/
├── your_script.py
├── dist/
│   └── your_script       # 실행파일
├── build/
├── your_script.spec
```

---

### ✅ 3.2 PyInstaller + PyArmor

- PyArmor로 먼저 코드를 난독화한 후 PyInstaller로 패키징
- 명령어 예시:

```bash
pyarmor obfuscate your_script.py
pyinstaller --onefile dist/your_script.py
```

또는 자동 패키징 명령:

```bash
pyarmor pack -e " --onefile" -x " --exclude tests" your_script.py
```

#### 장점
- `.pyc` 난독화로 분석 저항성 향상
- 기간 제한, HW 바인딩 등 라이센스 기능 포함 가능

---

### ✅ 3.3 Cython + GCC

- Python 코드를 C 코드로 변환 후 컴파일하여 완전한 네이티브 실행파일 생성

```bash
cython --embed -o your_script.c your_script.py
gcc -Os -o your_script your_script.c $(python3-config --includes --ldflags)
```

#### 장점
- 코드 완전 제거
- 역디컴파일 거의 불가능
- 실행 성능 향상

#### 단점
- 디버깅 어려움
- C 컴파일 환경 필요

---

## 4. 추천 전략

| 목적 | 추천 방법 |
|------|-----------|
| 빠르고 쉬운 배포 | PyInstaller 단독 사용 |
| 적당한 보안 + 쉬운 배포 | PyInstaller + PyArmor |
| 고보안 + 상용 배포 | Cython + GCC |

#### 추가 보안 팁
- `chmod 700` 등으로 실행파일 권한 제한
- MAC 주소 등으로 장비 바인딩
- Docker 내부에서 실행하여 접근 차단

---

## 5. 결론

Python 실행파일을 만들 때는 단순한 배포만이 아닌, **보안성**을 반드시 고려해야 합니다.  
PyInstaller는 빠르지만 노출 위험이 있고, PyArmor와 Cython은 보다 강력한 보안을 제공합니다.  
보안 수준에 따라 전략을 선택하고, 필요 시 암호화 옵션(`--key`)도 병행하여 사용하는 것이 좋습니다.

---
