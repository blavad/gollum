# Handbook


- [1. Features](#features)
- [2. User manual](#user-manual)
- [3. Administrator manual](#admin-manual)
    - [Manage users](#manage-users)
    - [Manage groups](#manage-groups)

## Features

## User manual

### Connexion to Gollum
```sh
ssh username@gollum.citi.insa-lyon.fr
```

## Admin manual

### Manage users

```sh
# List users and infos
cat /etc/passwd

# Add a new user
sudo adduser [USERNAME]

# Delete a user account
sudo userdel -r [USERNAME]
```

### Manage groups

```sh

# List groups and infos
cat /etc/group

# Add a group 
sudo groupadd [GROUPNAME] 

# Add a user in a group (useful to add users in docker group)
usermod -a -G [GROUPNAME] [USERNAME]
```
