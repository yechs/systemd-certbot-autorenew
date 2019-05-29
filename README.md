# systemd-certbot-autorenew
A systemd script for automatic renewal of certbot TLS certificates

**Note: this script ONLY RENEWS certificates. You need to manually initialize by obtaining your certificate through command line.**

### Usage

1. Copy `certbot.service` and `certbot.timer` to `/etc/systemd/system/`
2. Enable and start `certbot.timer`

```shell
# Copy unit files to /etc/systemd/system
sudo cp certbot.{service,timer} /etc/systemd/system

sudo systemctl daemon-reload

# Enable and start timer unit
sudo systemctl enable certbot.timer
sudo systemctl start certbot.timer
```

### Further Reading

[https://certbot.eff.org/docs/using.html](https://certbot.eff.org/docs/using.html)
