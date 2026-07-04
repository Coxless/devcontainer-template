FROM mcr.microsoft.com/devcontainers/base:ubuntu

# Pre-create the workspace dir owned by vscode so the named volume mounted
# there (see devcontainer.json workspaceMount) inherits correct ownership.
RUN mkdir -p /workspace && chown vscode:vscode /workspace

USER vscode

# Claude Code (installs into ~/.local/bin for the vscode user)
RUN curl -fsSL https://claude.ai/install.sh | bash
ENV PATH="/home/vscode/.local/bin:${PATH}"
