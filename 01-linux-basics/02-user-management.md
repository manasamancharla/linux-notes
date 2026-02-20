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
