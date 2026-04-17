# Verification Module Documentation

## verification.py
Contains the logic for handling user verification processes through Discord interactions.

- **VERIFYING_USERS**: A set used to prevent users from starting multiple verification processes simultaneously.

- **VerificationView**: A Discord UI view that provides buttons for different verification types.
  - **on_error**: Handles errors during interactions, such as cooldowns or unexpected issues.
  - **_handle_verification**: A wrapper function to manage the verification process and ensure users cannot start multiple verifications at once.
  - **student_button**: Initiates the student verification process.
  - **alumni_button**: Initiates the alumni verification process.
  - **friend_button**: Initiates the friend verification process.
  - **verified_button**: Initiates the general verification process.

- **_send_verification_embed**: Sends an embed message to a specified channel with buttons for users to start the verification process. The embed includes descriptions for each verification type:
  - **Student**: Current RPI students.
  - **Alumni**: Former RPI students.
  - **Friend**: Friends of existing members.
  - **General Verification**: For any other reason.