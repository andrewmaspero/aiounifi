# Data Models

This page documents each model class and the properties available on them.
Descriptions are extracted from source code docstrings.

## Client

| Property | Description |
|----------|-------------|
| `access_point_mac` | MAC address of access point. |
| `association_time` | When was client associated with controller. |
| `blocked` | Is client blocked. |
| `device_name` | Device name of client. |
| `essid` | ESSID client is connected to. |
| `firmware_version` | Firmware version of client. |
| `first_seen` | When was client first seen. |
| `fixed_ip` | List IP if fixed IP is configured. |
| `hostname` | Hostname of client. |
| `idle_time` | Idle time of client. |
| `ip` | IP of client. |
| `is_guest` | Is client guest. |
| `is_wired` | Is client wired. |
| `last_seen` | When was client last seen. |
| `last_seen_by_access_point` | When was client last seen by access point. |
| `last_seen_by_gateway` | When was client last seen by gateway. |
| `last_seen_by_switch` | When was client last seen by network switch. |
| `latest_association_time` | When was client last associated with controller. |
| `mac` | MAC address of client. |
| `name` | Name of client. |
| `oui` | Vendor string for client MAC. |
| `powersave_enabled` | Powersave functionality enabled for wireless client. |
| `site_id` | Site ID client belongs to. |
| `switch_depth` | How many layers of switches client is in. |
| `switch_mac` | MAC for switch client is connected to. |
| `switch_port` | Switch port client is connected to. |
| `rx_bytes` | Bytes received over wireless connection. |
| `rx_bytes_r` | Bytes recently received over wireless connection. |
| `tx_bytes` | Bytes transferred over wireless connection. |
| `tx_bytes_r` | Bytes recently transferred over wireless connection. |
| `uptime` | Uptime of client. |
| `uptime_by_access_point` | Uptime of client observed by access point. |
| `uptime_by_gateway` | Uptime of client observed by gateway. |
| `uptime_by_switch` | Uptime of client observed by network switch. |
| `wired_rate_mbps` | Wired rate in Mbps. |
| `wired_rx_bytes` | Bytes received over wired connection. |
| `wired_rx_bytes_r` | Bytes recently received over wired connection. |
| `wired_tx_bytes` | Bytes transferred over wired connection. |
| `wired_tx_bytes_r` | Bytes recently transferred over wired connection. |

```python
# Accessing Client properties
client = ...  # obtain from Controller interface
print(client.access_point_mac)
```

## Configuration

| Property | Description |
|----------|-------------|
| `url` | Represent console path. |

```python
# Accessing Configuration properties
config = Configuration(session, "host")
print(config.url)
```

## Device

| Property | Description |
|----------|-------------|
| `board_revision` | Board revision of device. |
| `considered_lost_at` | When device is considered lost. |
| `disabled` | Is device disabled. |
| `downlink_table` | All devices with device as uplink. |
| `fan_level` | Fan level of device. |
| `general_temperature` | General temperature of device. |
| `has_fan` | Do device have a fan. |
| `has_temperature` | Do the device have a general temperature. |
| `hw_caps` | Hardware capabilities. |
| `id` | ID of device. |
| `ip` | IP of device. |
| `last_seen` | When was device last seen. |
| `led_override` | LED override. |
| `led_override_color` | LED override color. |
| `led_override_color_brightness` | LED override color brightness. |
| `lldp_table` | All clients and devices directly attached to device. |
| `mac` | MAC address of device. |
| `model` | Model of device. |
| `name` | Name of device. |
| `next_heartbeat_at` | Next heart beat full UNIX time. |
| `next_interval` | Next heart beat in seconds. |
| `overheating` | Is device overheating. |
| `outlet_overrides` | Overridden outlet configuration. |
| `outlet_ac_power_budget` | The amount of power available to outlets. |
| `outlet_ac_power_consumption` | The amount of power consumed by all outlets. |
| `outlet_table` | List of outlets. |
| `port_overrides` | Overridden port configuration. |
| `port_table` | List of ports and data. |
| `speedtest_status` | Speedtest status. |
| `state` | State of device. |
| `storage` | Device storage information. |
| `sys_stats` | Output from top. |
| `system_stats` | System statistics. |
| `temperatures` | Device temperature sensors. |
| `type` | Type of device. |
| `version` | Firmware version. |
| `upgradable` | Is a new firmware available. |
| `upgrade_to_firmware` | Firmware version to update to. |
| `uplink` | Information about uplink. |
| `uplink_depth` | Hops to gateway. |
| `uptime` | Uptime of device. |
| `uptime_stats` | Uptime statistics. |
| `user_num_sta` | Amount of connected clients. |
| `wlan_overrides` | Wlan configuration override. |
| `supports_led_ring` | Check if the hardware supports an LED ring based on the second bit of `hw_caps`. |

```python
# Accessing Device properties
device = ...  # obtain from Controller interface
print(device.board_revision)
```

## DPIRestrictionApp

| Property | Description |
|----------|-------------|
| `id` | DPI app ID. |
| `apps` | List of apps. |
| `blocked` | Is blocked. |
| `cats` | Categories. |
| `enabled` | Is enabled. |
| `log` | Is logging enabled. |
| `site_id` | Site ID. |

```python
# Accessing DPIRestrictionApp properties
dpirestrictionapp = ...  # obtain from Controller interface
print(dpirestrictionapp.id)
```

## DPIRestrictionGroup

| Property | Description |
|----------|-------------|
| `id` | DPI group ID. |
| `attr_no_delete` | Can be deleted. |
| `attr_hidden_id` | Attr hidden ID. |
| `name` | DPI group name. |
| `site_id` | Site ID. |
| `dpiapp_ids` | DPI app IDs belonging to group. |

```python
# Accessing DPIRestrictionGroup properties
dpirestrictiongroup = ...  # obtain from Controller interface
print(dpirestrictiongroup.id)
```

## Event

| Property | Description |
|----------|-------------|
| `datetime` | Datetime of event '2020-03-01T15:35:08Z'. |
| `key` | Event key e.g. 'EVT_WU_Disconnected'. |
| `event` | Event key e.g. 'EVT_WU_Disconnected'. To be removed. |
| `msg` | Event message. |
| `time` | Time of event 1583076908000. |
| `mac` | MAC of client or device. |
| `ap` | Access point connected to. |
| `bytes` | Bytes of data consumed. |
| `channel` | Wi-Fi channel. |
| `client` | MAC address of client. |
| `device` | MAC address of device. |
| `duration` | Duration. |
| `hostname` | Nice name. |
| `radio` | Radio. |
| `subsystem` | Subsystem like 'lan' or 'wlan'. |
| `site_id` | Site ID. |
| `ssid` | SSID. |
| `version_from` | Version from. |
| `version_to` | Version to. |

```python
# Accessing Event properties
event = ...  # obtain from Controller interface
print(event.datetime)
```

## FirewallPolicy

| Property | Description |
|----------|-------------|
| `id` | Unique id of firewall policy. |
| `name` | Firewall policy name. |
| `enabled` | Is firewall policy enabled. |
| `action` | Firewall policy action. |
| `predefined` | Is this a predefined policy. |
| `description` | Policy description. |
| `protocol` | Policy protocol. |
| `connection_state_type` | Connection state type. |
| `connection_states` | List of connection states. |
| `create_allow_respond` | Whether to create allow respond rule. |
| `destination` | Destination endpoint configuration. |
| `source` | Source endpoint configuration. |
| `icmp_typename` | ICMP type name. |
| `icmp_v6_typename` | ICMPv6 type name. |
| `index` | Policy index/priority. |
| `ip_version` | IP version (IPv4/IPv6/BOTH). |
| `logging` | Whether logging is enabled. |
| `match_ip_sec` | Whether to match IPSec traffic. |
| `match_opposite_protocol` | Whether to match opposite protocol. |
| `schedule` | Policy schedule configuration. |

```python
# Accessing FirewallPolicy properties
firewallpolicy = ...  # obtain from Controller interface
print(firewallpolicy.id)
```

## FirewallZone

| Property | Description |
|----------|-------------|
| `id` | Unique ID of firewall zone. |
| `name` | Firewall zone name. |
| `attr_no_edit` | Whether zone is editable. |
| `default_zone` | Whether this is a default zone. |
| `network_ids` | List of network IDs associated with zone. |
| `zone_key` | Zone key identifier. |

```python
# Accessing FirewallZone properties
firewallzone = ...  # obtain from Controller interface
print(firewallzone.id)
```

## Outlet

| Property | Description |
|----------|-------------|
| `name` | Name of outlet. |
| `index` | Outlet index. |
| `has_relay` | Is the outlet controllable. Not reported by USP-PDU-Pro, see caps. |
| `relay_state` | Is outlet power on. |
| `cycle_enabled` | Modem Power Cycle. |
| `has_metering` | Is metering supported. Reported false by UP1 and UP6 which does not have power metering. Not reported by by USP-PDU-Pro, see caps. |
| `caps` | Outlet capabilities. 1: Outlet supports relay (switching) 3: Outlet supports relay and metering |
| `voltage` | Voltage draw of outlet. |
| `current` | Usage of outlet. |
| `power` | Power consumption of the outlet. |
| `power_factor` | Power factor. |

```python
# Accessing Outlet properties
outlet = ...  # obtain from Controller interface
print(outlet.name)
```

## Port

| Property | Description |
|----------|-------------|
| `ifname` | Port name used by USG. |
| `media` | Media port is connected to. |
| `name` | Port name. |
| `port_idx` | Port index. |
| `poe_caps` | Port PoE capabilities. 0 - no caps 3 - auto (PoE/PoE+) 35 - auto (Poe/PoE+/PoE++) 7 - 24V passive 8 - Passthrough |
| `poe_class` | Port PoE class. |
| `poe_enable` | Is PoE supported/requested by client. |
| `poe_mode` | Is PoE auto, pasv24, passthrough, off or None. |
| `poe_power` | Is PoE power usage. |
| `poe_voltage` | Is PoE voltage usage. |
| `portconf_id` | Port configuration ID. |
| `port_poe` | Is PoE used. |
| `rx_bytes` | Bytes received. |
| `rx_bytes_r` | Bytes recently received. |
| `tx_bytes` | Bytes transferred. |
| `tx_bytes_r` | Bytes recently transferred. |
| `up` | Is port up. |

```python
# Accessing Port properties
port = ...  # obtain from Controller interface
print(port.ifname)
```

## PortForward

| Property | Description |
|----------|-------------|
| `id` | Unique ID of port forward. |
| `destination_port` | Destination port. |
| `enabled` | Is port forward enabled. |
| `forward_port` | Forwarded port. |
| `forward_ip` | IP address to forward. |
| `name` | Name of port forward. |
| `port_forward_interface` | Interface to expose port forward. |
| `protocol` | Protocol to forward. tcp_udp |
| `site_id` | Site id port forward belongs to. |
| `source` | Source. |

```python
# Accessing PortForward properties
portforward = ...  # obtain from Controller interface
print(portforward.id)
```

## Site

| Property | Description |
|----------|-------------|
| `site_id` | Site ID. |
| `description` | Site description. |
| `hidden_id` | Unknown. |
| `name` | Site name. |
| `no_delete` | Can not delete site. |
| `role` | User role. |

```python
# Accessing Site properties
site = ...  # obtain from Controller interface
print(site.site_id)
```

## SystemInformation

| Property | Description |
|----------|-------------|
| `anonymous_controller_id` | Anonymous controller ID. |
| `device_type` | Network host device type. |
| `hostname` | Host name. |
| `ip_address` | External IP address. |
| `is_cloud_console` | Cloud hosted console. |
| `name` | Name. |
| `previous_version` | Previous application version. |
| `update_available` | Application update available. |
| `uptime` | Application uptime. |
| `version` | Current application version. |

```python
# Accessing SystemInformation properties
systeminformation = ...  # obtain from Controller interface
print(systeminformation.anonymous_controller_id)
```

## TrafficRoute

| Property | Description |
|----------|-------------|
| `id` | ID of traffic route. |
| `description` | Description given by user to traffic route. |
| `domains` | What IP addresses are matched against by this traffic route. Note: Domain matching requires the client devices to use the UniFi gateway as the DNS server. |
| `enabled` | Is traffic route enabled. |
| `ip_addresses` | What IP addresses are matched against by this traffic route. |
| `ip_ranges` | What IP addresses are matched against by this traffic route. |
| `matching_target` | What target is matched by this traffic route. |
| `network_id` | Network ID that this rule applies to. |
| `next_hop` | Used for defining a static route. |
| `regions` | Regions that the rule applies to. |
| `target_devices` | What target devices are affected by this traffic route. |

```python
# Accessing TrafficRoute properties
trafficroute = ...  # obtain from Controller interface
print(trafficroute.id)
```

## TrafficRule

| Property | Description |
|----------|-------------|
| `id` | ID of traffic rule. |
| `description` | Description given by user to traffic rule. |
| `enabled` | Is traffic rule enabled. |
| `action` | What action is defined by this traffic rule. |
| `matching_target` | What target is matched by this traffic rule. |
| `target_devices` | What target devices are affected by this traffic rule. |

```python
# Accessing TrafficRule properties
trafficrule = ...  # obtain from Controller interface
print(trafficrule.id)
```

## Voucher

| Property | Description |
|----------|-------------|
| `id` | ID of voucher. |
| `site_id` | Site ID. |
| `note` | Note given by creator to voucher. |
| `code` | Code of voucher in known format 00000-00000. To enter the code on the captive portal, the hyphen must be placed after the fifth digit. |
| `quota` | Allowed uses (0 = unlimited) of voucher. |
| `duration` | Expiration of voucher. |
| `qos_overwrite` | Defaults for QoS overwritten by the use of this voucher. |
| `qos_usage_quota` | Quantity of bytes (in MB) allowed when using this voucher. |
| `qos_rate_max_up` | Up speed (in kbps) allowed when using this voucher. |
| `qos_rate_max_down` | Down speed (in kbps) allowed when using this voucher. |
| `used` | Number of uses of this voucher. |
| `create_time` | Create datetime of voucher. |
| `start_time` | Start datetime of first usage of voucher. |
| `end_time` | End datetime of latest usage of voucher. |
| `for_hotspot` | For hotspot use. |
| `admin_name` | Creator name of voucher. |
| `status` | Status of voucher. |
| `status_expires` | Status expires in seconds. |

```python
# Accessing Voucher properties
voucher = ...  # obtain from Controller interface
print(voucher.id)
```

## Wlan

| Property | Description |
|----------|-------------|
| `id` | ID of WLAN. |
| `bc_filter_enabled` | Is BC filter enabled. |
| `bc_filter_list` | List of BC filters. |
| `dtim_mode` | DTIM mode. |
| `dtim_na` | DTIM NA. |
| `dtim_ng` | DTIM NG. |
| `enabled` | Is WLAN enabled. |
| `group_rekey` | Group rekey. |
| `is_guest` | Is WLAN a guest network. |
| `mac_filter_enabled` | Is MAC filtering enabled. |
| `mac_filter_list` | List of MAC filters. |
| `mac_filter_policy` | MAC filter policy. |
| `minrate_na_advertising_rates` | Minrate NA advertising rates. |
| `minrate_na_beacon_rate_kbps` | Minrate NA beacon rate kbps. |
| `minrate_na_data_rate_kbps` | Minrate NA data rate kbps. |
| `minrate_na_enabled` | Is minrate NA enabled. |
| `minrate_na_mgmt_rate_kbps` | Minrate NA management rate kbps. |
| `minrate_ng_advertising_rates` | Minrate NG advertising rates. |
| `minrate_ng_beacon_rate_kbps` | Minrate NG beacon rate kbps. |
| `minrate_ng_cck_rates_enabled` | Is minrate NG CCK rates enabled. |
| `minrate_ng_data_rate_kbps` | Minrate NG data rate kbps. |
| `minrate_ng_enabled` | Is minrate NG enabled. |
| `minrate_ng_mgmt_rate_kbps` | Minrate NG management rate kbps. |
| `name` | WLAN name. |
| `name_combine_enabled` | If 2.5 and 5 GHz SSIDs should be combined. |
| `name_combine_suffix` | Suffix for 2.4GHz SSID if name is not combined. |
| `no2ghz_oui` | No 2GHz OUI. |
| `schedule` | Schedule list. |
| `security` | Security. |
| `site_id` | WLAN site ID. |
| `usergroup_id` | WLAN user group ID. |
| `wep_idx` | WEP index. |
| `wlangroup_id` | WLAN group ID. |
| `wpa_enc` | WPA encryption. |
| `wpa_mode` | WPA mode. |
| `x_iapp_key` | X iapp key. |
| `x_passphrase` | Passphrase. |

```python
# Accessing Wlan properties
wlan = ...  # obtain from Controller interface
print(wlan.id)
```

