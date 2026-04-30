
1. Sensores IoT
Sensores geram dados continuamente em tempo real. Eles se comunicam via protocolo MQTT, padrão leve e eficiente para ambientes IoT com recursos limitados.

2. AWS IoT Core
Serviço gerenciado da Amazon que recebe as mensagens dos sensores automaticamente. Aplica regras de roteamento para encaminhar os dados ao back-end sem necessidade de infraestrutura manual de broker.

3. Back-end / API REST
Ele vai validar, processar e distribuir os dados recebidos. mostra endpoints REST que direcionam as escritas simultaneamente para os dois bancos de dados, garantindo que o mesmo volume de dados seja inserido em ambos para fins de comparação justa no benchmark.

4. Amazon RDS (PostgreSQL) vs Amazon DynamoDB
Os mesmos dados são gravados em paralelo nos dois bancos:

RDS/PostgreSQL — banco relacional gerenciado, com suporte a ACID, schema definido e consultas complexas com joins.

DynamoDB — banco NoSQL serverless, com schema flexível, otimizado para alta taxa de inserção e escalabilidade horizontal automática.

5. Benchmark de Desempenho
O benchmark coleta e compara métricas dos dois bancos sob as mesmas condições de carga: latência de inserção, throughput, tempo de consulta e uso de recursos.

6. Dashboard Analítico
Interface de visualização que consome tanto os dados históricos armazenados quanto os dados correntes em tempo real, permitindo acompanhar o comportamento dos sensores e os resultados do benchmark de forma contínua.