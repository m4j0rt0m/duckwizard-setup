# duckWizard Setup

<div align="center">
  <img src="./logo.png" alt="duckWizard Logo" width="200"/>
</div>

`duckWizard-setup` provides easy-to-use scripts for initializing and upgrading the environment for projects that use the `duckWizard` framework. These scripts, `duckwizard-init` and `duckwizard-upgrade`, simplify the process of setting up and maintaining a consistent project structure across different platforms.

## Features

- duckwizard-init: Initializes a new project environment, setting up required directories, files, and configuration.
- duckwizard-upgrade: Upgrades an existing project environment by merging local changes with the latest configuration and files.
- Designed for compatibility with various Linux distributions (Ubuntu, Fedora, Arch, etc.).

### 1. `duckwizard-init`

The `duckwizard-init` script is used to initialize a new project environment, creating the required directory structure and necessary configuration files.

#### Example usage:

```bash
duckwizard-init
```

- Initializes the environment by creating essential directories (e.g., `src/rtl`, `tb/rtl`, etc.).
- Ensures the `project.config` and `.duckwizard` directories are set up correctly.
- If a `Makefile` is missing, it creates one with the necessary includes for `duckWizard`.
- If `.duckwizard` or `project.config` already exists, it asks if you want to upgrade the environment.

### 2. `duckwizard-upgrade`

The `duckwizard-upgrade` script merges local changes in `project.config` with the latest version of the configuration file, ensuring that local modifications are preserved while pulling in updates.

#### Example usage:

```bash
duckwizard-upgrade
```

- Checks if there are any differences between the current `project.config` and `.duckwizard/project.config.orig`.
- Merges any updates from `.duckwizard` into the local environment.
- Updates `.duckwizard` if necessary.

## Customization

The scripts can be adapted for use with other directory structures, configurations, or specific tools. They provide flexibility to fit into various project setups.

## Compatibility

These scripts are compatible with the following Linux distributions:

- Ubuntu
- Fedora
- Arch
- Other Unix-based systems

If additional support or custom modifications are needed, the scripts can be easily adjusted to fit any setup.

## Contributions

Contributions to `duckWizard-setup` are welcome! Feel free to open issues, submit pull requests, or suggest improvements.

## License

This repository is licensed under the MIT License. See the [LICENSE](./LICENSE) file for more details.
