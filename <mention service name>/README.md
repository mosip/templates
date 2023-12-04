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

   docker build . --build-arg SOURCE=mosip --build-arg COMMIT_HASH= --build-arg COMMIT_ID= --build-arg BUILD_TIME=$(date +'%Y-%m-%d-%H-%M-%S') --file Dockerfile --tag "/:"