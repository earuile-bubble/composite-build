# Composite build

## User guide

### Open project
1. Clone [composite-build](https://github.com/earuile-bubble/composite-build), [server](https://github.com/earuile-bubble/bubble-server) and [client](https://github.com/earuile-bubble/bubble-client) repositories to same directory.
2. Open `composite-build` in IDEA as gradle project.
3. Wait until gradle finished loading
4. Now you should see 3 modules in project explorer: `composite-build`, `bubble-server[server]` and `desktop[client-desktop]`:

![project-explorer-composite-build](https://github.com/earuile-bubble/composite-build/assets/89979817/a1d887d0-178f-4f20-83b1-c103e5680ad7)

### Git
For better git UI experience, go to `Settings`->`Version Control`->`Directory Mappings` and using `+`/`-` buttons configure it so all 3 directories are git roots:![git-config-composite-build](https://github.com/earuile-bubble/composite-build/assets/89979817/b085ebfd-db15-4efa-b034-9a57c9ecbdfe)

Then, open git commit pane and in `View Options` select `Group By`->`Repository`:![git-group-by-composite-build](https://github.com/earuile-bubble/composite-build/assets/89979817/f8e3acdc-8bd4-4f40-833a-f607d8f621cf)

### Build&Run
There are 4 predefined configurations: 
1. ServerDocker - runs `docker-compose` defined in server repository
2. RunServer - runs server as a `Spring Boot` application. *Also runs ServerDocker configuration before, so it is not necessary to run docker separately*
3. RunClientLocal - runs client that will connect to server on `localhost:8082`, so it is suitable when you run `RunServer` config in parallel
4. RunClientRemote - runs client that will connect to server on address defined in [application.yml](https://github.com/earuile-bubble/bubble-client/blob/master/desktop/src/main/resources/application.yml)
