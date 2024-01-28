# Hello Docker LAMP

Docker Compose that setups a LAMP Stack.

## Docker Compose [PKB](https://en.wikipedia.org/wiki/Personal_knowledge_base)

- Restart: Specifies a restart policy:
  - `no`: Default value. The container won't be restarted.
  - `always`: The service will be restarted every time it is stopped, even if
    you stops it.
  - `unless-stopped`: Same as `always` but it will remain stopped if you stops
    it.
  - `on-failure[:times]`: The container will be restarted if it fails.
    Optionally you can specify how many attempts until be considered a failure service.

  ```yml
  restart:
    - on-failure:5
  ```

- Ports: Binds specific posts between real host and docker.

  ```yml
  ports:
    - <host-port>:<docker-port>
  ```

- Volumes: Links a folder from working dir to the service target folder. The
  working dir folder will be create if doesn't exists.

  ```yml
  volumes:
    - <working-dir-folder>:<target-dir>
  ```