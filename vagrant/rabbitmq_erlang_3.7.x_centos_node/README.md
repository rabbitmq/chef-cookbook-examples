# Single 3.7.x Node and RabbitMQ Erlang Package Example

This provisions Erlang/OTP 21.x via [zero dependency Erlang RPM](https://github.com/rabbitmq/erlang-rpm/),
RabbitMQ 3.7.x and a few commonly used plugins.
Configures kernel limits for RabbitMQ via systemd.

## How to Run It

Make sure that [Vagrant](https://www.vagrantup.com/), [Virtualbox](https://www.virtualbox.org/) and Ruby 2.x are
installed, then:

```
gem install librarian-chef
```

to install Librarian and

```
librarian-chef install
vagrant up --provision
```

to pull down the cookbook and start a Vagrant VM.

## Exposed Ports

The VM exposes [non-standard ports](https://www.rabbitmq.com/networking.html#selinux-ports) to avoid clashes with any services
that may be running locally:

 * 5692 for AMQP 0-9-1 and AMQP 1.0
 * 15692 for HTTP API and management UI
 * 1897 for MQTT
 * 61627 for STOMP
