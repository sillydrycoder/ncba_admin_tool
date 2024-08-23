# Firebase Admin SDK User Management

This Python script allows you to manage user accounts in a Firebase project using the Firebase Admin SDK. Specifically, it provides functionality to add or remove admin claims from users based on their UID or email.

## Features

- **Add Admin Claim**: Grant admin privileges to a user by setting a custom claim.
- **Remove Admin Claim**: Revoke admin privileges by removing the admin custom claim.
- **User Identification**: Identify users by either their email or UID.

## Prerequisites

### Python Installation

Ensure Python 3.7 or higher is installed on your system. You can download Python from the [official website](https://www.python.org/downloads/).

To verify your Python installation, run:

```bash
python --version
```

### Firebase Setup

1. **Create a Firebase Project**: If you haven't already, create a project in the [Firebase Console](https://console.firebase.google.com/).

2. **Service Account Key**: Generate a service account key from your Firebase project:
   - Go to the Firebase Console > Project Settings > Service Accounts.
   - Click "Generate New Private Key" and download the JSON file.
   - Save this file as `serviceAccountKey.json` in the root directory of your project.

### Install Dependencies

Create a virtual environment and install the required packages:

```bash
# Create a virtual environment
python -m venv venv

# Activate the virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Install required packages
pip install firebase-admin
```

### Project Structure

Ensure your project has the following structure:

```plaintext
your_project_directory/
│
├── serviceAccountKey.json   # Firebase service account key
├── manage_users.py          # Main Python script
└── README.md                # This README file
```

## Usage

To run the script, simply execute the Python file:

```bash
python manage_users.py
```

### Options

1. **Add Admin Claim**: Add admin privileges to a user.
2. **Remove Admin Claim**: Revoke admin privileges from a user.
3. **Exit**: Quit the program.

### Example

**Adding an Admin Claim:**

```plaintext
Choose an action:
1. Add admin claim for a user (by UID or Email)
2. Remove admin claim for a user (by UID or Email)
0. Exit
Enter your choice: 1
Enter the UID or Email of the user to add admin claim: user@example.com
Admin claim added successfully for user abc123
```

**Removing an Admin Claim:**

```plaintext
Choose an action:
1. Add admin claim for a user (by UID or Email)
2. Remove admin claim for a user (by UID or Email)
0. Exit
Enter your choice: 2
Enter the UID or Email of the user to remove admin claim: user@example.com
Admin claim removed successfully for user abc123
```

## Error Handling

The script includes basic error handling for:
- Invalid UIDs or emails.
- Users not found in Firebase.
- Firebase Admin SDK errors.

## Contributing

Contributions are welcome! If you find a bug or want to add a feature, feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.