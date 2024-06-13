# Labo03 - Run a first container

## Pedagogical intent

In this lab, you'll:

* Get to grips with the first Docker commands,
* Run your first Docker
* Familiarize yourself with port publishing

---

Note: the docker engine must be running

## Task 01 - Get to grips with the first Docker commands

* List all images present on your installation

[INPUT]
```bash
docker images
```

[OUTPUT]
```bash
REPOSITORY                 TAG                IMAGE ID       CREATED         SIZE
supabase/studio            20240301-0942bfe   59143d989fda   2 months ago    693MB
supabase/edge-runtime      v1.38.0            dbdc661a4f84   2 months ago    270MB
supabase/realtime          v2.25.66           a3791a36ff98   2 months ago    182MB
supabase/postgres-meta     v0.79.0            ebb35524ef78   2 months ago    338MB
supabase/gotrue            v2.143.0           72e6beabb340   2 months ago    40MB
supabase/storage-api       v0.46.4            fb99faca5dbe   3 months ago    180MB
postgrest/postgrest        v12.0.1            988950c493af   5 months ago    319MB
supabase/postgres          15.1.0.147         d0e122868acd   5 months ago    1.16GB
docker/welcome-to-docker   latest             648f93a1ba7d   6 months ago    19MB
supabase/logflare          1.4.0              0b971a10611d   9 months ago    431MB
timberio/vector            0.28.1-alpine      e1dceaa760d2   14 months ago   111MB
kong                       2.8.1              a5957d67fc55   18 months ago   149MB
darthsim/imgproxy          v3.8.0             696a5c233e29   19 months ago   162MB
```

* Get the official Nginx image using this command

[INPUT]
```bash
docker pull nginx
```

[OUTPUT]
```
Using default tag: latest
latest: Pulling from library/nginx
24c63b8dcb66: Pull complete 
ac894f1d1dfb: Pull complete 
2572d4eb2260: Pull complete 
0ac3805c647c: Pull complete 
da20f09652a8: Pull complete 
2de21a3abd85: Pull complete 
77cea143f3c3: Pull complete 
Digest: sha256:a484819eb60211f5299034ac80f6a681b06f89e65866ce91f356ed7c72af059c
Status: Downloaded newer image for nginx:latest
docker.io/library/nginx:latest

What's Next?
  1. Sign in to your Docker account → docker login
  2. View a summary of image vulnerabilities and recommendations → docker scout quickview nginx
```

Note : do you see the different layer uploaded ?

* List -again- all image present on your installation

[INPUT]
```bash
docker images
```

[OUTPUT]
```
REPOSITORY                 TAG                IMAGE ID       CREATED         SIZE
nginx                      latest             8dd77ef2d82e   12 days ago     193MB
supabase/studio            20240301-0942bfe   59143d989fda   2 months ago    693MB
supabase/edge-runtime      v1.38.0            dbdc661a4f84   2 months ago    270MB
supabase/realtime          v2.25.66           a3791a36ff98   2 months ago    182MB
supabase/postgres-meta     v0.79.0            ebb35524ef78   2 months ago    338MB
supabase/gotrue            v2.143.0           72e6beabb340   2 months ago    40MB
supabase/storage-api       v0.46.4            fb99faca5dbe   3 months ago    180MB
postgrest/postgrest        v12.0.1            988950c493af   5 months ago    319MB
supabase/postgres          15.1.0.147         d0e122868acd   5 months ago    1.16GB
docker/welcome-to-docker   latest             648f93a1ba7d   6 months ago    19MB
supabase/logflare          1.4.0              0b971a10611d   9 months ago    431MB
timberio/vector            0.28.1-alpine      e1dceaa760d2   14 months ago   111MB
kong                       2.8.1              a5957d67fc55   18 months ago   149MB
darthsim/imgproxy          v3.8.0             696a5c233e29   19 months ago   162MB
```

Note : 188 MB is the size of your image... check it.

* List -again- all image present on your installation

[INPUT]
```bash
docker images
```

[OUTPUT]
```
REPOSITORY                 TAG                IMAGE ID       CREATED         SIZE
nginx                      latest             8dd77ef2d82e   12 days ago     193MB
supabase/studio            20240301-0942bfe   59143d989fda   2 months ago    693MB
supabase/edge-runtime      v1.38.0            dbdc661a4f84   2 months ago    270MB
supabase/realtime          v2.25.66           a3791a36ff98   2 months ago    182MB
supabase/postgres-meta     v0.79.0            ebb35524ef78   2 months ago    338MB
supabase/gotrue            v2.143.0           72e6beabb340   2 months ago    40MB
supabase/storage-api       v0.46.4            fb99faca5dbe   3 months ago    180MB
postgrest/postgrest        v12.0.1            988950c493af   5 months ago    319MB
supabase/postgres          15.1.0.147         d0e122868acd   5 months ago    1.16GB
docker/welcome-to-docker   latest             648f93a1ba7d   6 months ago    19MB
supabase/logflare          1.4.0              0b971a10611d   9 months ago    431MB
timberio/vector            0.28.1-alpine      e1dceaa760d2   14 months ago   111MB
kong                       2.8.1              a5957d67fc55   18 months ago   149MB
darthsim/imgproxy          v3.8.0             696a5c233e29   19 months ago   162MB
```

* List all Docker

[INPUT]
```bash
docker ps -a
```

[OUTPUT]
```
CONTAINER ID   IMAGE                              COMMAND                   CREATED          STATUS                      PORTS     NAMES
a86fec753e91   docker/welcome-to-docker:latest    "/docker-entrypoint.…"    15 minutes ago   Exited (0) 13 minutes ago             peaceful_wozniak
56406f327e57   supabase/storage-api:v0.46.4       "docker-entrypoint.s…"    2 months ago     Exited (0) 7 weeks ago                supabase-storage
657f32f34c44   supabase/studio:20240301-0942bfe   "docker-entrypoint.s…"    2 months ago     Exited (0) 7 weeks ago                supabase-studio
cbeb733efe36   postgrest/postgrest:v12.0.1        "postgrest"               2 months ago     Exited (255) 7 weeks ago              supabase-rest
1249034f0141   supabase/edge-runtime:v1.38.0      "edge-runtime start …"    2 months ago     Exited (137) 7 weeks ago              supabase-edge-functions
817ee1c94cd9   supabase/gotrue:v2.143.0           "auth"                    2 months ago     Exited (0) 7 weeks ago                supabase-auth
c0f241b83b61   supabase/realtime:v2.25.66         "/usr/bin/tini -s -g…"    2 months ago     Exited (143) 7 weeks ago              realtime-dev.supabase-realtime
34d1c39f8a5a   kong:2.8.1                         "bash -c 'eval \"echo…"   2 months ago     Exited (0) 7 weeks ago                supabase-kong
00007eb28455   supabase/postgres-meta:v0.79.0     "docker-entrypoint.s…"    2 months ago     Exited (0) 7 weeks ago                supabase-meta
ecaa5d711842   supabase/logflare:1.4.0            "sh run.sh"               2 months ago     Exited (137) 7 weeks ago              supabase-analytics
38ed33e4f69e   supabase/postgres:15.1.0.147       "docker-entrypoint.s…"    2 months ago     Exited (0) 7 weeks ago                supabase-db
592a4a78bebe   timberio/vector:0.28.1-alpine      "/usr/local/bin/vect…"    2 months ago     Exited (137) 7 weeks ago              supabase-vector
a22854072ddb   darthsim/imgproxy:v3.8.0           "imgproxy"                2 months ago     Exited (0) 7 weeks ago                supabase-imgproxy
```

## Task 02 - Run the container

* Run Nginx Docker

[INPUT]
```bash
docker run nginx
```

[OUTPUT]
```
docker run nginx
/docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration
/docker-entrypoint.sh: Looking for shell scripts in /docker-entrypoint.d/
/docker-entrypoint.sh: Launching /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh
10-listen-on-ipv6-by-default.sh: info: Getting the checksum of /etc/nginx/conf.d/default.conf
10-listen-on-ipv6-by-default.sh: info: Enabled listen on IPv6 in /etc/nginx/conf.d/default.conf
/docker-entrypoint.sh: Sourcing /docker-entrypoint.d/15-local-resolvers.envsh
/docker-entrypoint.sh: Launching /docker-entrypoint.d/20-envsubst-on-templates.sh
/docker-entrypoint.sh: Launching /docker-entrypoint.d/30-tune-worker-processes.sh
/docker-entrypoint.sh: Configuration complete; ready for start up
2024/05/16 06:40:25 [notice] 1#1: using the "epoll" event method
2024/05/16 06:40:25 [notice] 1#1: nginx/1.25.5
2024/05/16 06:40:25 [notice] 1#1: built by gcc 12.2.0 (Debian 12.2.0-14) 
2024/05/16 06:40:25 [notice] 1#1: OS: Linux 6.6.12-linuxkit
2024/05/16 06:40:25 [notice] 1#1: getrlimit(RLIMIT_NOFILE): 1048576:1048576
2024/05/16 06:40:25 [notice] 1#1: start worker processes
2024/05/16 06:40:25 [notice] 1#1: start worker process 29
2024/05/16 06:40:25 [notice] 1#1: start worker process 30
2024/05/16 06:40:25 [notice] 1#1: start worker process 31
2024/05/16 06:40:25 [notice] 1#1: start worker process 32
2024/05/16 06:40:25 [notice] 1#1: start worker process 33
2024/05/16 06:40:25 [notice] 1#1: start worker process 34
2024/05/16 06:40:25 [notice] 1#1: start worker process 35
2024/05/16 06:40:25 [notice] 1#1: start worker process 36
2024/05/16 06:40:25 [notice] 1#1: start worker process 37
2024/05/16 06:40:25 [notice] 1#1: start worker process 38
```

* Can you reach the default page of nginx

Note : By default, Nginx is listening on port 80

[INPUT]
```bash
curl localhost
```

[OUTPUT]
```
curl: (7) Failed to connect to localhost port 80 after 0 ms: Couldn't connect to server
```

* Stop this first attempt

[INPUT]
```
docker stop <id>
```

[OUTPUT]
```
^C2024/05/16 06:42:17 [notice] 1#1: signal 2 (SIGINT) received, exiting
2024/05/16 06:42:17 [notice] 29#29: exiting
2024/05/16 06:42:17 [notice] 30#30: exiting
2024/05/16 06:42:17 [notice] 31#31: exiting
2024/05/16 06:42:17 [notice] 32#32: exiting
2024/05/16 06:42:17 [notice] 30#30: exit
2024/05/16 06:42:17 [notice] 29#29: exit
2024/05/16 06:42:17 [notice] 32#32: exit
2024/05/16 06:42:17 [notice] 31#31: exit
2024/05/16 06:42:17 [notice] 34#34: exiting
2024/05/16 06:42:17 [notice] 34#34: exit
2024/05/16 06:42:17 [notice] 36#36: exiting
2024/05/16 06:42:17 [notice] 36#36: exit
2024/05/16 06:42:17 [notice] 35#35: exiting
2024/05/16 06:42:17 [notice] 35#35: exit
2024/05/16 06:42:17 [notice] 37#37: exiting
2024/05/16 06:42:17 [notice] 33#33: exiting
2024/05/16 06:42:17 [notice] 38#38: exiting
2024/05/16 06:42:17 [notice] 37#37: exit
2024/05/16 06:42:17 [notice] 33#33: exit
2024/05/16 06:42:17 [notice] 38#38: exit
2024/05/16 06:42:17 [notice] 1#1: signal 17 (SIGCHLD) received from 32
2024/05/16 06:42:17 [notice] 1#1: worker process 32 exited with code 0
2024/05/16 06:42:17 [notice] 1#1: signal 29 (SIGIO) received
2024/05/16 06:42:17 [notice] 1#1: signal 17 (SIGCHLD) received from 29
2024/05/16 06:42:17 [notice] 1#1: worker process 29 exited with code 0
2024/05/16 06:42:17 [notice] 1#1: worker process 31 exited with code 0
2024/05/16 06:42:17 [notice] 1#1: worker process 35 exited with code 0
2024/05/16 06:42:17 [notice] 1#1: signal 29 (SIGIO) received
2024/05/16 06:42:17 [notice] 1#1: signal 17 (SIGCHLD) received from 36
2024/05/16 06:42:17 [notice] 1#1: worker process 30 exited with code 0
2024/05/16 06:42:17 [notice] 1#1: worker process 36 exited with code 0
2024/05/16 06:42:17 [notice] 1#1: signal 29 (SIGIO) received
2024/05/16 06:42:17 [notice] 1#1: signal 17 (SIGCHLD) received from 30
2024/05/16 06:42:17 [notice] 1#1: worker process 37 exited with code 0
2024/05/16 06:42:17 [notice] 1#1: signal 29 (SIGIO) received
2024/05/16 06:42:17 [notice] 1#1: signal 17 (SIGCHLD) received from 34
2024/05/16 06:42:17 [notice] 1#1: worker process 34 exited with code 0
2024/05/16 06:42:17 [notice] 1#1: worker process 38 exited with code 0
2024/05/16 06:42:17 [notice] 1#1: signal 29 (SIGIO) received
2024/05/16 06:42:17 [notice] 1#1: signal 17 (SIGCHLD) received from 38
2024/05/16 06:42:17 [notice] 1#1: signal 17 (SIGCHLD) received from 33
2024/05/16 06:42:17 [notice] 1#1: worker process 33 exited with code 0
2024/05/16 06:42:17 [notice] 1#1: exit
```

## Task 03 - Familiarize yourself with port publishing

* Make it possible to reach nginx with this command

[Publish a port](https://docs.docker.com/network/#published-ports)

[INPUT]
```
curl localhost:8080
```

[OUTPUT]
```html
<!DOCTYPE html>
<html>
<head>
    <title>Welcome to nginx!</title>
    <style>
        html {
            color-scheme: light dark;
        }

        body {
            width: 35em;
            margin: 0 auto;
            font-family: Tahoma, Verdana, Arial, sans-serif;
        }
    </style>
</head>
<body>
<h1>Welcome to nginx!</h1>
<p>If you see this page, the nginx web server is successfully installed and
    working. Further configuration is required.</p>

<p>For online documentation and support please refer to
    <a href="http://nginx.org/">nginx.org</a>.<br/>
    Commercial support is available at
    <a href="http://nginx.com/">nginx.com</a>.</p>

<p><em>Thank you for using nginx.</em></p>
</body>
</html>
```

* Stop and delete the container

[INPUT]
```
docker rm 999ddb269e3
```

[OUTPUT]
```
999ddb269e3c
```

* Delete the image

[INPUT]
```
docker image rm ba5f9d86724c
```

[OUTPUT]
```
Deleted: sha256:ba5f9d86724cd93f804e6ac7b298e9e78e281af35887b5ddf17523d39d14122f
```
