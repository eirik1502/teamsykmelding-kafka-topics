# teamsykmelding-kafka-topics
Repo for Team Sykmelding sine kafkatopics.

> **Note**
> Dette er er eit repo kun for teamsykmelding om kafka topicene vi har, som ikke er av allmenn interesse. 
> Vi har derfor valgt å holde dette repoet lukket

## Bruk av kafka-consumer-groups
Kafka-consumer-groups lar deg se hvilke topics en consumer lytter på, samt offset og eventuelt lag for disse. Du kan 
også sette offset manuelt. For å bruke kafka-consumer-groups må du gjøre følgende: 
1. Vær tilkoblet naisdevice og ha tilgang til kafka-brokers

### Noen nyttige kommandoer for kafka-consumer-groups
Se informasjon om en consumer: 

``kafka-consumer-groups --command-config <config> --bootstrap-server <HOST>:<PORT> --group <consumerGroupName> --describe``

Sette offset for en gitt topic basert på timestamp: 

``kafka-consumer-groups --command-config <config> --bootstrap-server <HOST>:<PORT> --group <consumerGroupName>  --topic <topic> --reset-offsets --to-datetime '2021-12-05T00:00:00.000' --execute``

OBS: For å endre offset må den aktuelle consumer-group være inaktiv. 
