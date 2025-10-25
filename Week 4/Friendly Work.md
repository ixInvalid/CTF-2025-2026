# Friendly-Work Solution

Date: October 20, 2025

### Steps

#### Flag 1
- Enter Name as: AAAAAAAAAAAAAAAAAAAAAAAAN
- 24 Characters of 'A' into Name + "N" at the End
- Overflow into Type (ADMIN=78 Which is ASCII 'N')

#### Flag 2
- Run 2 Once
- Run 1 and Send "20568"
- (Writes Bytes 0x58 0x50 0x00 0x00 in Memory → ASCII "X" "P" '\0' '\0')

#### Flag 3
- Writing the Flag into `work.message`
- Overflow the Numbers Such That Friend Becomes ':' , ')' , 'A' , 'A'.
- Also, Make the Memory Between Friend and Message NonZero, So %s Scan Continues
- Because `work.friend[0] == ':'` and `work.friend[1] == ')'`, the Program Will Execute `printf("Yes He is Right Here: %s\n\n", work.friend);`. Because friend[2..] and the numbers[] Words are NonZero and `work.message` Contains the Flag (terminated by \0), the %s Scan Will Continue into `work.message` and Print FLAG_3.