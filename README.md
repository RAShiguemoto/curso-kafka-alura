# Kafka  Produtores e Consumidores  
Este repositório contém exemplos de código para a primeira unidade do curso de Kafka da Alura, focando em produtores e consumidores.

## Prérequisitos
  - Java 11+  
  - Apache Kafka (instalação e configuração)  
  - Apache Zookeeper (instalação e configuração)  

Instalação e Configuração

Baixar e instalar o Apache Kafka e o Apache Zookeeper:
https://kafka.apache.org/downloads
https://zookeeper.apache.org/


Configurar o Zookeeper:
Criar um arquivo zookeeper.properties na pasta config do Kafka.
Definir as propriedades do Zookeeper no arquivo zookeeper.properties.


Configurar o Kafka:
Criar um arquivo server.properties na pasta config do Kafka.
Definir as propriedades do Kafka no arquivo server.properties.


Iniciar o Zookeeper:
                 
                    
                        bash
                        
                            Copiar código
                        
                    
                    
                        bin/zookeeperserverstart.sh config/zookeeper.properties
                    
                
        
Iniciar o Kafka:
                 
                    
                        bash
                        
                            Copiar código
                        
                    
                    
                        bin/kafkaserverstart.sh config/server.properties
                    
                
        

Executando os exemplos

Criar um tópico:
                 
                    
                        bash
                        
                            Copiar código
                        
                    
                    
                        bin/kafkatopics.sh create bootstrapserver localhost:9092 replicationfactor 1 partitions 1 topic ECOMMERCE_NEW_ORDER
                    
                
        
Executar o produtor:
                 
                    
                        bash
                        
                            Copiar código
                        
                    
                    
                        java cp target/classes br.com.alura.ecommerce.NewOrderProducer
                    
                
        
Executar o consumidor:
                 
                    
                        bash
                        
                            Copiar código
                        
                    
                    
                        bin/kafkaconsoleconsumer.sh bootstrapserver localhost:9092 topic ECOMMERCE_NEW_ORDER frombeginning
                    
                
        

Anotações

Executar Zookeeper antes do Kafka:
                 
                    
                        bash
                        
                            Copiar código
                        
                    
                    
                        bin/zookeeperserverstart.sh config/zookeeper.properties
                    
                
        
Executar Kafka:
                 
                    
                        bash
                        
                            Copiar código
                        
                    
                    
                        bin/kafkaserverstart.sh config/server.properties
                    
                
        
Listar tópicos:
                 
                    
                        bash
                        
                            Copiar código
                        
                    
                    
                        bin/kafkatopics.sh list bootstrapserver localhost:9092
                    
                
        
Descrever os tópicos:
                 
                    
                        bash
                        
                            Copiar código
                        
                    
                    
                        bin/kafkatopics.sh describe bootstrapserver localhost:9092
                    
                
        
Criando consumer para ficar escutando os tópicos:
                 
                    
                        bash
                        
                            Copiar código
                        
                    
                    
                        bin/kafkaconsoleconsumer.sh bootstrapserver localhost:9092 topic ECOMMERCE_NEW_ORDER frombeginning
                    
                
        

Observações

Os exemplos de código neste repositório são apenas para fins de demonstração.
Para uma implementação mais robusta, é recomendável utilizar bibliotecas como o Apache Kafka Client para Java.
Este repositório é apenas um ponto de partida para o aprendizado de Kafka. 
Para mais informações sobre Kafka, consulte a documentação oficial: https://kafka.apache.org/

Próximos passos

Implementar um consumidor em Java para o tópico ECOMMERCE_NEW_ORDER.
Criar um novo tópico para armazenar informações de pedidos processados.
Implementar um produtor para enviar mensagens para o novo tópico.

Espero que este README seja útil para você! 
