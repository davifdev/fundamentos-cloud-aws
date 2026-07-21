## AWS CloudFormation

- O CloudFormation é um serviço da AWS, que nós ajuda a configuar melhor os nossos recursos, sem precisar ficar gastando muito tempo gerenciando esses recursos focando mais nos aplicativos que serão exeutados na AWS. Nós criamos um modelo que descreve todos os recursos que vamos utilizar, e o CloudFormation cuida do provisionamento e da configuração desses recursos.

- Para criarmos uma aplicação Web escalável, precisamos de um banco de dados de backend, usar um grupo do Auto Scaling, um balanceador de carga do Elastic Load Balancing e uma instância de banco de dados Amazon Relational Database Service. Todas essas tarefas podem adicionar complexidade e tempo antes que sejam todas configuradas.

- Em vez disso podemos cirar ou modificar um modelo de CloudFormation existente. Um modelo vai descrever todos os recursos e propiedades. Ao usar esse modelo o CloudFormation provisionará o Auto Scaling, Balanceador de Carga e o Banco de dados para ser utilizados. Depois da pilha ser criada os nossos recursos da AWS estão em funcionamento.

- Se o nosso aplicativo precisa ter mais disponibilidade, é possível replicá-lo em várias regiões, de forma que se uma região se tornar indisponível, os usuários ainda podem usar o aplicativo em outras regiões. Podemos utilizar o nosso modelo do CloudFormation para criar recursos de modo consistente e repetível.
