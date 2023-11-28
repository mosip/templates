## <mention service name>

## Overview
<add overview of the service>

## Databases
Refer to [SQL scripts](db_scripts).

## Build & run (for developers)
The project requires <mention build tool>.
1. Build and install:
    ```
    $ cd kernel
    $ mvn install -DskipTests=true -<mention required service>.skip=true -Dgpg.skip=true
    ```
1. Build Docker for a service:
    ```
    $ cd <service folder>
    $ docker build -f Dockerfile