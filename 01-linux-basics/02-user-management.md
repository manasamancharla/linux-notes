# User Management

Multiple Users can use the system simultaneously. This brings User Management into the picture as it is important to give controlled access to the users. 

## Creating Users in Linux
To create a new user in Linux, use:
```bash
useradd username
```
This creates a user without a home directory.

To create a user with a home directory:
```bash
useradd -m username
```

To specify a shell:
```bash
useradd -s /bin/bash username
```

## Managing User Passwords
To set or change a user’s password:
```bash
passwd username
```

### Enforcing Password Policies
- **Password expiration**: Set password expiry days
  ```bash
  chage -M 90 username
  ```
- **Lock a user account**
  ```bash
  passwd -l username
  ```
- **Unlock a user account**
  ```bash
  passwd -u username
  ```

## Modifying Users
Modify an existing user with usermod:
- Change the username:
  ```bash
  usermod -l new_username old_username
  ```
- Change the home directory:
  ```bash
  usermod -d /new/home/directory -m username
  ```
- Change the default shell:
  ```bash
  usermod -s /bin/zsh username
  ```

## Deleting Users
To remove a user but keep their home directory:
```bash
userdel username
```
To remove a user and their home directory:
```bash
userdel -r username
```

##  Working with Groups
### Creating Groups
```bash
groupadd groupname
```

### Adding Users to Groups
```bash
gpasswd -a username groupname 
```
```bash
gpasswd -M username,username,username groupname 
```

Using `usermod`
```bash
usermod -aG groupname username
```
Here `a` is append and `G` is set supplementary group. Without `a` the command wipes out other supplementary groups.  

### Adding a User to Sudo Group

```bash
usermod -aG sudo username
```
## getent (get entries)
It is used to retrieve entries from system databases defined in `/etc/nsswitch.conf`

```bash
getent database key
```
## Working with passwd and group files
### View passwd file contents

```bash
cat /etc/passwd
```
Using `getent`
```bash
getent passwd
```

### View group file contents

```bash
cat /etc/group
```
Using `getent`
```bash
getent group
```


### Check user's groups

```bash
id username
```



