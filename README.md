# Learning Environments

Strategies for consistent SDS learning environments.

Goals:

- Identical environments for everyone
- Consistent software paths (`/usr/bin/`, `/bin/`, etc.)
- Common methods for installing software (`apt`, `yum`, `pip` etc.)
- Easy setup
- Integration with GitHub

## 0. UVA SDS VSCode Extension Pack

From within VS Code, search the Extensions for "UVA SDS" and you will find an extension pack that currently loads 29 additional plugins. These are currently curated for the first year of the BSDS curriculum.

Additional extensions can be added, or more Extension Packs can be published.

## 1. VSCode Devcontainers

The "terminal" of VS Code natively offers the user a command-line to her/his local environment, invoking `bash`, `zsh`, Windows PowerShell, Windows CMD, etc. This can be customized in a variety of ways, for example Windows users running WSL can use that terminal within VS Code, along with PowerShell or the Windows CMD.

Devcontainers provide a method for consistent local terminals by containerizing the interactive terminal. This means all students have the same software, the same environment configuration, and the same paths to their work.

### Advantages :thumbsup:

- Truly local environment, runs 100% on the student machine.
- Configuration can also be used in GitHub Codespaces!
- Supports most languages: Python, R, etc.
- Completely customizable. Can even use custom Dockerfile.
- Allows for port mappings, volume mappings, between computer and container

### Disadvantages :thumbsdown:

- Requires an understanding of the `devcontainers.json` file
- Built-in GitHub authentication is not automatic in all scenarios
- Available container images are specifically built for this use
- Access to other local files (`.ssh` directory, etc.) must be mapped in

### Try It

Fork **https://github.com/UVADS/learning-environments** to explore a working Devcontainer environment.

Note the `.devcontainer/devcontainer.json` file, which configures the environment. This can include:

- Base devcontainer image to use; OR
- Dockerfile to build from
- Environment variables
- Mounts of local storage into the devcontainer
- Commands to run upon creation
- Port forwarding, etc.
- Other features available

## 2. GitHub Codespaces :octocat:

Built into the GitHub UI is a web-based dev environment that is free to use. In some ways this makes the perfect fallback environment for any student experiencing issues on their local workstation. Codespaces can be partially configured using the `devcontainer.json` file from above.

> [**Codespaces**](https://github.com/features/codespaces) - fully configured, secure cloud development environments native to GitHub. **GitHub Education** faculty can get double the resources for free.

### Advantages :thumbsup:

- One-click environment
- Templates: VS Code, Jupyter, etc.
- Built-in integration with GitHub
- Web-based (no software required)
- Customizable

### Disadvantages :thumbsdown:

- Only 2 cores / 8 GB of memory. More for GitHub Education
- Some community support for R but no native option
- Good for development, NOT usable for larger workloads
- Requires students to be familiar with "remote" local development

### Try It

From the main page of any GitHub repository, find the **CODE** drop-down button. In the top of the tab that appears, there is a Codespaces pane. Click into that and select "Create codespace".

Your codespace will open in a new browser tab, and will hibernate when you close the tab. They are automatically deleted after 30 days of non-use.

To see or manage your codespaces, visit [**`https://github.com/codespaces/`**](https://github.com/codespaces/)