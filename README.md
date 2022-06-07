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

##### Input fields:
1. Username
  - can be up to 26 characters long
  - can only use latin characters
  - can use both lowercase or uppercase letters
  - verification in real time (red text if violates the requirements, common text if not violates the requirements)
  - checking availability in real time (green check mark appears if available, red cross appears if not available)
2. Phone number
  - can be exactly 10 entered characters long
  - can only use numeric characters
  - append `+7` in front of the number automatically
3. Number confirmation
  - uses only 6 numeric characters
5. Password
  - can be up to 26 characters long
  - can use both lowercase or uppercase letters
  - can use special characters like `(spacebar) ! " # $ % &`
7. Repeat password
  - can not be different to password field
  - verification of identity to password in real time (green check mark appears if available, notice "does not match the password" if not available)

##### Buttons:
1. Register
  - available to push if entered values satisfied the requirements for input fields and personal data processing consent agreement checkbox marked.
3. Repeat sending confirmation password
  - available after 40 seconds from previous sended request

##### Checkboxes:
1. Personal data processing consent agreement

