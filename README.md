# nubesPC2
ejecutar los comandos de Kafka para crear un tema y producir y consumir mensajes.
-> docker-compose exec kafka kafka-topics --create --topic mi-tema --partitions 1 --replication-factor 1 --bootstrap-server kafka:9092
Esto creará un tema llamado "mi-tema" con 1 partición y un factor de replicación de 1.
Para producir mensajes en el tema, ejecuta el siguiente comando:
->docker-compose exec kafka bash -c "echo 'Hola mundo' | kafka-console-producer --topic mi-tema --bootstrap-server kafka:9092"
Esto enviará el mensaje "Hola mundo" al tema "mi-tema".
Para consumir mensajes del tema, ejecuta el siguiente comando:
->docker-compose exec kafka kafka-console-consumer --topic mi-tema --bootstrap-server kafka:9092 --from-beginning
