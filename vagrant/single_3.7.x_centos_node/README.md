# Single 3.7.x Node Example

This provisions Erlang/OTP 20.x, RabbitMQ 3.7.x and a few commonly
used plugins. Configures kernel limits for RabbitMQ via systemd.

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

 * 5682 for AMQP 0-9-1 and AMQP 1.0
 * 15682 for HTTP API and management UI
 * 1893 for MQTT
 * 61623 for STOMP
