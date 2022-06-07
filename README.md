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
    - append `+7` in front of the number automatically 

3. **Send confirmation password button** 
    - activates when phone number satisfied the requirements of phone number field
    - confirmation password comes to the specified phone number within 1-40 seconds

4. **Number confirmation field**
    - uses only 6 numeric characters
   
5.  **Password field**
    - can be up to 26 characters long
    - can use both lowercase or uppercase letters
    - can use special characters like `(spacebar) ! " # $ % &` 

6. **Repeat password field**
    - can not be different to password field
    - verification of identity to password in real time (green check mark appears if available, notice "does not match the password" if not available) 

7. **Register button**
    - available to push if entered values satisfied the requirements for input fields and personal data processing consent agreement checkbox marked

8. **Repeat sending confirmation password button**
    - available after 40 seconds from previous sended request

9. **Personal data processing consent agreement checkbox**
    - Register button is not available without marked checkbox (duplicated from requirement to register button)


---
### Check-list<a name="checklist"></a>

(ft) - functional tests

#### Username field
1. empty field
2. 1 latin character (ft)
3. 2-24 latin characters (ft)
4. 25 latin characters (ft)
5. 26 latin characters (ft)
6. 27 latin characters
7. 28+ latin characters
8. uppercase letters + lowercase letters (ft)
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
22. `<, >, {, }, (, )` tags input
23. XSS injection
24. clipboard input

#### Phone number field
1. empty field
2. 1-8 numeric characters
3. 9 numeric characters
4. 10 numeric characters (ft)
5. 11 numeric characters
6. numeric + cyrillic + latin + special characters
7. appending `+7` in front of the number (ft)
8. clipboard input

