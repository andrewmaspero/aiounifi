# Command Line Interface

The library ships with a small CLI that exposes many of the same operations used internally. After installation a command called `aiounifi` is available.

Run `aiounifi --help` to see the available arguments:

```text
usage: aiounifi [-h] [-p PORT] [-s SITE] [-D] host username password
```

Example connecting to a controller:

```bash
aiounifi 192.168.1.10 ubnt password -s default
```

The CLI logs in, fetches several resources in parallel and then starts a websocket connection which outputs raw websocket messages to STDOUT until interrupted.

