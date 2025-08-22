# Mac AI Dev Kit — Boilerplate (SE)

Pick & choose. Read comments before running.

---

## 1) Install Homebrew (Mac package manager)

Lets us install apps/tools easily from terminal.

```bash
if ! command -v brew >/dev/null; then
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
  eval "$(/opt/homebrew/bin/brew shellenv)"
fi

## 2) Terminal Productivity Tools

brew install --quiet \
  iterm2 \                # Better terminal app than default Mac Terminal
  starship \              # Fancy prompt: shows git branch, errors, time
  zsh-autosuggestions \   # Suggests commands as you type
  zsh-completions \       # Adds more tab-completion
  fzf \                   # Fuzzy finder for files, commands, git history
  ripgrep \               # Super-fast text search in files
  bat \                   # "cat" replacement with syntax highlighting
  eza \                   # "ls" replacement with colors & icons
  fd \                    # Faster file search than 'find'
  zoxide \                # Jump to folders quickly by name
  btop \                  # Resource monitor (CPU, RAM, etc.)
  git \                   # Version control
  gh \                    # GitHub CLI
  lazygit \               # Git TUI (manage commits visually)
  gpg \                   # Encryption/signing keys
  coreutils \             # GNU core tools (more Linux-like behavior)
  findutils \             # GNU find/xargs
  wget \                  # File downloader
  curl \                  # URL/HTTP tool
  jq \                    # JSON query tool
  yq \                    # YAML query tool
  neovim                  # Modern terminal-based text editor

## 3) Editor/IDE

brew install --quiet vscodium  # Open-source VS Code (no telemetry)

 ## 4) Languages & runtimes

brew install --quiet uv   # Super-fast Python package/venv manager
brew install --quiet fnm  # Fast Node.js version manager
brew install --quiet go   # Go programming language

## 5) Containers (without Docker Desktop)

brew install --quiet colima           # Lightweight Docker VM for Mac
brew install --quiet docker           # Docker CLI
brew install --quiet docker-buildx    # Docker build toolkit
brew install --quiet docker-compose   # Run multi-container apps

## 6) Kubernetes Toolchain

brew install --quiet \
  kubernetes-cli \   # kubectl: main K8s CLI
  kind \             # Run K8s clusters locally in Docker
  k3d \              # Lightweight multi-node K8s in Docker
  helm \             # K8s package manager (charts)
  kustomize \        # Customize YAML configs
  k9s \              # Terminal UI for managing clusters
  kubectx \          # Switch between clusters
  stern \            # Stream pod logs
  tilt \             # Live-reload dev into K8s
  skaffold           # Build/deploy workflows for K8s apps

## 7) API & HTTP testing tools
brew install --quiet httpie              # Friendlier curl for APIs
brew install --cask --quiet bruno        # Open-source Postman alternative

## 8) Database clients
brew install --cask --quiet dbeaver-community   # Cross-platform DB tool
# brew install --cask --quiet beekeeper-studio # (optional) Another DB GUI

## 9) Local AI model tooling
brew install --quiet ollama   # Easiest way to run LLMs locally
# MLX for Apple Silicon — installed later via pip:
# python3 -m pip install mlx-lm
