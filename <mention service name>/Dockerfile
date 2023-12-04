## Reference for creating an Dockerfile:

## mention requred version of java
FROM <tag-name>

ARG SOURCE
ARG COMMIT_HASH
ARG COMMIT_ID
ARG BUILD_TIME

LABEL source=${SOURCE}
LABEL commit_hash=${COMMIT_HASH}
LABEL commit_id=${COMMIT_ID}
LABEL build_time=${BUILD_TIME}

# You can add multiple the environment (ENV) and argument variables (ARG).

ARG <arg_name>=arg-name

ENV <env-variable-name>="env-var-value"

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
ADD <mention service name>/<mention folder name>/target ./<mention folder name>/

ADD entrypoint.sh $work_dir/entrypoint.sh

RUN chmod +x $work_dir/entrypoint.sh

# change permissions of file inside working dir
RUN chown -R ${container_user}:${container_user} <other-directories>
RUN chown -R ${container_user}:${container_user} <other-directories>

# select container user for all tasks
USER ${container_user_uid}:${container_user_gid}

ENTRYPOINT ["./entrypoint.sh" ]

