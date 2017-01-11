# Customized Minecraft Server
This is a minecraft server from https://travis-ci.org/stephen-mw/vagrant_minecraft with ongoing mods by JTW90210

## Running the server

Install Vagrant, change to this directory and issue ```vagrant up```. 

When you run ```vagrant destroy``` the virtualize machine is destroyed but your persistent data is kept in ```persistent_data```. 

At this point you can run ```vagrant ssh``` to go into the server. You'll be greated with a MOTD with some helpful information:

To stop, start, restart or check the status of the the minecraft server
process, simply run:

  $ service minecraft <stop|start|restart|status>

The runtime logs are available at /opt/minecraft/logs

To change the min or max server memory values, make the change in:

  /etc/init/minecraft.conf

And then restart the server proces.

Status of minecraft server:

minecraft start/running, process 2344

Have fun!
```

After the installation completes, you and others will be able to connect to your server at your _host's_ ip address. That means if you launch the vagrant instance on a laptop that has the ip address of 192.168.0.101, then you can connect to the server at the same address (regardless of what your guest ip address is).

The instance itself doesn't need to be destroyed between runs. You can also halt it. Either way, when you bring it back online it should be running the server.
