FROM ubuntu

WORKDIR /root


RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get full-upgrade -y \
    && apt-get autoremove -y \
    && apt-get install wget -y \
    && wget https://github.com/containers/podman/releases/download/v5.8.1/podman-remote-static-linux_amd64.tar.gz \
    && tar -C /usr/local/ -xzf podman-remote-static-linux_amd64.tar.gz \
    && echo "export PATH=$PATH:/usr/local/bin" >> ~/.bashrc \
    && ln -sf /usr/local/bin/podman-remote-static-linux_amd64 /usr/local/bin/podman

WORKDIR /workspaces

CMD [ "/bin/bash" ]