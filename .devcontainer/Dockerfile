FROM docker.io/zmkfirmware/zmk-dev-arm:stable


ARG ZMK_URL
ARG ZMK_BRANCH
ARG ZMK_PATH


# CLONE ZMK
RUN git clone --filter=tree:0 --single-branch --branch=${ZMK_BRANCH} ${ZMK_URL} ${ZMK_PATH}


# SET WORKDIR
WORKDIR ${ZMK_PATH}


# BUILD ZMK
RUN west init -l app/
RUN west update || west update || west update


# CONFIGURE GIT
RUN git config --global user.name "Roberto Lobo"
RUN git config --global user.email "rhlobo@gmail.com"


# RUN cd /
