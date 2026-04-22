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
### 4-empty
- **Purpose**: Creates an empty file called `hello`
- **Command**: `touch hello`
- **Usage**: `./4-empty`
### 5-execute
- **Purpose**: Adds execute permission to the owner of file `hello`
- **Command**: `chmod u+x hello`
- **Usage**: `./5-execute`
- **Permissions change**: `-rw-rw-r--` → `-rwxrw-r--`
eof
### 6-multiple_permissions
- **Purpose**: Adds execute to owner and group, read to other for file `hello`
- **Command**: `chmod u+x,g+x,o+r hello`
- **Usage**: `./6-multiple_permissions`
- **Permissions change**: `-rw-r-----` (640) → `-rwxr-xr--` (754)
