# Chef RabbitMQ Cookbook Examples

This repository contains examples that demonstrate
how various node attributes are used and can serve as
a starting point or a scratchpad for experimentation.

The examples currently use [Vagrant](https://github.com/applicationsonline/librarian-chef) and `chef-solo` for provisioning.
Librarian is used for dependency management.

## Available Examples

 * [Single 3.7.x node with plugins](./vagrant/single_3.7.x_node): provisions Erlang/OTP 20.x, RabbitMQ 3.7.x and a few commonly
   used plugins. Configures kernel limits for RabbitMQ via systemd.
 * [Single 3.7.x node on CentOS 7](./vagrant/single_3.7.x_centos_node): same as above but uses CentOS 7.x instead
   of Ubuntu.


## Dependencies

Make sure that [Vagrant](https://www.vagrantup.com/), [Virtualbox](https://www.virtualbox.org/) and Ruby 2.x are
installed, then install Librarian:

```
gem install librarian-chef
```

and cookbook dependencies (from the example directory):

```
librarian-chef install
```

then use Vagrant as usual.


## License and Copyright

See [LICENSE](./LICENSE).

2018 (c) Pivotal Software, Inc.
