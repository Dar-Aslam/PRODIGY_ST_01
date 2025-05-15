#  Calculator Application – Test Case Documentation  



> **Display Limit**: Supports up to **15-digit precision** in standard numeric format (range: −999,999,999,999,999 to 999,999,999,999,999).  
> **Note**: When computation results exceed this limit, **scientific (exponential) notation** may be used (e.g., `1e+15`).

---

## 1.  Basic Arithmetic Operations

### **Test Case ID:** TC_Calc_001  
- **Test Description**: Addition of two positive integers  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `5`  
  2. Press `+`  
  3. Enter `3`  
  4. Press `=`  
- **Expected Result**: Display should show `8`

### **Test Case ID:** TC_Calc_002  
- **Test Description**: Addition of positive and negative numbers  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `5`  
  2. Press `+`  
  3. Enter `-3`  
  4. Press `=`  
- **Expected Result**: Display should show `2`

### **Test Case ID:** TC_Calc_003  
- **Test Description**: Addition of two negative numbers  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `-5`  
  2. Press `+`  
  3. Enter `-3`  
  4. Press `=`  
- **Expected Result**: Display should show `-8`

### **Test Case ID:** TC_Calc_004  
- **Test Description**: Subtraction of two positive integers  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `10`  
  2. Press `-`  
  3. Enter `4`  
  4. Press `=`  
- **Expected Result**: Display should show `6`

### **Test Case ID:** TC_Calc_005  
- **Test Description**: Subtraction involving zero  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `5`  
  2. Press `-`  
  3. Enter `0`  
  4. Press `=`  
- **Expected Result**: Display should show `5`

### **Test Case ID:** TC_Calc_006  
- **Test Description**: Subtraction of negative numbers  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `-5`  
  2. Press `-`  
  3. Enter `-3`  
  4. Press `=`  
- **Expected Result**: Display should show `-2`

---
## 2. Decimal and Large Number Operations

### **Test Case ID:** TC_Calc_007  
- **Test Description**: Addition of decimal numbers  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `2.5`  
  2. Press `+`  
  3. Enter `3.1`  
  4. Press `=`  
- **Expected Result**: Display should show `5.6`

### **Test Case ID:** TC_Calc_008  
- **Test Description**: Subtraction with decimal values  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `10.75`  
  2. Press `-`  
  3. Enter `2.25`  
  4. Press `=`  
- **Expected Result**: Display should show `8.5`

### **Test Case ID:** TC_Calc_009  
- **Test Description**: Multiplication of decimals  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `1.5`  
  2. Press `*`  
  3. Enter `2.5`  
  4. Press `=`  
- **Expected Result**: Display should show `3.75`

### **Test Case ID:** TC_Calc_010  
- **Test Description**: Division resulting in a decimal  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `5`  
  2. Press `/`  
  3. Enter `2`  
  4. Press `=`  
- **Expected Result**: Display should show `2.5`

### **Test Case ID:** TC_Calc_011  
- **Test Description**: Division of two negative numbers  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `-10`  
  2. Press `/`  
  3. Enter `-2`  
  4. Press `=`  
- **Expected Result**: Display should show `5`

### **Test Case ID:** TC_Calc_012  
- **Test Description**: Multiplication near 15-digit limit  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `999999999999999`  
  2. Press `*`  
  3. Enter `2`  
  4. Press `=`  
- **Expected Result**: Display should show `1.999999999999998e+15`


## 3.  BODMAS and Parentheses

### **Test Case ID:** TC_Calc_013  
- **Test Description**: Operator precedence - multiplication before addition  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `2`  
  2. Press `+`  
  3. Enter `3`  
  4. Press `*`  
  5. Enter `4`  
  6. Press `=`  
- **Expected Result**: Display should show `14`

### **Test Case ID:** TC_Calc_014  
- **Test Description**: Parentheses overriding operator precedence  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `( 2 + 3 )`  
  2. Press `*`  
  3. Enter `4`  
  4. Press `=`  
- **Expected Result**: Display should show `20`

### **Test Case ID:** TC_Calc_015  
- **Test Description**: Nested parentheses calculation  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `2 * ( 3 + ( 4 / 2 ) )`  
  2. Press `=`  
- **Expected Result**: Display should show `10`

### **Test Case ID:** TC_Calc_016  
- **Test Description**: Mixed signs with parentheses  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `( -3 + 2 )`  
  2. Press `*`  
  3. Enter `-4`  
  4. Press `=`  
- **Expected Result**: Display should show `-4`

### **Test Case ID:** TC_Calc_017  
- **Test Description**: Handling empty parentheses  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `5 + ( )`  
  2. Press `=`  
- **Expected Result**: Display should show error or treat as no operation


## 4.  Invalid Inputs

### **Test Case ID:** TC_Calc_018  
- **Test Description**: Division by zero  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `5`  
  2. Press `/`  
  3. Enter `0`  
  4. Press `=`  
- **Expected Result**: Display should show `Cannot divide by zero` or appropriate error

### **Test Case ID:** TC_Calc_019  
- **Test Description**: Multiple decimal points in a single number  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `5..6` or `2.5.3`  
  2. Press `=`  
- **Expected Result**: Display should show input error or prevent additional decimal

### **Test Case ID:** TC_Calc_020  
- **Test Description**: Leading zeros with numeric input  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `0005`  
  2. Press `+`  
  3. Enter `003`  
  4. Press `=`  
- **Expected Result**: Display should show `8`

### **Test Case ID:** TC_Calc_021  
- **Test Description**: Leading zeros with decimal input  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `0005.500`  
  2. Press `+`  
  3. Enter `00.50`  
  4. Press `=`  
- **Expected Result**: Display should show `6.0`

### **Test Case ID:** TC_Calc_022  
- **Test Description**: Input exceeding 15-digit limit  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `1000000000000000` (16-digit number)  
  2. Press `=` or attempt operation  
- **Expected Result**: Display should show error, truncate, or switch to exponential notation


## 5. Exponent Format & Overflow Behavior

> When the result of a calculation exceeds the 15-digit display limit, the calculator should switch to scientific notation (exponent format).

### **Test Case ID:** TC_Calc_023  
- **Test Description**: Result exceeds limit in multiplication  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `999999999999999`  
  2. Press `*`  
  3. Enter `2`  
  4. Press `=`  
- **Expected Result**: Display should show `1.999999999999998e+15`

### **Test Case ID:** TC_Calc_024  
- **Test Description**: Exponential format on addition overflow  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `999999999999999`  
  2. Press `+`  
  3. Enter `1000000000000000`  
  4. Press `=`  
- **Expected Result**: Display should show `1.999999999999999e+15`

### **Test Case ID:** TC_Calc_025  
- **Test Description**: Negative result underflow behavior  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `-999999999999999`  
  2. Press `-`  
  3. Enter `1`  
  4. Press `=`  
- **Expected Result**: Display should show error or `-1e+15`

### **Test Case ID:** TC_Calc_026  
- **Test Description**: Result of exponential division  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `9999999999999999`  
  2. Press `/`  
  3. Enter `0.0000001`  
  4. Press `=`  
- **Expected Result**: Display should show `1e+17` or equivalent formatted value

### **Test Case ID:** TC_Calc_027  
- **Test Description**: Exponential multiplication of small decimals  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `0.0000001`  
  2. Press `*`  
  3. Enter `10000000000`  
  4. Press `=`  
- **Expected Result**: Display should show `1.0`


## 6. Functional Cases

### **Test Case ID:** TC_Calc_028  
- **Test Description**: Pressing `=` without any prior input  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Press `=`  
- **Expected Result**: Display should show `0`

### **Test Case ID:** TC_Calc_029  
- **Test Description**: Chained operations without pressing clear/reset  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `5`  
  2. Press `+`  
  3. Enter `3`  
  4. Press `=`  
  5. Press `+`  
  6. Enter `2`  
  7. Press `=`  
- **Expected Result**: Display should show `10`

### **Test Case ID:** TC_Calc_030  
- **Test Description**: Repeated equals for operation repetition  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `2`  
  2. Press `+`  
  3. Enter `2`  
  4. Press `=`  
  5. Press `=` again multiple times  
- **Expected Result**: Display should show `8` (repeating addition of 2)

### **Test Case ID:** TC_Calc_031  
- **Test Description**: Decimal input without leading zero  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `.5`  
  2. Press `+`  
  3. Enter `.5`  
  4. Press `=`  
- **Expected Result**: Display should show `1.0`

### **Test Case ID:** TC_Calc_032  
- **Test Description**: Use of backspace or clear after partial input  
- **Preconditions**: Calculator is in a ready/reset state  
- **Test Steps**:  
  1. Enter `5 +`  
  2. Press `C` (clear)  
- **Expected Result**: Display should reset to `0`

---

<center>
 **End of Document**  
 </center>

