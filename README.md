# youless
Home Assistant custom sensor for youless

Based on the version of Gerben Jongerius, but displays the counter values directly into the icon instead of an image and adds some extra meter sensors.

Update: Thanks to @gjong this sensor has a sucessull pull request to become part of the officiel integrations soon.


**Available sensors**


| Sensor | Description | Column |
|:----------|:----------|:----------|
| pwr | Current Power usage | CW |
| net | Net Power usage counter | kWh |
| p1 |	Power Meter Low |	kWh |
| p2 |	Power Meter High | 	kWh |
| n1 |	Power Delivery Low |	kWh |
| n2 |	Power Delivery High |	kWh |
| cs0 |	Current Power usage for extra meter connected to s0 port | kWh |
| ps0 |	Net Power usage counter for extra meter connected to s0 port | W |
| gas |	Gas consumption | m3 |


**Installation**

* create a folder called 'custom_components' if not exists into your Home Assistant configuration folder
* Download the folder Youless with its contents into this folder.
* Add configuration to you configuration.yaml file:


```
  - platform: youless
    name: Youless
    host: <your youless IP address>
    monitored_variables:
      - pwr
      - net
      - p1
      - p2
      - n1
      - n2
      - cs0
      - ps0
      - gas
```
