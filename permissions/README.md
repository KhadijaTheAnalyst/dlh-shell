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
### 6-multiple_permissions
- **Purpose**: Adds execute to owner and group, read to other for file `hello`
- **Command**: `chmod u+x,g+x,o+r hello`
- **Usage**: `./6-multiple_permissions`
- **Permissions change**: `-rw-r-----` (640) → `-rwxr-xr--` (754)
### 7-everybody
- **Purpose**: Adds execute permission to owner, group, and other for file `hello`
- **Command**: `chmod a+x hello`
- **Usage**: `./7-everybody`
- **Permissions change**: `-rw-r-----` (640) → `-rwxr-x--x` (751)
- **Note**: Uses `a+x` (all) instead of commas to avoid restriction
### 8-James_Bond
- **Purpose**: Sets permissions so only other users have all permissions
- **Command**: `chmod 007 hello`
- **Usage**: `./8-James_Bond`
- **Permissions**: `-------rwx` (007)
- **Note**: Owner and group have NO permissions, others have rwx
- **Method**: Uses octal (numeric) to avoid comma restriction
### 9-John_Doe
- **Purpose**: Sets file `hello` to specific permissions (-rwxr-x-wx)
- **Command**: `chmod 753 hello`
- **Usage**: `./9-John_Doe`
- **Permissions**: `-rwxr-x-wx` (753)
- **Breakdown**: Owner=rwx(7), Group=r-x(5), Other=-wx(3)
- **Method**: Uses octal (numeric) to avoid comma restriction
### 10-mirror_permissions
- **Purpose**: Sets file `hello` to have same permissions as file `olleh`
- **Command**: `chmod --reference=olleh hello`
- **Usage**: `./10-mirror_permissions`
- **Note**: Works with ANY permissions - dynamically copies from olleh to hello
- **Method**: Uses `--reference` flag to mirror permissions
