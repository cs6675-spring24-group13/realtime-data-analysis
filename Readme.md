## CS6675 Group 13 Realtime Trading Analysis

### I am still exploring the cryptofeeds!!

* [Binance US](https://www.binance.us/en) - Not working
* [Coinbase](https://www.coinbase.com/) - Need Authentication but cryptofeed libarary doesn't seem to support
* [Bequant](https://bequant.io/) - Working
* [HitBTC](https://hitbtc.com/) - Working


### Procedues to start process at Mac AppleSilicon

- Start docker
```
docker-compose up -d
```

- Log into the docker and check kafka's consumer

```
kafka-console-consumer --bootstrap-server localhost:9092 --topic ticker-HITBTC-XLM-USDT --from-beginning
```

- You can see the data in the consumer

```
{"exchange":"HITBTC","symbol":"XLM-USDT","bid":0.11924,"ask":0.119283,"timestamp":1709146868.173,"receipt_timestamp":1709146868.180787}
{"exchange":"HITBTC","symbol":"XLM-USDT","bid":0.11924,"ask":0.119288,"timestamp":1709146868.373,"receipt_timestamp":1709146868.397893}
{"exchange":"HITBTC","symbol":"XLM-USDT","bid":0.119247,"ask":0.119288,"timestamp":1709146868.574,"receipt_timestamp":1709146868.5954921}
{"exchange":"HITBTC","symbol":"XLM-USDT","bid":0.119247,"ask":0.119283,"timestamp":1709146868.974,"receipt_timestamp":1709146869.012954}
{"exchange":"HITBTC","symbol":"XLM-USDT","bid":0.119247,"ask":0.119288,"timestamp":1709146869.374,"receipt_timestamp":1709146869.4037209}
{"exchange":"HITBTC","symbol":"XLM-USDT","bid":0.119247,"ask":0.119283,"timestamp":1709146869.975,"receipt_timestamp":1709146870.0044413}
{"exchange":"HITBTC","symbol":"XLM-USDT","bid":0.119247,"ask":0.119288,"timestamp":1709146870.376,"receipt_timestamp":1709146870.409218}
{"exchange":"HITBTC","symbol":"XLM-USDT","bid":0.119247,"ask":0.119288,"timestamp":1709146870.676,"receipt_timestamp":1709146870.872053}
{"exchange":"HITBTC","symbol":"XLM-USDT","bid":0.119247,"ask":0.119283,"timestamp":1709146870.776,"receipt_timestamp":1709146870.87225}
{"exchange":"HITBTC","symbol":"XLM-USDT","bid":0.119247,"ask":0.119288,"timestamp":1709146871.077,"receipt_timestamp":1709146871.4190223}
{"exchange":"HITBTC","symbol":"XLM-USDT","bid":0.119252,"ask":0.119288,"timestamp":1709146872.078,"receipt_timestamp":1709146872.2285795}
{"exchange":"HITBTC","symbol":"XLM-USDT","bid":0.119288,"ask":0.119306,"timestamp":1709146872.579,"receipt_timestamp":1709146872.6436334}
{"exchange":"HITBTC","symbol":"XLM-USDT","bid":0.119291,"ask":0.119306,"timestamp":1709146872.779,"receipt_timestamp":1709146872.78021}
{"exchange":"HITBTC","symbol":"XLM-USDT","bid":0.119295,"ask":0.119347,"timestamp":1709146873.58,"receipt_timestamp":1709146873.587899}
{"exchange":"HITBTC","symbol":"XLM-USDT","bid":0.119312,"ask":0.119347,"timestamp":1709146873.881,"receipt_timestamp":1709146874.0210495}
```

- Stop the docker

```
docker compose down
```

- Some useful command


```
// output kafka's message from the begining
kafka-console-consumer --bootstrap-server localhost:9092 --topic ticker-HITBTC --from-beginning
kafka-console-consumer --bootstrap-server localhost:9092 --topic ticker-BEQUANT --from-beginning

// list kafka's topic
kafka-topics --bootstrap-server localhost:9092 --list

```
