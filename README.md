# Pre-commit Config

Shared pre-commit configuration file that can be reused across multiple projects via Git Submodule.

## Usage

### Add as Submodule

```bash
cd /path/to/your/project

# Add as submodule
git submodule add https://github.com/YOUR_USERNAME/pre-commit-config.git .pre-commit-config-repo

# Or add with a specific branch
git submodule add -b main https://github.com/YOUR_USERNAME/pre-commit-config.git .pre-commit-config-repo

# Create symlink
ln -sf .pre-commit-config-repo/.pre-commit-config.yaml .pre-commit-config.yaml

# Install pre-commit hooks
pre-commit install

# Commit changes
git add .gitmodules .pre-commit-config-repo .pre-commit-config.yaml
git commit -m "Add pre-commit config as submodule"
```

### Clone a Project with This Submodule

```bash
# Option 1: Initialize submodule during clone
git clone --recursive https://github.com/YOUR_USERNAME/your-project.git

# Option 2: Initialize after clone
git submodule update --init
```

### Update to Latest Config

```bash
# Update submodule to latest remote version
git submodule update --remote .pre-commit-config-repo

# Commit the update
git add .pre-commit-config-repo
git commit -m "Update pre-commit config"
```
