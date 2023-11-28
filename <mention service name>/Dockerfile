## Reference for creating an Dockerfile:

---
## mention requred version of java
FROM

ARG SOURCE
ARG COMMIT_HASH
ARG COMMIT_ID
ARG BUILD_TIME

LABEL source=${SOURCE}
LABEL commit_hash=${COMMIT_HASH}
LABEL commit_id=${COMMIT_ID}
LABEL build_time=${BUILD_TIME}

ARG

ENV


# can be passed during Docker build as build time environment for github branch to pickup configuration from.
ARG container_user=mosip

# can be passed during Docker build as build time environment for github branch to pickup configuration from.
ARG container_user_group=mosip

# can be passed during Docker build as build time environment for github branch to pickup configuration from.
ARG container_user_uid=1001

# can be passed during Docker build as build time environment for github branch to pickup configuration from.
ARG container_user_gid=1001

# install packages and create user
RUN <Install required packages & create ${container_user/group} with group ${container_user_uid/gid> \

# set working directory for the user
WORKDIR /home/${container_user}

ENV work_dir=/home/${container_user}

## Add required path according location of file.multiple ADD can be added to Dockerfile.
ADD <mention service name>/<mention folder name>/target ./<mention folder name>/target

ADD configure.sh configure.sh

# change permissions of file inside working dir
RUN chown -R ${container_user}:${container_user} /home/${container_user}
RUN chown -R ${container_user}:${container_user} /var/www

# select container user for all tasks
#USER ${container_user_uid}:${container_user_gid}

ENTRYPOINT ["./entrypoint.sh" ]

---

## The complete block above explains creation of Dockerfile.