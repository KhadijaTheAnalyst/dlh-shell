# Permissions Scripts
##Scripts Description
### 0-iam_betty
- **Purpose**: Switches the current user to the user 'betty'
-**Command**: 'su betty'
### 1-who_am_i
- **Purpose**: Prints the effective username of the current user
- **Command**: `whoami`
- **Usage**: `./1-who_am_i`
### 2-groups
- **Purpose**: Prints all the groups the current user is part of
- **Command**: `groups`
- **Usage**: `./2-groups`
### 3-new_owner
- **Purpose**: Changes the owner of the file `hello` to user `betty`
- **Command**: `chown betty hello`
- **Usage**: `sudo ./3-new_owner`
- **Requirements**: Must be run with sudo (root privileges)
