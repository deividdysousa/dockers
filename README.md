# Dockers
Repositorio pessoal de codigo dockers

## Indice
- [mysql](mysql.yml) banco de dados mysql-ce


## EnvFile
Possue arquivo de [exemplo](.env.example), bastando apenas copiar e colar como `.env`


## Comandos
- `docker-compose -f file.yml up -d`
- `docker-compose -f file.yml down --remove`


#### Kafka
Cria um topico
- `docker-compose -f kafka.yml exec kafka kafka-topics --create --topic meu-topico --partitions 1 --replication-factor 1 --if-not-exists --zookeeper localhost:32181`

Decrição de um topico
- `docker-compose -f kafka.yml exec kafka kafka-topics --describe --topic meu-topico --zookeeper localhost:32181`

Ficar escutando um topico
- `docker-compose -f kafka.yml exec kafka kafka-console-consumer --bootstrap-server localhost:29092 --topic meu-topico --from-beginning`