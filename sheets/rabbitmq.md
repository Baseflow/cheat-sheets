## Installing the RabbitMQ Server on your Mac

The easiest way to install the RabbitMQ server on your Mac is by using Homebrew (if don't have Homebrew installed you can follow these [instructions](https://docs.brew.sh/Installation)). You can install RabbitMQ using the following commands:

```
# Update taps and Homebrew
brew update

# Install RabbitMQ serve
brew install rabbitmq
```

If you would like to have the RabbitMQ daemon started automatically when you restart your machine use the following command:

```
# Make sure RabbitMQ is started as background service
brew services start rabbitmq
``` 

If you'd prefer to start RabbitMQ server manually you can type the command:

```
# Starts the RabbitMQ server manually
rabbitmq-server
```

> NOTE: if the `rabbitmq-server` command doesn't work you probably need to add the RabbitMQ installation directory to your path. To do so type the following command: `export PATH=$PATH:/usr/local/opt/rabbitmq/sbin`.

> NOTE 2: by default the `rabbitmq` Homebrew formula also installs the RabbitMQ Management portal which you can access (once the `rabbitmq-server` is running) at http://localhost:15672/. The default credentials are:
> - username: guest
> - password: guest

## Useful links

- RabbitMQ documentation: https://www.rabbitmq.com/documentation.html
