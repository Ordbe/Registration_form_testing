## Description 
Check-list composed for registration form. 
Composed scenarios are applicable to check different forms and principally shows variability of different tests.
For simplicity checks are focused only on the Russian users.
For full-fledged covering examples of test-cases are also below. 
---
### Marks:
- [Entry requirements](#entryrequirements)
- [Check-list](#checklist)
- [Test-cases](#testcases)

---
### Entry requirements:<a name="entryrequirements"></a>

##### Elements:
1. Username field
  - can be up to 26 characters long
  - can only use latin characters
  - can use both lowercase or uppercase letters
  - verification in real time (red text if violates the requirements, common text if not violates the requirements)
  - checking availability in real time (green check mark appears if available, red cross appears if not available)
2. Phone number field
  - can be exactly 10 entered characters long
  - can only use numeric characters
  - append `+7` in front of the number automatically
3. Number confirmation field
  - uses only 6 numeric characters
4. Password field
  - can be up to 26 characters long
  - can use both lowercase or uppercase letters
  - can use special characters like `(spacebar) ! " # $ % &`
5. Repeat password field
  - can not be different to password field
  - verification of identity to password in real time (green check mark appears if available, notice "does not match the password" if not available)
6. Register button
  - available to push if entered values satisfied the requirements for input fields and personal data processing consent agreement checkbox marked.
7. Repeat sending confirmation password button
  - available after 40 seconds from previous sended request
8. Personal data processing consent agreement checkbox


---
### Check-list

#####Username field
1. 
