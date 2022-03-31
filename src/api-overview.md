# Zones Quickstart - Media Controller API

Each digital signs belong to a group called a zone. Let's look at the most common zone calls:

- Getting a list of all zones.
- Getting a single zone.
- Rebooting all devices in a zone.

To get a list of all zones, make a GET request to `/zone`.

```bash
# Getting all zones
curl https://api.example.com/zone
```

```JSON
[
  {
    "id": 1,
    "name": "north-tower",
    "readable_name": "North Tower"
  },
  {
    "id": 2,
    "name": "river-walk",
    "readable_name": "River Walk"
  }
]
```

Getting a single zone requires adding an ID to the request. Make a GET request to `/zone/{id}`.

```bash
# Getting north tower zone.
curl https://api.example.com/zone/1
```

```JSON

{
  "id": 1,
  "name": "north-tower",
  "readable_name": "North Tower"
}
```

There is also a function for requesting a reboot from each device in the zone. The reboot function is convenient when you need to swap the content for a zone in the middle of the day. The result is a message string.

```bash
# Reboot the river-walk zone
curl https://api.example.com/reboot_zone/2
```

```JSON

{
  "msg": "Rebooting river-walk zone"
}
```
