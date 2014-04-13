# LXC

This file will list some usefull lxc-related tools and explain there usage.

## Important locations

### Container configuration

#### Default configuration

  - /etc/lxc

The default path where the configuration files for your containers reside. If not overridden, *lxc-create* will use _'/etc/lxc/default.conf'_.


> Note: Unprivileged containers can be found at:

  - ~/.config/lxc/default.conf


#### Share

To create a container you'll need a template script, hooks,... to perform the needed actions. Most of these things can be found at:

  - /usr/share/lxc


### System configuration

  - /etc/lxc/lxc.conf


> Note: Unprivileged containers can be configured at:

  - ~/.config/lxc/lxc.conf


### Other

#### Cgroups

  - /sys/fs/cgroup

This file is home to pretty much all information regarding the cgroups assigned to a container. The actual details about a container's *memory*, *cpu* and more can be found here.


## Some usefull commands

### Create a container

> sudo lxc-create --name=container_name --template=debian-static --conf=/etc/lxc/differ_from_default.conf


#### Explanation:

  - _"--template="_: Will look inside _"/usr/share/lxc/templates"_ for a file called *"lxc-debian-static"*
  - _"--conf="_    : Accepts config file other than _"/etc/lxc/default.conf"_


### Start a container

> sudo lxc-start --name=container_name --daemon


#### Explanation:

  - _"--daemon"_: Makes sure the console does not get attached while starting the console


### List containers

> sudo lxc-ls --fancy


### Get container info

> sudo lxc-info --name=container_name


### Stop a container

> sudo lxc-stop --name=container_name


### Destroy a container

> sudo lxc-destroy --name=container_name
