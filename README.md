### Description 
> Check-list composed for registration form. 
Composed scenarios are applicable to check different forms proceeded from invented requirements and principally shows variability of different tests.
For simplicity checks are focused only on russian users (mainly regarding the requirement for a telephone number).
For full-fledged covering and preparing scenarios for regression testing (also for comfortable covering by autotests) better to use test-cases. 
Some examples of test-cases are also below. 
---
### Marks:
- [Entry requirements](#entryrequirements)
- [Check-list](#checklist)
- [Test-case examples](#testcases)

---
### Entry requirements:<a name="entryrequirements"></a>

#### Elements:
1. **Username field**
    - can be up to 26 characters long
    - can only use latin characters
    - can accept both lowercase or uppercase letters (automatically transform uppercase to lowercase letters after registration)
    - verification in real time (red text if violates the requirements, common text if not violates the requirements)
    - checking availability in real time (green check mark appears if available, red cross appears if not available)

2. **Phone number field**
    - can be exactly 10 entered characters long
    - can only use numeric characters
    - input is not possible for latin, cyrillic and special characters (characters does exist when trying to enter)
    - append `+7` in front of the number automatically 

3. **Send confirmation password button** 
    - activates when phone number satisfied the requirements of phone number field
    - confirmation password comes to the specified phone number within 1-40 seconds

4. **Repeat sending confirmation password button**
    - available after 40 seconds from previous sended request

5. **Number confirmation field**
    - uses only 6 numeric characters
    - input is not possible for latin, cyrillic and special characters (characters does exist when trying to enter)
   
6.  **Password field**
    - can be up to 26 characters long
    - the minimum number of characters is 8
    - can use both lowercase or uppercase letters
    - can only use latin, numeric characters and special characters like `(spacebar) ! " # $ % &` 
    - input failure alert when trying to enter cyrillic characters and special characters except `(spacebar) ! " # $ % &`
7. **Repeat password field**
    - can not be different to password field
    - verification of identity to password in real time (green check mark appears if available, notice "does not match the password" if not available) 

8. **Personal data processing consent agreement checkbox**
    - Register button is not available without marked checkbox (duplicated from requirement to register button)

9. **Register button**
    - available to push if entered values satisfied the requirements for input fields and personal data processing consent agreement checkbox marked


---
### Check-list<a name="checklist"></a>
### Fields validation
*(ft) - functional tests*

#### Username field
1. empty field
2. 1 latin character *(ft)*
3. 2-24 latin characters *(ft)*
4. 25 latin characters *(ft)*
5. 26 latin characters *(ft)*
6. 27 latin characters
7. 28+ latin characters
8. uppercase letters + lowercase letters *(ft)*
9. only spacebar
10. spacebar at the beginning of username
11. spacebar at the end of username
12. spacebar in the middle of username
13. cyrillic characters
14. numeric characters
15. special characters
16. lowercase latin characters + cyrillic characters
17. lowercase latin characters + numeric characters
18. lowercase latin characters + special characters
19. lowercase latin characters + spacebar
20. real time verification of input characters
21. real time markers of username availability
22. XSS injection
23. clipboard input

#### Phone number field
1. empty field
2. 1-8 numeric characters
3. 9 numeric characters
4. 10 numeric characters *(ft)*
5. 11 numeric characters
6. input capability for cyrillic, latin and special characters
7. appending `+7` in front of the number *(ft)*
8. clipboard input

#### Send confirmation password button and repeat sending confirmation password button
1. sending when phone number is correct *(ft)*
2. sending when phone number is incorrect
3. button activation when verification of phone number is completed *(ft)*
4. time elapsed for responsing confirmation code
5. resend button activation *(ft)*
6. difference between the previous and repeated confirmation codes

#### Number confirmation field
1. successful confirmation by recieved confirmation code *(ft)*
2. entering an invalid verification code
3. input capability for latin, cyrillic and special characters
4. clipboard input

#### Password field
1. empty field
2. 1-6 valid characters 
3. 7 valid characters 
4. 8 valid characters *(ft)*
5. 9 valid characters *(ft)*
6. 10-24 valid characters *(ft)*
7. 25 valid characters *(ft)*
8. 26 valid characters *(ft)*
9. 27 valid characters
10. 8-26 characters in total of uppercase letters + lowercase letters + numeric characters + each special character like `(spacebar) ! " # $ % &` *(ft)*
11. real time verification of input characters
12. the ability to enter tags `<, >, {, }, (, ), ?`
13. XSS injection
14. clipboard input

#### Repeat password field
1. identity between the previous and repeated password *(ft)*
2. mismatch between the previous and repeated password
3. XSS injection

#### Personal data processing consent agreement checkbox
1. marked when clicked inside the checkbox *(ft)*
2. marked when clicked at a nearest area around checkbox
3. marked when clicked at an area of text description

#### Register button
1. activation when all fields and checkbox are filled with valid values *(ft)*
2. activation when at least one of fields is filled with invalid value
3. activation without personal data processing consent agreement 


---
### Test-cases<a  name="testcases"></a>

#### Functional testing
|***testcase_1***||
|---|---|
|**-Test group-**|*Registration form*|
|**-Description-**|*Phone number verification*|
|**-Precondition-**|*User is not registered*|
|**-Steps-** <br>|**-Expected result-** <br>|
|1. fill field of phone number with valid value|send confirmation password button became active|
|2. press send confirmation password button|countdown timer appeared inside button, phone recieved confirmation code|
|3. fill number confirmation field with recieved confirmation code|system accepted confirmation code, error notifications are not appeared|

|***testcase_2***||
|---|---|
|**-Test group-**|*Registration form*|
|**-Description-**|*User registration*|
|**-Precondition-**|*User is not registered, phone number verified*|
|**-Steps-**|**-Expected result-**|
|1. fill fields with valid values|system accepted input parameters|
|2. mark checkbox of data processing consent agreement|checkbox checked|
|3. press "Register" button|User registered, start page opened, successful registration message recieved on the phone|

