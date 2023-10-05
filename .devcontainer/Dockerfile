FROM docker.io/zmkfirmware/zmk-dev-arm:stable

ARG ZMK_URL
ARG ZMK_BRANCH
ARG ZMK_PATH

# CLONE ZMK
RUN git clone --filter=tree:0 --single-branch --branch=${ZMK_BRANCH} ${ZMK_URL} ${ZMK_PATH}

# BUILD ZMK
RUN cd ${ZMK_PATH} && \
    west init -l app/ && \
    west update && \
    cd /

# CONFIGURE GIT
# RUN cd ${ZMK_PATH} && \
#     git config --global user.name "Roberto Lobo" \
#     git config --global user.email "rhlobo@gmail.com" \
#     cd /

RUN cd ${ZMK_PATH}
RUN git config --global user.name "Roberto Lobo"
RUN git config --global user.email "rhlobo@gmail.com"
RUN cd /
