# Single 3.6.16 Node Example

This provisions Erlang/OTP 20.x, RabbitMQ 3.6.16 and a few commonly
used plugins. Configures kernel limits for RabbitMQ via systemd.

Note that **RabbitMQ 3.6.x has been out of support** since May 2018.

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

 * 5686 for AMQP 0-9-1 and AMQP 1.0
 * 15686 for HTTP API and management UI
 * 1896 for MQTT
 * 61626 for STOMP
