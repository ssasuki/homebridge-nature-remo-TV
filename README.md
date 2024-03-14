# homebridge-nature-remo-tv
  [Homebridge](https://github.com/homebridge/homebridge) plugin to turn TV on and off using  [Nature Remo](https://nature.global/nature-remo/).

## Installation
```bash
npm install -g homebridge-nature-remo-tv
```

## Example config.json
```json
  "accessories": [
    {
      "accessory": "NatureRemoTV",
      "name": "[Name display in Home app]",
      "access_token": "[Your access_token]",
      "appliance_id": "[aaaaaaaa-aaaa-aaaa-aaaa-aaaaaaaaaaaa]"
    }
  ]
```
- `name` can be set whatever you want
- To get `access_token`, visit https://home.nature.global/
- To get `signal_ID_on` and `signal_ID_off`, run `curl -X GET "https://api.nature.global/1/appliances" -H "Authorization: Bearer [access_token]"` and find `id` key
- `accessory` must be `NatureRemoSwitch`
