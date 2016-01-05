# Docker

## Tips

Inspect changes on a container's filesystem.

```
$ docker diff [container]
```

```
$ docker diff php
```

---

Run a command in a running container.

```
$ docker exec [container] [command]
```

```
$ docker exec php bash
```

---

Fetch the logs of a container.

```
$ docker logs [container]
```

```
$ docker logs php
```

Follow log output.

```
$ docker logs -f php
```

---

Display container(s) statistics.

```
$ docker stats [container...]
```

```
$ docker stats php mysql
```

---

Display the running processes of a container.

```
$ docker top [container] [ps options]
```

```
$ docker top php
```

