FROM mcr.microsoft.com/devcontainers/universal:2

RUN sudo git clone https://github.com/ahmetb/kubectx /opt/kubectx && \
    sudo ln -s /opt/kubectx/kubectx /usr/local/bin/kubectx && \
    sudo ln -s /opt/kubectx/kubens /usr/local/bin/kubens && \
    COMPDIR=$(pkg-config --variable=completionsdir bash-completion) && \
    sudo ln -sf /opt/kubectx/completion/kubens.bash $COMPDIR/kubens && \
    sudo ln -sf /opt/kubectx/completion/kubectx.bash $COMPDIR/kubectx
