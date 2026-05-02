FROM mcr.microsoft.com/devcontainers/base:ubuntu

COPY --from=jdxcode/mise /usr/local/bin/mise /usr/local/bin/

#make sure this is activated to both zsh and bash. Might be overridden by user's dotfiles.
RUN echo 'eval "$(mise activate bash)"' >> /home/vscode/.bashrc && \
    echo 'eval "$(mise activate zsh)"' >> /home/vscode/.zshrc

ENV MISE_CONFIG_TRUST=all

RUN apt-get update && apt-get install -y iputils-ping