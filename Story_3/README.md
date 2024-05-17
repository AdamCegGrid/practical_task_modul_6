### Story_3
**Requirements:**
- *There is a form of three input fields and 1 button.*  
- *A valid value for each field is [-81; +729].*  
- *Illegal characters etc are filtered out automatically, so only digits and “-”/”+” could be entered.*  
- *Those fields represent sides (A, B, C) of a triangle, i.e. side lengths.*  
- *By pressing the button you send the length values to the system and the system may answer in the following manner ONLY:*  
    - *The T. is equilateral aka A==B==C*  
    - *The T. is isosceles aka A==B!=C*  
     - *The T. is scalene aka A=!B!=C*  

<br>

## [Solution](#)

### Requirements Analysis

**Requirements:**
There is a form with three input fields (A, B, C) and one button. A valid value for each field is [-81; +729]. Illegal characters are filtered out automatically. These fields represent the sides of a triangle. When the button is pressed, the system determines the type of triangle based on the side lengths.

**System Responses:**

- The triangle is equilateral (A == B == C)
- The triangle is isosceles (A == B != C)
- The triangle is scalene (A != B != C)

**Test Cases:**

1. **Valid Input Tests:**
    - **Equilateral Triangle:**
        - Input: A = 100, B = 100, C = 100
        - Expected Output: "The T. is equilateral aka A==B==C"
    - **Isosceles Triangle:**
        - Input: A = 100, B = 100, C = 150
        - Expected Output: "The T. is isosceles aka A==B!=C"
    - **Scalene Triangle:**
        - Input: A = 100, B = 150, C = 200
        - Expected Output: "The T. is scalene aka A=!B!=C"
2. **Boundary Value Tests:**
    - **Minimum Boundary:**
        - Input: A = -81, B = -81, C = -81
        - Expected Output: "The T. is equilateral aka A==B==C" (assuming the system handles negative values correctly)
    - **Maximum Boundary:**
        - Input: A = 729, B = 729, C = 729
        - Expected Output: "The T. is equilateral aka A==B==C"
    - **Mixed Boundary:**
        - Input: A = -81, B = 729, C = 0
        - Expected Output: "The T. is scalene aka A=!B!=C"
3. **Invalid Input Tests:**
    - **Out of Range Values:**
        - Input: A = -100, B = 50, C = 50
        - Expected Output: No output / error message (assuming validation prevents out-of-range values)
    - **Non-numeric Characters:**
        - Input: A = "abc", B = 50, C = 50
        - Expected Output: No output / error message (assuming validation filters out non-numeric characters)

**Tasks:**

1. Implement validation to ensure inputs are within the valid range.
2. Implement functionality to determine the type of triangle based on the inputs.
3. Write test cases to cover different scenarios including valid inputs, boundary values, and invalid inputs.

**Testing:**

### Test Cases:

1. Input Validation:

- **Test Case:** Enter values within the range [-81; +729].
- **Expected Result:** The input is accepted.
- **Test Case:** Enter values outside the range [-81; +729].
- **Expected Result:** The system displays an error message.

2. Triangle Type Determination:

- **Test Case:** Enter equal values for all three sides (e.g., A = 100, B = 100, C = 100).
- **Expected Result:** The system identifies the triangle as equilateral.
- **Test Case:** Enter two equal values and one different value (e.g., A = 100, B = 100, C = 150).
- **Expected Result:** The system identifies the triangle as isosceles.
- **Test Case:** Enter three different values (e.g., A = 100, B = 150, C = 200).
- **Expected Result:** The system identifies the triangle as scalene.

3. Boundary Value Testing:

- **Test Case:** Enter minimum boundary values (e.g., A = -81, B = -81, C = -81).
- **Expected Result:** The system identifies the triangle type correctly.
- **Test Case:** Enter maximum boundary values (e.g., A = 729, B = 729, C = 729).
- **Expected Result:** The system identifies the triangle type correctly.

4. Invalid Input Testing:

- **Test Case:** Enter a non-numeric value (e.g., A = "abc", B = 50, C = 50).
- **Expected Result:** The system displays an error message.
- **Test Case:** Enter a negative value outside the valid range (e.g., A = -100, B = 50, C = 50).
- **Expected Result:** The system displays an error message.
