# Ansible configuration for CMS like applications

## Database params
To keep sensible information away from control version system, we should to create a bash script file that export database connetion parameters as environment variables that are used in group_vars/dbservers

* Ceate a file DATABASE_PARAMS containig the following lines:

``` sh
#!/bin/bash

export VM_CRC_DB_NAME="database_name"
export VM_CRC_DB_USER="database_user"
export VM_CRC_DB_PASSWD="database_secret"
```

Save the file and source it

``` sh
source DATABASE_PARAMS
```

* Finally you can check if environment variables where created

``` sh
env | grep VM_CRC
```

