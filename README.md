# youless
Home Assistant custom sensor for youless

Based on the version of Gerben Jongerius. This version displays the counter values directly into the icon instead of an image and adds some extra meter sensors:

- pwr: Actual Power usage
- net: total netto counter (usage minus delivery combined for high and low counters)
- p1:  total power consumption low
- p2:  total power consumption high
- n1:  total power delivery low
- n2:  total power delivery high
- cs0: total for extra power meter connected to s0 port
- ps0: Actual Power usage for extra power meter connected to s0 port
- gas: total gas cunsumption 


Installation:
1) create a folder called 'custom_components' into your Home Assistant folder
2) create a folder called 'youless' in the custom_components folder. 
3) Download the 'sensor.py' file into this 'youless' folder
4) Create an empty file called '__init__.py' in the same folder
5) Add the following to your configuration.yaml:

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
