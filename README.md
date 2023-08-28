# Sensible Airgapped

Shell script that combines various sensible configurations into one script so that it can more easily be accessible in an air-gapped machine.

As we know, in an air-gapped machine, usually we cannot connect to github.com directly to clone the repository, and generally moving multiple files to and from it is a hassle.

Some professions also provision and destroy air-gapped machines all the time and personal configurations need to be redone every time we do so.

[`sensible.airgapped`](./sensible.airgapped) attempts to combine sensible configurations into one script. We then use the host machine's clipboard to pass the script to the airgapped machine (usually accessed with SSH).

# Installation

1. Copy the contents of [`sensible.airgapped`](./sensible.airgapped)
2. In the airgapped machine, create a new file and paste the contents into it
   ```bash
   vim ~/.sensible.airgapped
   ```
3. Make it executable and execute it
   ```bash
   chmod u+x sensible.airgapped
   ~/.sensible.airgapped
   ```

# What it does

- Create a `~/.vimrc` based on [vim-sensible](https://github.com/tpope/vim-sensible) (Last updated: August 28, 2023)
