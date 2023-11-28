## Templates

## Overview
This repo contains all the required templates for all our respective teams.

## Checklist for using templates 

1) .github - In .github folder add the required keys and workflows.

2) mention service name - mention the services name for repo,
                          a) add required code under.
                          b) make changes in dockerfile as per requirement.
                          c) make changes in pom.xml as per requirement.

3) db_scripts - Add the required ddl and dml change the <service name>

4) db_upgrade_scripts - Rename the service name under db_upgrade_script, add rollback.sql and upgrade.sql scripts.