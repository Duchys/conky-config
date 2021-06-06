# conky-config
Customized conky configuration for showing AMD GPU usage, CPU Usage, Memory Usage, Top processes, Disk usage, Networking details and uptime

This configuration is based upon umaraziz0's conky configuration https://github.com/umaraziz0/conky-conf

![example.png](https://raw.githubusercontent.com/duchys/conky-config/main/example.png)

# Dependencies
radeontop

# Installation
cd /tmp
git clone https://github.com/Duchys/conky-config.git
cd conky-config
mkdir -p ~/.config/conky/duchys
cp conky.conf ~/.config/conky/duchys/.

# Post Installation
rm -rf /tmp/conky-config

# Initial startup
conky -m 0 -c ~/.config/conky/duchys/conky.conf # This starts Conky on first monitor
conky -m 1 -c ~/.config/conky/duchys/conky.conf # This starts Conky on secondary monitor

# Command to use for automatic startup (firstly you have to set the automatic startup process, based on your DE)
# The 10 second sleep is used to wait for your desktop to be already set up
sh -c 'sleep 10 && conky --daemonize --pause=1 -m 1 -c ~/.config/conky/umaraziz/conky.conf'
