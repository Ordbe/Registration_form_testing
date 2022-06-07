## Description 
Check-list composed for registration form. 
Composed scenarios are applicable to check different forms and principally shows variability of different tests.
For simplicity checks are focused only on the Russian users.
For full-fledged covering and preparing scenarios for regression testing (also for comfortable covering by autotests) better to use test-cases. 
Some templates for test-case are also below. 
---
### Marks:
- [Entry requirements](#entryrequirements)
- [Check-list](#checklist)
- [Test-case template](#testcases)

---
### Entry requirements:<a name="entryrequirements"></a>

##### Elements:
**1. Username field**
  - can be up to 26 characters long
  - can only use latin characters and numeric characters (both separately and in conjunction)
  - can accept both lowercase or uppercase letters (automatically transform uppercase to lowercase letters after registration)
  - verification in real time (red text if violates the requirements, common text if not violates the requirements)
  - checking availability in real time (green check mark appears if available, red cross appears if not available)
</br>
**2. Phone number field**
  - can be exactly 10 entered characters long
  - can only use numeric characters
  - append `+7` in front of the number automatically 
</br>
**3. Number confirmation field**
  - uses only 6 numeric characters
</br>
**4. Password field**
  - can be up to 26 characters long
  - can use both lowercase or uppercase letters
  - can use special characters like `(spacebar) ! " # $ % &` 
</br>
**5. Repeat password field**
  - can not be different to password field
  - verification of identity to password in real time (green check mark appears if available, notice "does not match the password" if not available) 
</br>
**6. Register button**
  - available to push if entered values satisfied the requirements for input fields and personal data processing consent agreement checkbox marked.
</br>
**7. Repeat sending confirmation password button**
  - available after 40 seconds from previous sended request
</br>
**8. Personal data processing consent agreement checkbox**
</br>


---
### Check-list

##### Username field
1. 0 latin characters
2. 1 latin character
3. 2-24 latin characters
4. 25 latin characters
5. 26 latin characters
6. 27 latin characters
7. 28+ latin characters
8. lowercase latin characters + numeric characters
9. uppercase letters + lowercase letters + numeric characters
10. cyrillic characters
11. numeric characters
12. special characters
13. lowercase latin characters + cyrillic characters
14. lowercase latin characters + numeric characters
15. lowercase latin characters + special characters

