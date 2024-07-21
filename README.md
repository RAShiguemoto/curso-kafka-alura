# Kafka  Produtores e Consumidores  
Este repositório contém exemplos de código para a primeira unidade do curso de Kafka da Alura, focando em produtores e consumidores.

## Pré-requisitos
  - Java 11+  
  - Apache Kafka (instalação e configuração)  
  - Apache Zookeeper (instalação e configuração)  

## Instalação e Configuração  
  - Baixar e instalar o Apache Kafka e o Apache Zookeeper:  
    - https://kafka.apache.org/downloads
    - https://zookeeper.apache.org/

  - Configurar o Zookeeper:  
    - Criar um arquivo zookeeper.properties na pasta config do Kafka.  
    - Definir as propriedades do Zookeeper no arquivo zookeeper.properties.  

## Configurar o Kafka:  
  - Criar um arquivo server.properties na pasta config do Kafka.  
  - Definir as propriedades do Kafka no arquivo server.properties.  

## Minhas Anotações

### Executar Zookeeper antes do Kafka:
    bin/zookeeper-server-start.sh config/zookeeper.properties
                         
### Executar Kafka:
    bin/kafka-server-start.sh config/server.properties
                                
### Listar tópicos:
    bin/kafka-topics.sh --list --bootstrap-server localhost:9092

### Descrever os tópicos:
    bin/kafka-topics.sh --describe --bootstrap-server localhost:9092
                    
### Criando consumer para ficar escutando os tópicos:
    bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic ECOMMERCE_NEW_ORDER --from-beginning

## Observações

Os exemplos de código neste repositório são apenas para fins de demonstração.
Este repositório é apenas um ponto de partida para o aprendizado de Kafka.   
Para mais informações sobre Kafka, consulte a documentação oficial: https://kafka.apache.org/  

Espero que este README seja útil para você! 
