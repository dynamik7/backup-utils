GitHub Enterprise Backup Utilities
==================================

This repository includes utilities for and documentation on running a
[GitHub Enterprise](https://enterprise.github.com) backup / DR site.

### Setup for server based backups

Follow these instructions to configure a new backup site:

 1. `git clone https://github.com/github/enterprise-backup-site.git ghe-backup`
 2. Copy the `backup.config-example` file to `backup.config` and modify as needed.
 3. Add the local user's ssh key to the GitHub Enterprise instance's authorized keys.
    See [Adding an SSH key for shell access](https://enterprise.github.com/help/articles/adding-an-ssh-key-for-shell-access)
    for instructions.
 4. Run `scripts/ghe-host-check` to verify connectivity with the GitHub Enterprise instance.

### Setup for S3 based backups

Follow these instructions to configure S3 backups:

 1. Perform the above steps to setup a backup site
 2. Install s3cmd
   * OSX: `brew install s3cmd`
   * Ubuntu: `apt-get install s3cmd`
 4. Run `scripts/ghe-s3-backup-all`

### See Also

The scripts in this repository build on the documentation provided in the
GitHub Enterprise help site. See the following more information:

 - [Backing up GitHub Enterprise data](https://enterprise.github.com/help/articles/backing-up-enterprise-data)
 - [Restoring GitHub Enterprise data](https://enterprise.github.com/help/articles/restoring-enterprise-data)
