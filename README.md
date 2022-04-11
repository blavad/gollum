# Gollum Handbook


- [1. Features](#features)
    - [CPU infos](#information-about-cpus)
    - [GPU infos](#information-about-gpus)
    - [Memory infos](#information-about-ram)
- [2. User manual](#user-manual)
    - [Accessing gollum](#connexion-to-gollum)
- [3. Administrator manual](#admin-manual)
    - [Manage users](#manage-users)
    - [Manage groups](#manage-groups)

## Features

### Information about CPUs 
- *Last update: 11/04/2022*

```sh
Architecture:        x86_64
CPU op-mode(s):      32-bit, 64-bit
Byte Order:          Little Endian
CPU(s):              16
On-line CPU(s) list: 0-15
Thread(s) per core:  2
Core(s) per socket:  4
Socket(s):           2
NUMA node(s):        2
Vendor ID:           GenuineIntel
CPU family:          6
Model:               63
Model name:          Intel(R) Xeon(R) CPU E5-2623 v3 @ 3.00GHz
Stepping:            2
CPU MHz:             1197.719
CPU max MHz:         3500,0000
CPU min MHz:         1200,0000
BogoMIPS:            5985.81
Virtualization:      VT-x
L1d cache:           32K
L1i cache:           32K
L2 cache:            256K
L3 cache:            10240K
NUMA node0 CPU(s):   0-3,8-11
NUMA node1 CPU(s):   4-7,12-15
```

### Information about GPUs 
- *Last update: 11/04/2022*


### Information about RAM 
- *Last update: 11/04/2022*


## User manual

### Connexion to Gollum

You can connect to gollum via the insa network ***eduoram***. 

```sh
ssh username@gollum.citi.insa-lyon.fr
```

If you are connected to another network, you will first need to access the VPN of INSA (i.e. ***https://sslvpn.cisr.fr***). On linux, this can be done using `openconnect` tools.

```sh
sudo openconnect https://sslvpn.cisr.fr
ssh [USERNAME]@gollum.citi.insa-lyon.fr
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
sudo usermod -a -G [GROUPNAME] [USERNAME]
```
