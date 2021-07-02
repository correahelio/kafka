===Executando zookeper====
zookeeper-server-start.bat C:\Users\<user>\workspace\kafka\config\zookeeper.properties

====Executando Kafka===
kafka-server-start.bat C:\Users\<user>\workspace\kafka\config\server.properties
kafka-server-start.bat C:\Users\<user>\workspace\kafka\config\server2.properties


=====Mensagem com chave valor / producer====
kafka-console-producer --broker-list localhost:9092 --topic teste --property "parser.key=true" --property "key.separator=,"
kafka-console-producer --broker-list localhost:9092,localhost:9093 --topic teste


==Criando tópico===
kafka-topics --bootstrap-server localhost:9092 --create --topic testejava

====Criando consumers===
kafka-console-consumer --bootstrap-server 127.0.0.1:9092 --topic teste
kafka-console-consumer --bootstrap-server 127.0.0.1:9092 --topic teste --property "print.key=true" --property "key.separator=," --group grupo1
kafka-console-consumer --bootstrap-server 127.0.0.1:9092 --topic teste --property "print.key=true" --property "key.separator=," --group grupo1

kafka-topics --bootstrap-server 127.0.0.1:9092 --topic teste --describe
kafka-topics --bootstrap-server localhost:9092 --alter --topic teste --partitions 10



====Interface Gráfica===
Conduktor