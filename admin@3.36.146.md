classDiagram
direction BT
class BloodPressure {
   float systolic
   float diastolic
   float pulse_rate
   datetime(6) createAt
   bigint(20) surveyId
   bigint(20) pid
   bigint(20) tid
}
class Dementia {
   varchar(255) dementia_question1
   varchar(255) dementia_question2
   varchar(255) dementia_question3
   varchar(255) dementia_question4
   varchar(255) dementia_question5
   varchar(255) dementia_question6
   varchar(255) dementia_question7
   varchar(255) dementia_question8
   varchar(255) dementia_question9
   varchar(255) dementia_question10
   varchar(255) dementia_question11
   varchar(255) dementia_question12
   varchar(255) dementia_question13
   varchar(255) dementia_question14
   datetime(6) createAt
   bigint(20) surveyId
   bigint(20) pid
   bigint(20) tid
}
class ErrorLog {
   varchar(255) err_code
   varchar(1000) err_message
   int(11) error1
   varchar(255) error10
   int(11) error2
   int(11) error3
   int(11) error4
   int(11) error5
   varchar(255) error6
   varchar(255) error7
   varchar(255) error8
   varchar(255) error9
   varchar(255) insert_table
   datetime(6) insert_time
   text json_txt
   bigint(20) id
}
class EyeCheckAmsler {
   int(11) Amsler1
   varchar(255) Amsler10
   int(11) Amsler2
   int(11) Amsler3
   int(11) Amsler4
   int(11) Amsler5
   varchar(255) Amsler6
   varchar(255) Amsler7
   varchar(255) Amsler8
   varchar(255) Amsler9
   datetime(6) createAt
   int(11) distance
   varchar(255) leftMacularLoc
   varchar(255) rightMacularLoc
   bigint(20) pid
   bigint(20) surveyId
   bigint(20) tid
}
class EyeCheckMCharts {
   datetime(6) createAt
   int(11) distance
   int(11) leftEyeHor
   int(11) leftEyeVer
   int(11) mChart1
   varchar(255) mChart10
   int(11) mChart2
   int(11) mChart3
   int(11) mChart4
   int(11) mChart5
   varchar(255) mChart6
   varchar(255) mChart7
   varchar(255) mChart8
   varchar(255) mChart9
   int(11) rightEyeHor
   int(11) rightEyeVer
   bigint(20) pid
   bigint(20) surveyId
   bigint(20) tid
}
class EyeCheckPresbyopia {
   datetime(6) createAt
   int(11) distance1
   int(11) distance2
   int(11) distance3
   int(11) distanceAvg
   int(11) presbyopia1
   varchar(255) presbyopia10
   int(11) presbyopia2
   int(11) presbyopia3
   int(11) presbyopia4
   int(11) presbyopia5
   varchar(255) presbyopia6
   varchar(255) presbyopia7
   varchar(255) presbyopia8
   varchar(255) presbyopia9
   bigint(20) pid
   bigint(20) surveyId
   bigint(20) tid
}
class EyeCheckSight {
   datetime(6) createAt
   int(11) distance
   varchar(255) leftPerspective
   int(11) leftSight
   varchar(255) rightPerspective
   int(11) rightSight
   int(11) test1
   varchar(255) test10
   int(11) test2
   int(11) test3
   int(11) test4
   int(11) test5
   varchar(255) test6
   varchar(255) test7
   varchar(255) test8
   varchar(255) test9
   varchar(255) testType
   bigint(20) pid
   bigint(20) surveyId
   bigint(20) tid
}
class EyeCheckStrabismus {
   datetime(6) createAt
   bigint(20) pid
   bigint(20) surveyId
   bigint(20) tid
}
class GripStrength {
   float left_grip
   float right_grip
   datetime(6) createAt
   bigint(20) surveyId
   bigint(20) pid
   bigint(20) tid
}
class PulmonaryFunction {
   datetime(6) createAt
   bigint(20) pid
   bigint(20) surveyId
   bigint(20) tid
}
class admin {
   datetime(6) create_at
   varchar(255) email
   varchar(255) name
   varchar(255) password
   varchar(255) refreshToken
   varchar(255) salt
   varchar(255) tel
   varchar(255) id
}
class extra1 {
   int(11) value1
   int(11) value10
   varchar(255) value11
   varchar(255) value12
   varchar(255) value13
   varchar(255) value14
   varchar(255) value15
   varchar(255) value16
   varchar(255) value17
   varchar(255) value18
   varchar(255) value19
   int(11) value2
   varchar(255) value20
   int(11) value3
   int(11) value4
   int(11) value5
   int(11) value6
   int(11) value7
   int(11) value8
   int(11) value9
   bigint(20) tid
}
class extra2 {
   int(11) value1
   int(11) value10
   varchar(255) value11
   varchar(255) value12
   varchar(255) value13
   varchar(255) value14
   varchar(255) value15
   varchar(255) value16
   varchar(255) value17
   varchar(255) value18
   varchar(255) value19
   int(11) value2
   varchar(255) value20
   int(11) value3
   int(11) value4
   int(11) value5
   int(11) value6
   int(11) value7
   int(11) value8
   int(11) value9
   bigint(20) tid
}
class extra3 {
   int(11) value1
   int(11) value10
   varchar(255) value11
   varchar(255) value12
   varchar(255) value13
   varchar(255) value14
   varchar(255) value15
   varchar(255) value16
   varchar(255) value17
   varchar(255) value18
   varchar(255) value19
   int(11) value2
   varchar(255) value20
   int(11) value3
   int(11) value4
   int(11) value5
   int(11) value6
   int(11) value7
   int(11) value8
   int(11) value9
   bigint(20) tid
}
class extra4 {
   int(11) value1
   int(11) value10
   varchar(255) value11
   varchar(255) value12
   varchar(255) value13
   varchar(255) value14
   varchar(255) value15
   varchar(255) value16
   varchar(255) value17
   varchar(255) value18
   varchar(255) value19
   int(11) value2
   varchar(255) value20
   int(11) value3
   int(11) value4
   int(11) value5
   int(11) value6
   int(11) value7
   int(11) value8
   int(11) value9
   bigint(20) tid
}
class extra5 {
   int(11) value1
   int(11) value10
   varchar(255) value11
   varchar(255) value12
   varchar(255) value13
   varchar(255) value14
   varchar(255) value15
   varchar(255) value16
   varchar(255) value17
   varchar(255) value18
   varchar(255) value19
   int(11) value2
   varchar(255) value20
   int(11) value3
   int(11) value4
   int(11) value5
   int(11) value6
   int(11) value7
   int(11) value8
   int(11) value9
   bigint(20) tid
}
class extra6 {
   int(11) value1
   int(11) value10
   varchar(255) value11
   varchar(255) value12
   varchar(255) value13
   varchar(255) value14
   varchar(255) value15
   varchar(255) value16
   varchar(255) value17
   varchar(255) value18
   varchar(255) value19
   int(11) value2
   varchar(255) value20
   int(11) value3
   int(11) value4
   int(11) value5
   int(11) value6
   int(11) value7
   int(11) value8
   int(11) value9
   bigint(20) tid
}
class extra7 {
   int(11) value1
   int(11) value10
   varchar(255) value11
   varchar(255) value12
   varchar(255) value13
   varchar(255) value14
   varchar(255) value15
   varchar(255) value16
   varchar(255) value17
   varchar(255) value18
   varchar(255) value19
   int(11) value2
   varchar(255) value20
   int(11) value3
   int(11) value4
   int(11) value5
   int(11) value6
   int(11) value7
   int(11) value8
   int(11) value9
   bigint(20) tid
}
class extra8 {
   int(11) value1
   int(11) value10
   varchar(255) value11
   varchar(255) value12
   varchar(255) value13
   varchar(255) value14
   varchar(255) value15
   varchar(255) value16
   varchar(255) value17
   varchar(255) value18
   varchar(255) value19
   int(11) value2
   varchar(255) value20
   int(11) value3
   int(11) value4
   int(11) value5
   int(11) value6
   int(11) value7
   int(11) value8
   int(11) value9
   bigint(20) tid
}
class location {
   varchar(255) ad1
   varchar(255) ad10
   varchar(255) ad2
   varchar(255) ad3
   varchar(255) ad4
   varchar(255) ad5
   varchar(255) ad6
   varchar(255) ad7
   varchar(255) ad8
   varchar(255) ad9
   varchar(255) adLoading
   varchar(255) adMain
   varchar(255) address
   varchar(255) companyName
   datetime(6) createAt
   varchar(255) detailAddress
   datetime(6) endTime
   varchar(255) gpsLatitude
   varchar(255) gpsLongitude
   varchar(255) id
   varchar(255) name
   varchar(255) password
   varchar(255) post
   varchar(255) printAd
   varchar(255) printAddress
   varchar(255) printTel
   varchar(255) refreshToken
   varchar(255) result
   varchar(255) site
   datetime(6) startTime
   varchar(255) tel
   datetime(6) updateAt
   varchar(255) video
   bigint(20) pid
}
class log {
   varchar(255) adminEmail
   datetime(6) createAt
   varchar(255) detail
   varchar(255) ip
   int(11) log1
   varchar(255) log10
   int(11) log2
   int(11) log3
   int(11) log4
   int(11) log5
   varchar(255) log6
   varchar(255) log7
   varchar(255) log8
   varchar(255) log9
   varchar(255) target
   varchar(255) url
   bigint(20) id
}
class survey {
   int(11) age
   datetime(6) createAt
   bit(1) diabetes
   varchar(255) gender
   bit(1) glasses
   varchar(255) surgery
   int(11) survey1
   varchar(255) survey10
   int(11) survey2
   int(11) survey3
   int(11) survey4
   int(11) survey5
   varchar(255) survey6
   varchar(255) survey7
   varchar(255) survey8
   varchar(255) survey9
   bigint(20) pid
   bigint(20) tid
}
class user {
   datetime(6) createAt
   varchar(255) email
   varchar(255) name
   varchar(255) id
   varchar(255) password
   varchar(255) salt
   varchar(255) refreshToken
   text vector
   varchar(255) qr_url
   bigint(20) surveyId
   bigint(20) pid
   bigint(20) tid
}
class user_survey_result {
   bigint(20) user_id
   datetime(6) createAt
   datetime(6) updateAt
   bigint(20) dementia_id
   bigint(20) blood_pressure_id
   bigint(20) grip_strength_id
   bigint(20) eye_presbyopia_id
   bigint(20) eye_amsler_id
   bigint(20) eye_mcharts_id
   bigint(20) eye_sight_id
   bigint(20) strabismus_id
   bigint(20) pulmonary_id
   bigint(20) tid
}

BloodPressure  -->  location : pid
BloodPressure  -->  survey : surveyId:tid
Dementia  -->  location : pid
Dementia  -->  survey : surveyId:tid
EyeCheckAmsler  -->  location : pid
EyeCheckAmsler  -->  survey : surveyId:tid
EyeCheckMCharts  -->  location : pid
EyeCheckMCharts  -->  survey : surveyId:tid
EyeCheckPresbyopia  -->  location : pid
EyeCheckPresbyopia  -->  survey : surveyId:tid
EyeCheckSight  -->  location : pid
EyeCheckSight  -->  survey : surveyId:tid
EyeCheckStrabismus  -->  location : pid
EyeCheckStrabismus  -->  survey : surveyId:tid
GripStrength  -->  location : pid
GripStrength  -->  survey : surveyId:tid
PulmonaryFunction  -->  location : pid
PulmonaryFunction  -->  survey : surveyId:tid
survey  -->  location : pid
user  -->  location : pid
user  -->  survey : surveyId:tid
user_survey_result  -->  BloodPressure : blood_pressure_id:tid
user_survey_result  -->  Dementia : dementia_id:tid
user_survey_result  -->  EyeCheckAmsler : eye_amsler_id:tid
user_survey_result  -->  EyeCheckMCharts : eye_mcharts_id:tid
user_survey_result  -->  EyeCheckPresbyopia : eye_presbyopia_id:tid
user_survey_result  -->  EyeCheckSight : eye_sight_id:tid
user_survey_result  -->  EyeCheckStrabismus : strabismus_id:tid
user_survey_result  -->  GripStrength : grip_strength_id:tid
user_survey_result  -->  PulmonaryFunction : pulmonary_id:tid
user_survey_result  -->  user : user_id:tid
user_survey_result  -->  user : user_id:id
