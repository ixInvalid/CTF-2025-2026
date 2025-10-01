# Hash-Brown Solution

Date: September 29, 2025

### Steps

- Inspected the Submit Button
- Saw That There Was `onclick="check_password"`
- Went to Sources and Selected the (index) File
- CTR + F to Find `check_password` Function in (index) File
- Found `hash == d4b45864d9d6fabfc568d74f26c35ababde2105337d7af9a6605e1c56c891aa6`
- Went to https://crackstation.net/ to Crack the Hash
- Result of the Crack Was `Type: sha256` and `Result: cheeseburger`
- Entered `cheeseburger` Into Login
- Saw There Was a `print_flag` Function
- Went to Console and Typed `print_flag()`
- Grabbed the Flag from the HTML
