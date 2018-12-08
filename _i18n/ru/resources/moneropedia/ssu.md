---
tags: ["kovri"]
terms: ["SSU"]
summary: "SSU - это один из двух транспортных средств Kovri"
---

### Основная информация

SSU (Secure Semi-reliable UDP) является одной из двух технологий шифрования на @транспортном уровне @Kovri.

Подобно @NTCP *основной* целью @SSU является безопасная передача внутрисетевых @I2NP сообщений по @туннелям, но, в отличие от @NTCP, @SSU работает только с протоколом [UDP](https://en.wikipedia.org/wiki/User_Datagram_Protocol).

### Углублённая информация

- Как и @NTCP, @SSU является ориентированной на соединение "точка-точка" транспортной технологией данных
- Технология называется  *semi-reliable* ("полунадёжной"), так как @SSU многократно передаёт *неподтверждённые* сообщения (вплоть до максимального количества, после чего сообщение сбрасывается)
- @SSU также обеспечивает несколько уникальных сервисов (в дополнение к своей функции @транспортного уровня):
  - обнаружение IP (путём локальной проверки или [тестирования одноранговых узлов](https://geti2p.net/en/docs/transport/ssu#peerTesting))
  - прослеживание [NAT](https://en.wikipedia.org/wiki/Network_address_translation) (при помощи [вводных элементов](https://geti2p.net/en/docs/transport/ssu#introduction))
  - статус [Firewall](https://en.wikipedia.org/wiki/Firewall_%28computing%29) и, если такая функция будет реализована, @SSU будет уведомлять @NTCP об изменениях статуса внешнего адреса или Firewall

### Примечания

Подробности на странице @Java-I2P [SSU](https://geti2p.net/en/docs/transport/ssu)