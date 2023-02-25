
# Error : Process Restart request too quickly

- nano /etc/redis/redis.conf

### On Terminal
```javascript
nano /etc/systemd/system/redis.service
```

#### in service file
```javascript
Restart=no
StartLimitInterval=0
```

### On Terminal
```javascript
systemctl daemon-reload
systemctl stop redis.service
systemctl start redis.service
systemctl status redis.service
```
