# Btrfs

In this cheat sheet, I will enlist some usefull btrfs-tools related commands.

## Issue quota on a subvolume

### 1. Enable support for quota's

> sudo btrfs quota enable <path to the subvolume>


### 2. Assign a it quota-group

> sudo btrfs qgroup limit <size[g/m/k/b/...]> <path to the subvolume>


### 3. Check the quota

> sudo btrfs qgroup show <path to the subvolume>
