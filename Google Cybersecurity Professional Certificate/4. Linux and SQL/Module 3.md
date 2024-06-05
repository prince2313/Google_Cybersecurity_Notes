# Linux commands in the Bash shell
## Linux commands via the Bash shell

- **Security analysts:**
	- Work with server logs.
	- Navigate, manage, and analyze files remotely.
	- Verify and configure users and group access.
	- Give authorization and set file permissions.

- **Command:**
	- An instruction telling the computer to do something.

- **Argument (Linux):**
	- Specific information needed by a command.

---
## Filesystem Navigation and Reading File Content

### Filesystem Hierarchy Standard (FHS)

- FHS organizes data in Linux.
- Key directories: `/home`, `/bin`, `/etc`, `/tmp`, `/mnt`.

#### Root directory

- Highest-level directory.
- Always represented as `/`.
- All subdirectories branch off from it.

#### Standard FHS directories

- Examples: `/home`, `/bin`, `/etc`, `/tmp`, `/mnt`.
- `/bin`: Contains binaries and executables.
- `/etc`: Stores system configuration files.
- `/tmp`: Stores temporary files.
- `/mnt`: Stores mount points for external media.

#### User-specific subdirectories

- Located under `/home`.
- Each user has their own subdirectories.
- Represented as `~/` for the user's home directory.

### Key commands for navigation

#### pwd
- Prints current directory.
- Example: `/home/analyst`.

#### ls
- Lists files and directories.
- Example: `ls /home/analyst/projects`.

#### cd
- Navigates between directories.
- Example: `cd projects`.

### Relative and Absolute Paths

- **Relative path:** Starts from the current directory.
  - Example: `../projects` (Moves up one directory then enters the projects directory).

- **Absolute path:** Starts from the root directory.
  - Example: `/home/analyst/projects` (Directly accesses the projects directory under analyst's home).

### Common commands for reading file content

#### cat
- Displays entire file content.

#### head
- Displays beginning of file (by default 10 lines).

#### tail
- Displays end of file (by default 10 lines).

#### less
- Displays content one page at a time.
- Useful for large files.

### Key takeaways

- Understanding FHS and key commands is crucial for Linux navigation.
- Reading file content is important for security analysis.
- Mastering these commands aids troubleshooting and maintaining system security.

---
## Filter content in Linux

### Filtering

- **Definition**: Selecting data that match a certain condition.

### grep

- **Definition**: Command to search a specified file for lines containing a specified string or text.
  - **Usage**: Takes two arguments: string to search for and file to search through.
  - **Example**: `grep OS updates.txt` returns lines containing "OS" in "updates.txt".

### Piping

- **Definition**: Sending standard output of one command as standard input to another for further processing.
  - **Character**: Pipe command accessed using | character.
  - **Function**: Sends output of one command to another.

### find

- **Definition**: Command to search for directories and files meeting specified criteria.
  - **Criteria**: Include name, file size, or modification time.
  - **Options**: Modify behavior, commonly begin with a hyphen (-).
  - **-name and -iname**: Find file or directory names containing a specific string.
    - **Difference**: -name is case-sensitive, -iname is not.
  - **-mtime**: Find files or directories last modified within a certain time frame.
    - **Usage**: -mtime option with a number of days.
    - **-mtime +1**: Modified more than one day ago.
    - **-mtime -1**: Modified less than one day ago.

---
## Manage directories and files

### Creating and modifying directories

#### mkdir

- **Definition**: Command to create a new directory.
  - **Usage**: Provide either absolute or relative file path.
  - **Example**: `mkdir /home/analyst/logs/network`.

#### rmdir

- **Definition**: Command to remove a directory.
  - **Note**: Cannot delete directories with files or subdirectories inside.

### Creating and modifying files

#### touch and rm

- **touch**: Command to create a new file.
- **rm**: Command to remove a file.
  - **Caution**: Not easy to recover files deleted with `rm`.

#### mv and cp

- **mv**: Command to move a file or directory to a new location.
- **cp**: Command to copy a file or directory to a new location.
  - **Note**: `mv` can also rename files.

### nano text editor

- **nano**: Command-line file editor available in many Linux distributions.
  - **Usage**: Create new files, modify file contents.
  - **Saving**: Use Ctrl + O to save, Ctrl + X to exit.

### Standard output redirection

- **Concept**: Redirecting standard output to files.
  - **Operators**: > (overwrite), >> (append).
  - **Caution**: Overwriting files with > can lead to data loss.
  - **Example**: `echo "last updated date" >> permissions.txt`.

### Key takeaways

- Managing the file system is crucial for security analysts.
- Commands like mkdir, rmdir, touch, rm, mv, and cp are essential.
- nano text editor is user-friendly for basic file editing.
- Standard output redirection with > and >> operators allows writing to files.

---
## File permissions and ownership

- **Permissions:**
	- The type of access granted for a file or directory.

- **Authorization:**
	- The concept of granting access to specific resources in a system.

- **Options:**
	- Input that modifies the behavior of a command.

---
## Permission Commands

### Reading Permissions

- Permissions in Linux: represented by a 10-character string.
- Types: read, write, execute for user, group, and other owners.
- 10-character string breakdown explained.

| Character | Example    | Meaning                                                                                                                                                          |
| --------- | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1st       | drwxrwxrwx | file type<br><ul><li>d for directory</li><li>- for a regular file</li></ul>                                                                                      |
| 2nd       | drwxrwxrwx | read permissions for the user<br><ul><li>r if the user has read permissions</li><li>- if the user lacks read permissions</li></ul>                               |
| 3rd       | drwxrwxrwx | write permissions for the user<br><ul><li>w if the user has write permissions</li><li>- if the user lacks write permissions</li></ul>                            |
| 4th       | drwxrwxrwx | execute permissions for the user<br><ul><li>x if the user has execute permissions</li><li>- if the user lacks execute permissions</li></ul>                      |
| 5th       | drwxrwxrwx | read permissions for the group<br><ul><li>r if the group has read permissions</li><li>- if the group lacks read permissions</li></ul>                            |
| 6th       | drwxrwxrwx | write permissions for the group<br><ul><li>w if the group has write permissions</li><li>- if the group lacks write permissions</li></ul>                         |
| 7th       | drwxrwxrwx | execute permissions for the group<br><ul><li>x if the group has execute permissions</li><li>- if the group lacks execute permissions</li></ul>                   |
| 8th       | drwxrwxrwx | read permissions for other<br><ul><li>r if the other owner type has read permissions</li><li>- if the other owner type lacks read permissions</li></ul>          |
| 9th       | drwxrwxrwx | write permissions for other<br><ul><li>w if the other owner type has write permissions</li><li>- if the other owner type lacks write permissions</li></ul>       |
| 10th      | drwxrwxrwx | execute permissions for other<br><ul><li>x if the other owner type has execute permissions</li><li>- if the other owner type lacks execute permissions</li></ul> |


### Exploring existing permissions

- `ls` command options:
  - `-a`: Displays hidden files.
  - `-l`: Displays permissions, owner, group, file size, and modification time.
  - `-la`: Combination of `-a` and `-l`.

### Principle of Least Privilege

- Grant minimal access required.

#### Changing Permissions

- `chmod` command:
    - Two arguments: changes and file/directory.
    - Examples of adding/removing permissions.
    - Using equals sign (=) to assign permissions exactly.

| Character | Description                                         |
| --------- | --------------------------------------------------- |
| u         | Indicates changes will be made to user permissions  |
| g         | Indicates changes will be made to group permissions |
| o         | Indicates changes will be made to other permissions |
| +         | Adds permissions to the user, group, or other       |
| -         | Removes permissions from the user, group, or other  |
| =         | Assigns permissions for the user, group, or other   |

#### The Principle of Least Privilege in Action

- Example scenario with bonuses.txt file.
- Initial permissions: `-rw-rw----`.
- Alignment with the principle of least privilege.
- Using `chmod` to restrict group permissions: `chmod g-rw bonuses.txt`.

### Key takeaways

- Importance for security analysts.
- Using `ls` with `-l` and `-la` to explore permissions.
- Using `chmod` to change permissions, ensuring alignment with the principle of least privilege.

---
## Responsible Use of sudo

### Problems with Logging in as Root

- **Root user (or superuser):**
	- A user with elevated privileges to modify the system.
- **Root User Risks**: 
  - Increased security risks if compromised.
  - Higher chance of irreversible mistakes.
  - Lack of command accountability.
- **Recommended Practice**: 
  - Use `sudo` instead of logging in as root.

### Authentication and Authorization with sudo

- **sudo Command**: 
  - Temporarily grants elevated permissions to specific users.
  - Users must be granted access in the "sudoers file."

#### useradd Command

- **Functionality**: 
  - Adds a user to the system.
- **Options**:
  - `-g`: Sets the user’s default group.
  - `-G`: Adds the user to additional groups.

#### usermod Command

- **Functionality**: 
  - Modifies existing user accounts.
- **Options**:
  - `-g`: Changes primary group.
  - `-G`: Adds supplemental groups.

#### userdel Command

- **Functionality**: 
  - Deletes a user from the system.
- **Options**:
  - `-r`: Deletes user's home directory.

#### chown Command

- **Functionality**: 
  - Changes ownership of a file or directory.
- **Usage**: 
  - Change user or group ownership.

### Key Takeaways

- **Authentication & Authorization**: 
  - sudo enables running commands with elevated privileges.
- **Commands Overview**: 
  - `useradd`, `usermod`, `userdel`, and `chown` for user and file ownership management.

---
## Linux Resources

### Linux Community

- **Overview**:
  - Extensive online community offering support and resources for Linux users.
  - Valuable for troubleshooting, learning, and sharing knowledge.
- **Resource**: [UNIX and Linux Stack Exchange](https://unix.stackexchange.com/)
  - Trusted platform for asking and answering Linux-related questions.
  - Community-driven voting system ensures high-quality solutions.

### Integrated Linux Support

#### man

- **Functionality**:
  - Displays detailed information about Linux commands ("manual").
- **Usage**:
  - Access command details by appending the command to `man`.
  - Example: `man chown` provides details about the `chown` command.

#### apropos

- **Functionality**:
  - Searches man page descriptions for specified strings.
- **Usage**:
  - Simplifies keyword searches within man pages.
  - Example: `apropos -a graph editor` searches for both "graph" and "editor" keywords.

#### whatis

- **Functionality**:
  - Provides concise command descriptions in a single line.
- **Usage**:
  - Offers quick insights into command functionalities.
  - Example: `whatis nano` gives a brief overview of the `nano` command.

### Key Takeaways

- **Community Support**:
  - Utilize the vast global community for troubleshooting and learning.
- **Integrated Commands**:
  - Leverage `man`, `apropos`, and `whatis` for comprehensive support directly within Linux.

### Resources for Further Learning

- Explore additional online resources to deepen Linux knowledge.
- [Unix and Linux Stack Exchange](https://unix.stackexchange.com/): A prominent platform for Linux-related discussions and queries.

---
## **Cybersecurity Terms and Concepts**

| Term                                   | Description                                                                                       |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Absolute file path                    | The full file path, which starts from the root                                                    |
| Argument (Linux)                      | Specific information needed by a command                                                          |
| Authentication                       | The process of verifying who someone is                                                           |
| Authorization                        | The concept of granting access to specific resources in a system                                   |
| Bash                                  | The default shell in most Linux distributions                                                      |
| Command                               | An instruction telling the computer to do something                                                |
| File path                             | The location of a file or directory                                                               |
| Filesystem Hierarchy Standard (FHS)  | The component of the Linux OS that organizes data                                                 |
| Filtering                             | Selecting data that match a certain condition                                                      |
| nano                                  | A command-line file editor that is available by default in many Linux distributions               |
| Options                               | Input that modifies the behavior of a command                                                      |
| Permissions                           | The type of access granted for a file or directory                                                 |
| Principle of least privilege          | The concept of granting only the minimal access and authorization required to complete a task     |
| Relative file path                    | A file path that starts from the user's current directory                                          |
| Root directory                       | The highest-level directory in Linux                                                              |
| Root user (or superuser)             | A user with elevated privileges to modify the system                                               |
| Standard input                        | Information received by the OS via the command line                                                |
| Standard output                       | Information returned by the OS through the shell                                                   |

---