# User Management Bash Script 👨🏻‍💼✨

## Introduction⭐

This project, developed during the 2022-2023 academic year, aims to simplify and automate the management of user accounts in a Unix system using Bash scripts. By leveraging the power and simplicity of Bash, the scripts enable efficient user and group management, including the creation, deletion, and listing of users and groups, as well as the archiving of directories. The primary goal is to enhance the system administrator's experience by automating repetitive tasks and ensuring seamless user management.

## Features⭐

1. **User Management**
    - **Add User**: Create new user accounts with specified login, password, and group.
    - **Bulk Add Users from CSV**: Add multiple users from a CSV file.
    - **Delete User**: Remove user accounts.
    - **Bulk Delete Users from CSV**: Remove multiple users listed in a CSV file.
    - **List Users**: Display a list of all users.
2. **Group Management**
    - **Create Group**: Create new user groups.
    - **Delete Group**: Remove groups and their associated users.
3. **Directory Archiving**
    - **Archive Directory**: Move directories to an archive location.
    - **Bulk Archive Directories from Text File**: Archive multiple directories listed in a text file.
4. **Logging**
    - Comprehensive logging of all actions performed, including timestamps and reasons for any errors encountered.

## Script Breakdown⭐

### `ajout_utilisateur()`

This function prompts for user details (login, password, and group), checks if the user or group already exists, and creates the user account if valid. Logs actions and errors in `Gestion_utilisateur.log`.

### `creer_groupe()`

Creates a new group after verifying it doesn't already exist. Logs the creation in `Gestion_utilisateur.log`.

### `lister_utilisateur()`

Displays the list of users if any exist, otherwise prompts to add a user.

### `supprimer_utilisateur()`

Deletes a specified user account and updates the log and user lists accordingly.

### `supprimer_group_utilisateur()`

Deletes a specified group and all associated user accounts, updating logs and lists.

### `ajout_utilisateurs_csv()`

Reads user details from a CSV file and adds them, handling duplicates and missing groups appropriately.

### `suprression_utilisateurs_csv()`

Reads user details from a CSV file and deletes the specified users, updating logs and lists.

### `archiver_repertoire()`

Moves a specified directory to an archive location, logging the action.

### `archiver_repertoires_text()`

Reads directory paths from a text file and archives them, logging each action.

### `home()`

The main menu function, providing options for user and group management, as well as directory archiving.

## Usage⭐

1. **Run the Script**: Execute the script using a terminal.
    
    ```bash
    ./script_name.sh
    
    ```
    
2. **Main Menu**: Choose between user/group management and directory archiving.

### User and Group Management

1. **Add User**: Follow prompts to add a single user.
2. **Bulk Add Users from CSV**: Provide the path to a CSV file containing user details.
3. **Create Group**: Follow prompts to create a new group.
4. **List Users**: View the list of existing users.
5. **Delete User**: Provide the login of the user to be deleted.
6. **Delete Group and Users**: Provide the group name to delete the group and all its users.
7. **Bulk Delete Users from CSV**: Provide the path to a CSV file containing users to delete.

### Directory Archiving

1. **Archive Directory**: Provide the path to the directory to be archived.
2. **Bulk Archive Directories from Text File**: Provide the path to a text file containing directory paths to be archived.

## Logging⭐

All actions are logged with timestamps in `Gestion_utilisateur.log` and `Archivage.log`, providing a detailed record of operations performed and any errors encountered.

## Conclusion⭐

This Bash script project offers an efficient and automated solution for managing user accounts and directories in Unix systems, significantly improving the system administrator's workflow and reducing the potential for human error. The detailed logging ensures transparency and ease of troubleshooting.

## License🧾

This project is licensed under the MIT License.
