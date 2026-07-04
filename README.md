# Fundamentos de Cloud com AWS

## Introdução á AWS e Conceitos básicos

Nesse primeiro módulo começamos a entender o motivo da computação em nuvem está tão em alta nós dias de hoje, com o avanço da inteligencia artificial no mercado, surgiram mais aplicações e mais aplicações necessitam de mais recursos computacionais.

Logo depois partimos para a história da amazon fundada la em 1994 por Jeff bezos, onde ele decidiu dar o nome da empresa de "Amazon", graças ao Rio Amazonas que é o maior rio do planeta terra.

Depois em 2006 veio a AWS(Amazon Web Services) que foi fundada como uma resposta a necessidade de oferecer serviços de infraestrutura em nuvem.

Antes da computação em nuvem se tornar popular, as empresas utilizavam o modelo On-premises, onde toda a infraestrutura ficava dentro da própia empresa.

O que é o modelo On-premise e como ele funciona ?

Antes as empresas elas presisavam, comprar servidores físicos, instalar os servidores em uma sala ou em um datacenter, fazer configuração de rede e internet, instalar sistemas operacionais, instalar e configurar banco de dados, instalar o runtime da aplicação que irá rodar, fazer a configuração de backups, segurança e firewaal e ainda realizar a manutenção do hardware.

Com a chegada da computação em nuvem, não era mais necessário comprar servidores, pois poderiamos alugar recursos sob demanda e pagar somente pelo uso.

### Infraestrutura Global da AWS

A infraestrutura global da AWS fornece mais de 200 serviços em todo mundo, onde se precisarmos implantar um workload em todo mundo próximos dos usuários finais com uma latência baixa ela disponibiliza tudo isso.

Ela possui uma rede global de data centers que são chamadas de Regions e Availability Zones, onde as regions são áreas geográficas contendo várias Availability Zones, em cada region existem no mínimo 2 Availabilit Zones, onde se pode fazer uma replica da sua aplicação em diferentes zonas se uma der problema ela ainda continua online.

### Modelo de Negócio da AWS

A AWS assim como outros cloud provider possui o modelo de pagamento por uso, isso é oque difere o modelo cloud dos demais modelos antigos como On-premises.

Ela fornece diversos serviços desde computação, armazenamento e banco de dados até serviços especializados como machine learning, IoT, e análise de dados.

Dentro da AWS temos diferentes modelos de cloud como Pública, Híbrida e Privada

Pública

- Maior risco de privacidade
- Acesso imediato
- Alto desempenho
- Baixo custo
- Escalabilidade

Privada

- Segurança
- Controle total
- Alto investimento no custo continuo da operação

Híbrido

- Acesso imediato
- Alto desempenho
- Baixo custo
- Escalabilidade
- Segurança
- Controle total

### Modelos de computação em nuvem

1. IaaS (Infrastrutucture as a Service)
   O provedor ele fornece uma estrutura básica

- Servidores
- Rede
- Armazenamento
- Máquinas virtuais

2. PaaS (Plataform as a Service)
   O provedor cuida da infraestrutura e da plataforma
   Precisamos apenas:

- Escrever o código
- Fazer Deploy

3. SaaS (Software as a Service)
   O software jpa está pronto, apenas utilizamos.

## Configurações da conta e práticas de segurança

Sempre que nós criamos uma conta na AWS temos uma contra principal (root) que possui super permissões dentro do seu workspace, é muito importante que nós guardemos essa conta que tem super privilégio e depois criar um outro usuário que ter permite ter alguns privilégio dentro da plataforma.
Boas práticas de segurança na AWS:

- Criar conta root e depois guardar
  A conta root possui super privilégios, por isso é importante não criar e sair utilizando através do IAM, criar outra conta com alguns privilégios de administrador
- Não compartilhar dados da conta
  Não compartilhar o acesso da sua conta com outras pessoas.
- Ficar atento ao email com as cobranças
  As cobranças da AWS chega no email que é utilizado para criar sua conta
- Autenticação MFA
  Ela é importante para garantir segurança
- Estabelecer barreira de proteção para permissões
  Criar políticas dentro da plataforma para dar alguma permissões, segregar acessos

IAM - é uma ferramenta que gerencia acessos dentro da plataforma

## Primeiro acesso a AWS

Quais são as formas de se criar recursos na AWS ?

- Através do portal
- Via SDKs
- Cloud Shel

Quais são as formas de acessar a AWS ?

- Console AWS
  O console da AWS é a interface gráfica onde podemos gerenciar nossos serviçis

- Cloud Shell
  Através dos comandos shell é possível gerenciar a plataforma, podemos interagir com a nuvem através de linhas de comandos.

- AWS CLI
  É uma interface que nós podemos usar comandos para criar nossos recursos, através das nossas credenciais podemos nós conectar com a AWS e executar comando direto do nosso PC

## Controle de gastos na AWS

É possível definir múltiplos alertas para diferentes valores do orçamento, desta maneira conseguimos ver quando um recurso está sendo mais utilizado do que deveria

## Amazon EC2 - (Elastic Compute Cloud)

O que são instâncias EC2?
EC2 - Elastic Compute Cloud, são as máquinas virtuais da AWS, podendo ser com sistemas operacional windows ou linux

Uma EC2 é composta por:

- CPU
- Memória
- Disco/Armazenamento
- Rede
- Sistema Operacional

Existem opções de ter uma máquina isolada onde o recurso é todo seu, ou então dentro de um servidor várias máquinas virtuais onde você utiliza um espeço dele.
No modelo Cloud, uma EC2 é do tipo IaaS ou seja, quando criamos um EC2 estamos utilizando o tipo infraestrutura como serviço

Uma maneira de otimizar recursos de uma instância é parar enquanto ela não está sendo utilizada.

## Armazenamento na AWS

### Amazon EBS - (Amazon Elastic Block Store)

O amazon EBS é uma storage que pode ser anexada em uma instância EC2. Ele permite expandir a capacidade de armazenamento de maneira rápida.
Conseguimos criar uma partição em nossa instância, seria como anexar um HD externo. Escolhemos o modelo e o size e anexamos a nossa VM (EC2).

## Amazon S3 - (Amazon Simple Service Storage)

O amazon S3 é um serviço de armazenamento de objetos em nuvem oferecidos pela AWS.
É ideal para armazenar, organizar e recuperar grandes volumes de dados de forma segura e escalável, o amazon S3 possui algumas classes de storages onde conseguimos economizar nos custos, partindo das que possuem uma frequência alta de acessos para as que possui menos fequência de acessos.
O lifecycle permite fazer a transição de objetos e migrar automaticamente para a classe glacier.
