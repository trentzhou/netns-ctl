# netns-ctl - Bash script to create a network namespace on linux

We know linux supports namespaces. A network namespace appears to have a 
standalone TCP/IP stack. This project provides a bash script `netns-ctl`
to simplify the work of creating and deleting a network namespace.

This project is inspired by [this page](https://schnouki.net/post/2014/openvpn-for-a-single-application-on-linux/).

## Creating a network namespace

Simply run `netns-ctl` as root, it creates a new network namespace. Features:

* There is a "lo" interface in this namespace.
* There is a virtual ethernet interface in this namespace.
* Programs in this namespace can access internet as if it's another computer.

For more options, check output of `netns-ctl -h`.

## Deleting the network namespace

Run `netns-ctl -c`.

## Launching a shell in the network namespace

Run `netns-ctl -s`.


