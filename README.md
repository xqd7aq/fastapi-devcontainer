# Learning Environments

Strategies for consistent student learning environments.

## 1. GitHub Codespaces

Built into the GitHub UI is a web-based dev environment that is free to use. In some ways this
makes the perfect fallback environment for any student experiencing issues on their local
workstation.

## Advantages:

- One-click environment
- Templates: VS Code, Jupyter, etc.
- Built-in integration with GitHub
- Web-based (no software required)
- Customizable

## Disadvantages:

- Only 2 cores / 8 GB of memory
- Appears to have no native R support
- Good for development, NOT usable for larger workloads
- Requires students to be familiar with "remote" local development

## Try It

From the main page of any GitHub repository, find the **CODE** drop-down button. In the top
of the tab that appears, there is a Codespaces pane. Click into that and select "Create codespace".

Your codespace will open in a new browser tab, and will hibernate when you close the tab. They are
automatically deleted after 30 days of non-use.

To see or manage your codespaces, visit **`https://github.com/codespaces/`**

## 2. VS Code Devcontainers

The "terminal" of VS Code natively offers the user a command-line to her/his local environment.
This can be customized in a variety of ways, for example Windows users running WSL can use that
terminal within VS Code, along with PowerShell or the Windows CMD.

Devcontainers provide a method for consistent, and truly local, terminals by containerizing the
interactive terminal. This means all students have the same software, the same environment configuration,
and the same paths to their work.

Advantages:

- Truly local environment, entirely on the student machine
- Completely customizable
