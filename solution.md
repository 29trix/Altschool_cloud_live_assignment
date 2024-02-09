## Assignment Solution
### Prerequisite

i. Create a login user: `sudo adduser -m altschool`

ii. login to the altschool user home directory `su - altschool`

iii. Create the requested directories (_code, tests, personal and misc_): `mkdir code tests personal misc`

### Solution to task a-m

| Tasks | Task description | Solution |

|-------|------------------|------------|

|a      | Change to the tests directory using absolute pathname | `cd /home/altschool/tests` |

|b      | Change to the tests directory from your home directory using relative pathname | `cd ./test` |

|c      |  Use echo command to create a file named fileA with text content ‘Hello A’ in the misc directory | `echo "Hello A" > /home/altschool/misc/fileA`   |

|d      | Create an empty file named fileB and polulate it with dummy contents | `head -c /dev/urandom ./misc/fileB |

|e      | Copy contents of fileA into fileC               | `cp ./misc/fileA ./misc/fileC  |

|f      | Move contents of fileB into fileD | `mv ./misc/fileB ./misc/fileD`  |

|g      | Create a tar archive called misc.tar for the contents of the misc directory | `tar -cf misc.tar misc.tar` |
|h      | Compress the tar archive to create a misc.tar.gz file | `gzip misc.tar` |
