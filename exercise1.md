## Assignment Solution

### Prerequisite

i. Create a login user: `sudo adduser  altschool`

ii. login to the altschool user home directory `su - altschool`

iii. Create the requested directories (_code, tests, personal and misc_): `mkdir code tests personal misc`

### Solution to task a-m

| Task  | Task description | Solution | Images |
|-------|------------------|------------|------|
|a      | Change to the tests directory using absolute pathname | `cd /home/altschool/tests` | ![change_dir](./assets/absolute_path.png) |
|b      | Change to the tests directory from your home directory using relative pathname | `cd ./test` | ![realative_path](./assets/realative_path.png) |
|c      | Use echo command to create a file named fileA with text content ‘Hello A’ in the misc directory | `echo "Hello A" > /home/altschool/misc/fileA` | ![echo](./assets/echo_command.png) |
|d      | Create an empty file named fileB and populate it with dummy contents |create empty `touch fileB` then populate `head -c 720 /dev/urandom ./misc/fileB` | ![dummy](./assets/dummy.png) |
|e      | Copy contents of fileA into fileC               | `cp ./misc/fileA ./misc/fileC` | ![copy](./assets/copy_content.png) |
|f      | Move contents of fileB into fileD | `mv ./misc/fileB ./misc/fileD`  | ![move](./assets/move_content.png) |
|g      | Create a tar archive called misc.tar for the contents of the misc directory | `tar -cf misc.tar misc` | ![tar archive](./assets/tar_archive) |
|h      | Compress the tar archive to create a misc.tar.gz file | `gzip misc.tar` | ![tar.gz](./assets/gzip.png) |
|i      | Create a user and force the user to change his password upon login | first of create a user with `sudo adduser user1` then force user to change password with `sudo chage -d 0 user1` | ![admin enforce](./assets/admin_enforced.png) |
|j      | Lock a users password | `sudo passwd -l user1` | ![lock users password](./assets/lock_user_passwd.png) |
|k      | Create a user with no login shell | `sudo useradd -s /sbin/nologin user2` | ![no login](./assets/nologin_shell.png) |
|l      | Disable password based authentication for ssh | `sudo vi /etc/ssh/sshd_config` and  insert `PasswordAuthentication no` | ![disable PasswordAuthentication](./assets/disable_passAuth.png) |
|m      | Disable root login for ssh | `sudo vi /etc/ssh/sshd_config` and set `PermitRootLogin no`  | ![diable root login](./assets/disable_passAuth.png) |
