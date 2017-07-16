# Steps to build Docker For Mac 17.06.0 Community Edition


```git clone https://github.com/linuxkit/linuxkit
cd linuxkit
make
cp -rf bin/moby /usr/local/bin/
cp -rf bin/linuxkit /usr/local/bin/
```

# Using Moby Tool

```
moby build -name docker4mac base.yml docker-17.06-ce.yml
```

# Using LinuxKit

linuxkit run hyperkit -networking=vpnkit -vsock-ports=2376 -disk size=1024M docker4mac

# Containerd Commands

ctr containers ls

# Displaying Tasks

ctr tasks ls

# Entering into Docker service containers

ctr exec -t -exec-id <id> docker sh
