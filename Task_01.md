# Calculator Application Test Cases    

---

## **1. Valid Input Tests**  

### **1.1 Basic Arithmetic Operations**  

#### **TC-101: Verify Addition of Positive Numbers**  
- **Description**: Ensure the calculator correctly adds two positive integers.  
- **Preconditions**: Calculator is open and reset.  
- **Test Steps**:  
  1. Enter `5`.  
  2. Press `+`.  
  3. Enter `3`.  
  4. Press `=`.  
- **Expected Result**: `8` is displayed.  

#### **TC-102: Verify Subtraction with Negative Result**  
- **Description**: Verify subtraction yields a negative number when the second operand is larger.  
- **Preconditions**: Calculator is reset.  
- **Test Steps**:  
  1. Enter `10`.  
  2. Press `-`.  
  3. Enter `15`.  
  4. Press `=`.  
- **Expected Result**: `-5` is displayed.  

#### **TC-103: Verify Multiplication with Decimals**  
- **Description**: Test multiplication with decimal inputs.  
- **Preconditions**: Calculator is reset.  
- **Test Steps**:  
  1. Enter `2.5`.  
  2. Press `*`.  
  3. Enter `4`.  
  4. Press `=`.  
- **Expected Result**: `10` is displayed.  

#### **TC-104: Verify Division with Fractions**  
- **Description**: Ensure division returns accurate fractional results.  
- **Preconditions**: Calculator is reset.  
- **Test Steps**:  
  1. Enter `1`.  
  2. Press `/`.  
  3. Enter `4`.  
  4. Press `=`.  
- **Expected Result**: `0.25` is displayed.  

---

### **1.2 BODMAS/PEMDAS Rule Validation**  

#### **TC-105: Verify Operator Precedence (Multiplication Before Addition)**  
- **Description**: Validate that `2 + 3 * 4` follows BODMAS rules.  
- **Preconditions**: Calculator is reset.  
- **Test Steps**:  
  1. Enter `2 + 3 * 4`.  
  2. Press `=`.  
- **Expected Result**: `14` is displayed (not `20`).  

#### **TC-106: Verify Parentheses Override Precedence**  
- **Description**: Test if parentheses force addition before multiplication.  
- **Preconditions**: Calculator is reset.  
- **Test Steps**:  
  1. Enter `(2 + 3) * 4`.  
  2. Press `=`.  
- **Expected Result**: `20` is displayed.  

---

## **2. Invalid Input Tests**  

### **2.1 Non-Numeric Input Handling**  

#### **TC-201: Verify Error on Alphabetic Input**  
- **Description**: Ensure the calculator rejects non-numeric characters (e.g., letters).  
- **Preconditions**: Calculator is reset.  
- **Test Steps**:  
  1. Press keys `A + 2`.  
- **Expected Result**: Error message (e.g., "Invalid input").  

#### **TC-202: Verify Error on Special Characters**  
- **Description**: Test handling of symbols like `@`, `#`, etc.  
- **Preconditions**: Calculator is reset.  
- **Test Steps**:  
  1. Press `@ + 5`.  
- **Expected Result**: Error message displayed.  

---

### **2.2 Division Edge Cases**  

#### **TC-203: Verify Division by Zero Error**  
- **Description**: Ensure division by zero shows an error (not crash).  
- **Preconditions**: Calculator is reset.  
- **Test Steps**:  
  1. Enter `5`.  
  2. Press `/`.  
  3. Enter `0`.  
  4. Press `=`.  
- **Expected Result**: "Cannot divide by zero" error.  

#### **TC-204: Verify Division with Zero Numerator**  
- **Description**: Test `0 / X` returns `0`.  
- **Preconditions**: Calculator is reset.  
- **Test Steps**:  
  1. Enter `0 / 5`.  
  2. Press `=`.  
- **Expected Result**: `0` is displayed.  

---

## **3. Additional Scenarios**  

#### **TC-301: Verify Continuous Operations (Chaining)**  
- **Description**: Test sequential operations without resetting (e.g., `2 + 3 - 1`).  
- **Preconditions**: Calculator is reset.  
- **Test Steps**:  
  1. Enter `2 + 3 - 1`.  
  2. Press `=`.  
- **Expected Result**: `4` is displayed.  

#### **TC-302: Verify Clear/Reset Functionality**  
- **Description**: Ensure pressing `C` resets the calculator.  
- **Preconditions**: Calculator displays `5 + 3`.  
- **Test Steps**:  
  1. Press `C`.  
- **Expected Result**: Display shows `0` or blank.  

---
