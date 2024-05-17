### Story_2
- *As a user, I want to be able to change my photo.*  

<br>

## [Solution](#)

### Requirements Analysis

**User Story:**  
As a user, I want to be able to change my photo.

**Acceptance Criteria:**

1. The user should see an option to change their photo on their account page.
2. The user should be able to upload a new photo.
3. The new photo should replace the old one and be saved to the user's profile.

**Tasks:**

1. Add a 'Change Photo' button to the account page.
2. Implement functionality to upload a new photo.
3. Save the new photo to the user's profile in the database.
4. Display the updated photo on the account page.

**Testing:**

### Test Cases:

1. Change Photo Option:
    - **Input:** Navigate to the account page.
    - **Expected Result:** The user sees a 'Change Photo' button.
2. Upload New Photo:
    - **Input:** Click the 'Change Photo' button and select a new photo to upload.
    - **Expected Result:** The new photo is uploaded successfully.
3. Replace Old Photo:
    - **Input:** Upload a new photo.
    - **Expected Result:** The new photo replaces the old one and is saved to the user's profile.
4. Display Updated Photo:
    - **Input:** After uploading a new photo, refresh the account page.
    - **Expected Result:** The updated photo is displayed on the account page.
5. File Format Handling:
    - **Input:** Upload photos in different formats (e.g., .jpg, .png, .gif).
    - **Expected Result:** Photos in supported formats are uploaded successfully.
6. Large File Upload:
    - **Input:** Upload a large photo file.
    - **Expected Result:** The large photo file is uploaded successfully without any performance issues.
