# README

This is my code after following (more or less) the [Hotrails tutorial](https://www.hotrails.dev/). I didn't finish all the chapters, but I think I got to Chapter 4, at least. I didn't bother with the CSS styling much, either. So the pages aren't very pretty.

To run in a virtualized or containerized environment where the browser is outside the container:

```
bin/dev -b 0.0.0.0
```

Leave off the `-b 0.0.0.0` for other environments.

There's support in this project to run in a Docker container. I use plain Docker, not Docker Desktop, on Linux.

To start, run:

```
docker compose up -d
```

To run the server:

```
docker compose exec web bin/dev -b 0.0.0.0
```

The port mapping uses Docker ephemeral ports. To find the port you can browse to:

```
docker compose port web 3000 | cut -d: -f 2
```

Browse to `localhost:<port number from above>`.
