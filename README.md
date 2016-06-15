ABOUT
=====

  socat-multi-init is a LSB init tool to manage multiple socat relays
  See http://www.dest-unreach.org/socat/doc/socat.html

INSTALLATION
============

  Install files to their required locations:

        git clone https://github.com/isaacchapman/socat-multi-init.git
        cd socat-multi-init
        sudo cp -a etc/init.d/socat /etc/init.d/
        sudo cp -a etc/default/socat /etc/default/
        sudo mkdir -p /etc/socat/conf.d
        sudo cp -a etc/socat/conf.d/* /etc/socat/conf.d/

CONFIGURATION
=============

  ``$SOCAT_OPTS`` defined in ``/etc/default/socat`` override the default flags that
  are provided to each socat relay created.

  Each line in a ``/etc/socat/conf.d/*.conf`` file will setup a separate socat relay.
  Additional flags besides those provided by ``$SOCAT_OPTS`` can be included.

  See [socat examples](http://www.dest-unreach.org/socat/doc/socat.html#EXAMPLES) for example usage.

Inspired by https://github.com/asaif/socat-init
