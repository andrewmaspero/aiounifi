# Interfaces

The `Controller` exposes a number of interfaces. Each one manages a set of related objects retrieved from the API and provides helper methods. After calling `Controller.login()` these interfaces may be updated with `await interface.update()` to fetch data.

| Attribute | Description |
|-----------|-------------|
| `clients` | Current active clients. Provides `block`, `unblock`, `reconnect` and `remove_clients` methods. |
| `clients_all` | Historical clients from the controller. |
| `devices` | UniFi network devices. Supports firmware upgrades via `upgrade`. |
| `dpi_apps` | DPI restriction applications. |
| `dpi_groups` | DPI restriction groups. |
| `events` | Event history via websocket messages. |
| `firewall_policies` | Firewall policies configuration. |
| `firewall_zones` | Firewall zones configuration. |
| `outlets` | Outlet state and control. |
| `port_forwarding` | Port forwarding rules. |
| `ports` | Port configuration profiles. |
| `sites` | Sites available on the controller. |
| `system_information` | Information about the controller itself. |
| `traffic_routes` | Static routing rules. |
| `traffic_rules` | Application traffic restrictions. |
| `vouchers` | Hotspot voucher management. |
| `wlans` | Wireless network definitions. |

Each interface inherits from `APIHandler` which provides item storage, event subscription and websocket message dispatch.

