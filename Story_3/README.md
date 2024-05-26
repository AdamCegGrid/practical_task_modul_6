# Review of Requirements for Story 2

### Requirement Summary:

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

### Pros:

- **Specific:** The requirement clearly outlines what the form should contain and the expected outputs based on the input, which are well-defined triangle types.
- **Functional:** It addresses the functionality directly related to the user’s actions and the system’s response.

### Cons:

- **Lacks Error Handling Details:** It doesn’t specify what happens if the inputs do not form a valid triangle or if the inputs are outside the specified range after filtering.
- **Assumptions on Filtering:** The statement about automatic filtering of illegal characters is vague — does it include validation against non-numeric characters, and how is it communicated to the user?
- **Validation Needs:** No details on how the system should handle cases that defy the triangle inequality theorem (the sum of the lengths of any two sides must be greater than the length of the remaining side).

### Conclusion:

While the basic functionality is covered, the requirement lacks comprehensive error handling and user feedback mechanisms. It needs more specifics to ensure clarity and robust implementation.

## Questions to Improve the Requirements

1. What happens if the entered values do not adhere to the triangle inequality theorem? Should the system display an error message?
2. How should the system validate and react to inputs outside the valid range of [-81; +729] despite automatic filtering?
3. What feedback should the user receive if illegal characters are entered, given the automatic filtering?
4. Is there any visual or textual feedback provided to the user upon successful or unsuccessful submission of the form?
5. Should the input fields have any specific format or placeholder texts to guide the user?
6. How is the system's responsiveness defined? How quickly should it classify the triangle once the data is submitted?
7. Are there any accessibility considerations for users with disabilities in using the form?
8. What are the security considerations, if any, for submitting the triangle data?

## How to Apply These Improvements

1. **Revision of Requirement Statements:** Requirements should be updated to include responses to the questions, specifying what error messages to display, how inputs are validated, and the format of user feedback.

2. **Adjustment of Acceptance Criteria:** Detailed behaviors such as error handling and visual feedback should be incorporated into the acceptance criteria. These must be measurable and directly testable.

3. **Expansion of Test Cases:** Additional test cases should be formulated to encompass not just successful input scenarios but also various error conditions and user feedback expectations.