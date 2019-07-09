# kafka-connect-transform-flatten-avro
Kafka Connect Single Message Transform to flatten optional null value in avro

The original flatten has the drawback of throwing NPE when nested optional schema has null value

## How to use

add the following config to your connector

```
"transforms": "flattenAvro",
"transforms.flattenAvro.type": "org.sendoh.kafka.connect.transforms.FlattenAvro$Value",
```