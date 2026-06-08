# Packer Plugin Magalu Cloud

[![CI](https://github.com/MagaluCloud/packer-plugin-magalucloud/actions/workflows/ci.yml/badge.svg?event=push)](https://github.com/MagaluCloud/packer-plugin-magalucloud/actions/workflows/ci.yml)
[![Release](https://github.com/MagaluCloud/packer-plugin-magalucloud/actions/workflows/release.yml/badge.svg)](https://github.com/MagaluCloud/packer-plugin-magalucloud/actions/workflows/release.yml)

The `Magalu Cloud` multi-component plugin can be used with HashiCorp [Packer](https://www.packer.io) to create custom images.
For the full list of available features for this plugin see [docs](docs).

## Installation

### Using pre-built releases

#### Using the `packer init` command

Starting from version 1.7, Packer supports a new `packer init` command allowing automatic installation of Packer plugins.
Read the [Packer documentation](https://developer.hashicorp.com/packer/docs/commands/init) for more information.

To install this plugin, copy and paste this code into your Packer configuration.
Then, run [`packer init`](https://developer.hashicorp.com/packer/docs/commands/init).

```hcl
packer {
  required_plugins {
    magalucloud = {
      source  = "github.com/MagaluCloud/magalucloud"
      version = ">= 0.3.0"
    }
  }
}
```
**Note: Update to Packer Plugin Installation**

With the new Packer release starting from version 1.14.0, the `packer init` command will automatically install official plugins from the [HashiCorp release site.](https://releases.hashicorp.com/).

Going forward, to use newer versions of official Packer plugins, you'll need to upgrade to Packer version 1.14.0 or later.
If you're using an older version, you can still install plugins, but as a workaround, you'll need to [manually install them using the CLI.](https://developer.hashicorp.com/packer/docs/plugins/install#manually-install-plugins-using-the-cli).

There is no change to the syntax or commands for installing plugins.

#### Manual installation

You can find pre-built binary releases of the plugin [here](https://github.com/MagaluCloud/packer-plugin-magalucloud/releases).
Once you have downloaded the latest archive corresponding to your target OS, uncompress it to retrieve the plugin binary file corresponding to your platform.
To install the plugin, please follow the Packer documentation on [installing a plugin](https://developer.hashicorp.com/packer/docs/plugins/install).

### From Sources

If you prefer to build the plugin from sources, clone the Git repository locally and run the command `go build` from the root directory.
Upon successful compilation, a `packer-plugin-magalucloud` plugin binary file can be found in the root directory.
To install the compiled plugin, please follow the official Packer documentation on [installing a plugin](https://developer.hashicorp.com/packer/docs/plugins/install).

### Configuration

For more information on how to configure the plugin, please read the documentation located in the [`docs/`](docs) directory.

## Contributing

We welcome contributions to the Magalu Cloud Packer plugin!

1. **Report Issues**: Found a bug or have a feature request? [Open an issue](https://github.com/MagaluCloud/packer-plugin-magalucloud/pulls)

2. **Submit PRs**: Contributions via pull requests are welcome. Please:

   - Fork the repository
   - Run `make env` to configure local environment
   - Create a feature branch
   - Make your changes
   - Run `make before-commit` to verify
   - Submit a PR

3. **Join Discussions**: Participate in our [Discussions Forum](https://github.com/MagaluCloud/packer-plugin-magalucloud/discussions)
