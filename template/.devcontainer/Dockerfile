FROM  mcr.microsoft.com/devcontainers/python:latest

USER vscode

# Install additional packages with APT.
RUN <<-EOT
  set -eux

  export DEBIAN_FRONTEND=noninteractive

  sudo apt-get update

  sudo apt-get install --yes --no-install-recommends \
    curl \
    dnsutils \
    gnupg2
EOT

# Install additional packages with pipx.
RUN <<-EOT
	set -eux

  pipx --version

	pipx install \
    copier \
    pre-commit \
    uv
EOT

# Install Task with the official installer.
# Set up completion in Bash.
RUN <<-EOT
	set -eux

  mkdir -p ~/.local/bin
  curl --location --silent --show-error --fail \
    https://taskfile.dev/install.sh |
    sh -s -- -d -b ~/.local/bin

  mkdir -p ~/.local/share/bash-completion/completions
  ~/.local/bin/task --completion bash \
    > ~/.local/share/bash-completion/completions/task
EOT
