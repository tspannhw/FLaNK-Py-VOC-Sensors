## FLaNK-Py-VOC-Sensors

### From sploot machine

### Hardware List

Pimoroni Breakout Garden for Raspberry Pi 400
Raspberry Pi Official USB-C Power Supply - US
Raspberry Pi 400
Pimoroni Breakout Garden MLX90640 Thermal Camera Standard
Pimoroni Breakout Garden SGP30 Air Quality Sensor Breakout (TVOC/eCO2)
Python 3
Pimoroni Breakout Garden Python Libraries

### Data


### Running

````
python3 -W ignore /opt/demo/rp400cloudera.py

Sent message to kafka  sploot_baq_20230320193304

````

### Example Record

````
{"uuid": "sploot_pjt_20230320193227", "ipaddress": "192.168.1.159", "cputempf": 97, "runtime": 0, "host": "sploot", "hostname": "sploot", "macaddress": "e4:5f:01:f5:6c:e4", "endtime": "1679340747.5778904", "te": "0.0008721351623535156", "cpu": 0.2, "diskusage": "51240.8 MB", "memory": 5.5, "rowid": "20230320193227_13fdfc1a-dcd6-4b21-b869-e8a8af3f2afe", "systemtime": "03/20/2023 15:32:28", "ts": 1679340748, "starttime": "03/20/2023 15:32:27", "equivalentco2ppm": 416.0, "totalvocppb": 2.0}

````

### Schema

````

  {
 "type": "record",
 "name": "voc",
 "fields": [
  {
   "name": "uuid",
   "type": ["string","null"]
  },
    {
   "name": "rowid",
   "type": ["string","null"]
  },
  {
   "name": "systemtime",
   "type": ["string","null"]
  },
  {
   "name": "cpu",
   "type": ["double","null"]
  },
  {
   "name": "memory",
   "type": ["double","null"]
  },
    {
   "name": "ipaddress",
   "type": ["string","null"]
  },  
  {
   "name": "macaddress",
   "type": ["string","null"]
  },
  {
   "name": "endtime",
   "type": ["string","null"]
  },
  {
   "name": "runtime",
   "type": ["int","null"]
  },
  {
   "name": "ts",
   "type": ["int","null"]
  },
  {
   "name": "starttime",
   "type": ["string","null"]
  },
  {
   "name": "diskusage",
   "type": ["string","null"]
  },
  {
   "name": "te",
   "type": ["string","null"]
  },
  {
   "name": "equivalentco2ppm",
   "type": ["double","null"]
  },
  {
   "name": "totalvocppb",
   "type": ["double","null"]
  },
  {
   "name": "host",
   "type": ["string","null"]
  },
  {
   "name": "hostname",
   "type": ["string","null"]
  }
 ]
}

````


### Related

https://github.com/tspannhw/Flow-SGP30-MLX90640


