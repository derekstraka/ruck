FROM debian:testing

# Don't pin the packages versions to exact values
# hadolint ignore=DL3008
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        mmdebstrap \
		systemd \
        systemd-boot \
        python3-pip \
        python3-yaml \
        python3-rich \
        python3-stevedore \
        python3-cerberus \
        python3-systemd \
        dosfstools \
        systemd-container \
        git && \
        rm -rf /var/lib/apt/lists/*

COPY files/pip.conf /etc/pip.conf

RUN mkdir -p usr/src

