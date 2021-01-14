### GENERAL
List, status, show
````
pm2 list                        # display all processes status
pm2 jlist                       # print process list in raw JSON
pm2 prettylist                  # print process list in beautified JSON
pm2 describe <pid>              # display all information about a specific process
pm2 monit                       # monitor all processes
pm2 status                      # Shows status
pm2 show <id>                   # Shows details of a given process by id
````
### Logs
````
pm2 logs [--raw]                # display all processes logs in streaming
pm2 flush                       # empty all log files
pm2 reloadLogs                  # reload all logs
````
### Start “Fork mode”
````
pm2 start app.js --name MyApp
````
### Start “Cluster Mode”
````
pm2 start app.js -i 0
````
### Start process file
````
pm2 start ecosystem.json                    # start all applications
pm2 start ecosystem.json --only worker-app  # start only the app named worker-app
pm2 stop ecosystem.json                     # stop all
pm2 start ecosystem.json                    # restart all
pm2 restart ecosystem.json                  # restart all
pm2 reload ecosystem.json                   # reload all
pm2 delete ecosystem.json                   # delete all
````

### Example process file (json)
````
{
    "apps" : [
        {
            "name"        : "worker",
            "script"      : "./worker.js",
            "watch"       : true,
            "env": {
                "NODE_ENV": "development"
            },
            "env_production" : {
                "NODE_ENV": "production"
            }
        },{
            "name"       : "api-app",
            "script"     : "./api.js",
            "instances"  : 4,
            "exec_mode"  : "cluster"
        }
    ]
}
````

### Options
````
-h, --help                           # output usage information
-V, --version                        # output the version number
-v --version                         # get version
-s --silent                          # hide all messages
-m --mini-list                       # display a compacted list without formatting
-f --force                           # force actions
-n --name <name>                     # set a <name> for script
-i --instances <number>              # launch [number]instances (for networked app)(load balanced)
-l --log [path]                      # specify entire log file (error and out are both included)
-o --output <path>                   # specify out log file
-e --error <path>                    # specify error log file
-p --pid <pid>                       # specify pid file
--max-memory-restart <memory>        # specify max memory amount used to autorestart (in megaoctets)
--env <environment_name>             # specify environment to get specific env variables (for JSON declaration)
-x --execute-command                 # execute a program using fork system
-u --user <username>                 # define user when generating startup script
-c --cron <cron_pattern>             # restart a running process based on a cron pattern
-w --write                           # write configuration in local folder
--interpreter <interpreter>          # the interpreter pm2 should use for executing app (bash, python...)
--log-date-format <momentjs format>  # add custom prefix timestamp to logs
--no-daemon                          # run pm2 daemon in the foreground if it doesn't exist already
--merge-logs                         # merge logs from different instances but keep error and out separated
--watch                              # watch application folder for changes
--ignore-watch <folders|files>       # folder/files to be ignored watching, chould be a specific name or regex - e.g. --ignore-watch="test node_modules "some scripts""
--node-args <node_args>              # space delimited arguments to pass to node in cluster mode - e.g. --node-args="--debug=7001 --trace-deprecation"
--no-color                           # skip colors
--no-vizion                          # skip vizion features (versioning control)
--no-autorestart                     # do not automatically restart apps
````
