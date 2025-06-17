# Getting Started

Install the library from PyPI or install this repository in editable mode when developing locally.

```bash
pip install aiounifi
```

The main entry point is the `Controller` class. It requires a `Configuration` instance containing an `aiohttp` session and connection parameters.

```python
import aiohttp
from aiounifi.controller import Controller
from aiounifi.models.configuration import Configuration

async def main() -> None:
    session = aiohttp.ClientSession(cookie_jar=aiohttp.CookieJar(unsafe=True))
    config = Configuration(
        session=session,
        host="192.168.1.10",
        username="ubnt",
        password="password",
        port=8443,
        site="default",
        ssl_context=False,
    )
    controller = Controller(config)
    await controller.login()

    # fetch initial device state
    await controller.devices.update()
    for mac, device in controller.devices.items():
        print(device.name, mac)

    await controller.start_websocket()
```

