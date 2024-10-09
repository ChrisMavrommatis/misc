# Git Repo Structure

This document describes the best practices for a repo structure.
It is compiled information and according to my taste

```bash
/
├── src/                            # Source code of the application
├── test/                           # Unit tests, integration tests etc
├── config/ or .config/             # Configuration files related to local setup
├── build/ or .build/               # Build scripts (Powershell, Docker Compose ...)
├── dist/                           # Distribution-ready files (if applicable, often ignored in git)
├── dep/                            # Project dependencies (optional)
├── doc/                            # Documentation files (if applicable)
├── res/                            # Static resources
├── samples/ or examples/           # Providing samples that support the documentation
├── tools/                          # Convinience directory. Build scripts, rename scripts usualy .sh or .cmd
├── .gitignore
└── .github/                        # GitHub-specific configuration (workflows, issue templates)
    ├── workflows/                  # GitHub Actions CI/CD workflows
    └── ISSUE_TEMPLATE.md           # GitHub issue templates                        

```
