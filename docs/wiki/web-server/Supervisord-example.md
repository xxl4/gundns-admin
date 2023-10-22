Following is an example showing how to run PowerDNS-Admin with supervisord

Create supervisord program config file
```
$ sudo vim /etc/supervisor.d/gundnsadmin.conf
```

```
[program:gundnsadmin]
command=/opt/web/powerdns-admin/flask/bin/python ./run.py
stdout_logfile=/var/log/supervisor/program_gundnsadmin.log
stderr_logfile=/var/log/supervisor/program_gundnsadmin.error
autostart=true
autorestart=true
directory=/opt/web/powerdns-admin
```

Then `sudo supervisorctl start gundnsadmin` to start the Powerdns-Admin service.