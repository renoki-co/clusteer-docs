# ✨ Starting the server

For Laravel installation, you may run the server with the already registered `clusteer:serve` command:

```bash
php artisan clusteer:serve --help
```

**The --help parameter will give you a list of parameters you can pass. By default, it will run the server with the default configuration that exists in the config folder.**

### Vanilla PHP

If you use plain PHP, you can create your script that will run the server with ReactPHP [like in this command file](https://github.com/renoki-co/clusteer/blob/master/src/Console/Commands/ServeClusteer.php#L52-L95).

### Run with Supervisor

It's recommended to run the server with Supervisor or another process manager. However, make sure that in case of any interruption, the node process may still be running, blocking the allocated port.

In the Supervisor configuration, make sure to add `killasgroup` and `stopasgroup` as described below:

```
[program:clusteer]
process_name=%(program_name)s_%(process_num)02d
command=php artisan clusteer:serve
directory=/path/to/your/project
autostart=true
autorestart=true
killasgroup=true
stopasgroup=true
numprocs=1
redirect_stderr=true
stdout_logfile=/dev/null
```
