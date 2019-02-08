## Last week

I set up a custom Nerves system for Raspberry Pi called `hazel_rpi`. This is necessary because the default Nerves image doesn't include the kernel module for our Wi-Fi adapter, so I figured out how to build the image and make the necessary change to the kernel config.

Next, I set up libcluster to automatically discover other nodes on the network using a multicast gossip strategy. This right now works fine when the nodes are either running on the same host or on a network where the DNS is configured to register nodes' DHCP hostnames.

## This week

The next step is to figure out how to get the nodes to connect to each other when DNS isn't configured. I think this will involve modifying the gossip protocol to include node IP address. Nodes receiving the gossip messages can modify their `/etc/hosts` files to point the node name at the node IP, which should fix the issue.

## Blockers

None at the moment.

