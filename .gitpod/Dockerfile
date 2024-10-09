FROM gitpod/workspace-base

# Install kubectl
RUN curl -LO https://dl.k8s.io/release/$(curl -Ls https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl && \
    chmod +x ./kubectl && \
    sudo mv ./kubectl /usr/local/bin/kubectl

# Install kubectx & kubens
RUN sudo git clone https://github.com/ahmetb/kubectx /opt/kubectx && \
    sudo ln -s /opt/kubectx/kubectx /usr/local/bin/kubectx && \
    sudo ln -s /opt/kubectx/kubens /usr/local/bin/kubens && \
    COMPDIR=$(pkg-config --variable=completionsdir bash-completion) && \
    sudo ln -sf /opt/kubectx/completion/kubens.bash $COMPDIR/kubens && \
    sudo ln -sf /opt/kubectx/completion/kubectx.bash $COMPDIR/kubectx

# Install helm
RUN curl https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 | bash
