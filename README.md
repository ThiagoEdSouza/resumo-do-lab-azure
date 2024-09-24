
# Resumo do Lab: Azure, Computação em Nuvem e Desenvolvimento Colaborativo

Este repositório contém um resumo das lições aprendidas durante o desenvolvimento do lab na DIO, abrangendo tópicos desde Azure e computação em nuvem até versionamento de código e contribuição em projetos open source.

## Fundamentos do Microsoft Azure (AZ-900)

Introdução ao Azure e Computação em Nuvem
O Microsoft Azure é uma plataforma de computação em nuvem que oferece uma ampla gama de serviços para desenvolvimento, teste, implantação e gerenciamento de aplicações e serviços. A computação em nuvem é definida como o fornecimento de serviços de computação através da Internet, incluindo servidores, armazenamento, bancos de dados, rede, software, análise e inteligência.

## Modelos de Implantação de Nuvem

### 2.1 Nuvem Pública:

- Propriedade e operação por provedores de serviços de nuvem terceirizados
- Recursos compartilhados entre múltiplos clientes
- Acessível via conexões de rede seguras (tipicamente Internet)

### 2.2 Nuvem Privada:

- Infraestrutura dedicada a uma única organização
- Pode ser hospedada on-premises ou por terceiros
- Oferece maior controle e privacidade

### 2.3 Nuvem Híbrida:

- Combina nuvens públicas e privadas
- Permite compartilhamento de dados e aplicações entre elas
- Oferece maior flexibilidade e opções de implantação

## Modelos de Serviço em Nuvem

### 3.1 Infrastructure as a Service (IaaS):

IaaS representa o nível mais fundamental dos serviços de computação em nuvem, oferecendo:

- Recursos de computação virtualizados através de máquinas virtuais (VMs) com capacidade de processamento escalável.
- Armazenamento em bloco, objeto e arquivo, com opções de redundância e replicação geográfica.
- Redes virtuais, incluindo VLANs, balanceadores de carga, firewalls e VPNs.

#### Responsabilidades do cliente:

- Gerenciamento e patching do sistema operacional (OS).
- Configuração e manutenção de middleware e runtime environments.
- Implementação e gerenciamento de aplicações e dados.

#### Vantagens técnicas:

- Controle granular sobre recursos de infraestrutura.
- Capacidade de implementar arquiteturas personalizadas.
- Suporte a uma ampla gama de sistemas operacionais e aplicações.

##### Exemplos de serviços: 
Amazon EC2, Microsoft Azure VMs, Google Compute Engine.

### 3.2 Platform as a Service (PaaS):

PaaS fornece uma plataforma de desenvolvimento e implantação completa, incluindo:

- Ambientes de execução pré-configurados para várias linguagens de programação (e.g., Java, Python, Node.js).
- Serviços de banco de dados gerenciados (SQL e NoSQL).
- Ferramentas de integração e entrega contínua (CI/CD).
- Serviços de análise de dados e business intelligence (BI).

#### Características técnicas:

- Abstração da infraestrutura subjacente, permitindo escalabilidade automática.
- APIs e SDKs para integração de serviços e desenvolvimento de aplicações.
- Suporte a microsserviços e arquiteturas serverless.

#### Responsabilidades do cliente:

- Desenvolvimento e manutenção de aplicações.
- Configuração de ambientes de implantação.
- Gerenciamento de dados e controle de acesso.

##### Exemplos de serviços: 
Heroku, Google App Engine, Microsoft Azure App Service.

### 3.3 Software as a Service (SaaS):

SaaS oferece aplicações completas hospedadas e gerenciadas na nuvem:

- Acesso baseado em web, geralmente através de APIs RESTful.
- Modelo de multilocação (multi-tenancy) para eficiência de recursos.
- Atualizações e patches automáticos gerenciados pelo provedor.

#### Características técnicas:

- Balanceamento de carga automático e alta disponibilidade.
- Criptografia de dados em repouso e em trânsito.
- Integração com outros serviços de nuvem e APIs de terceiros.

#### Vantagens para o usuário final:

- Eliminação de requisitos de hardware e software local.
- Acesso ubíquo através de diversos dispositivos e plataformas.
- Modelo de pagamento baseado em uso ou assinatura.

#### Considerações de segurança e conformidade:

- Autenticação multifator e controles de acesso baseados em função (RBAC).
- Conformidade com regulamentações como GDPR, HIPAA, dependendo do setor.

##### Exemplos de serviços: 
Salesforce, Google Workspace, Microsoft 365.

## Benefícios e Características do Azure

### 4.1 Alta Disponibilidade:

Garantida por SLAs (Service Level Agreements)
Implementada através de redundância e balanceamento de carga

### 4.2 Escalabilidade:

- Vertical (scale up/down): Aumento/diminuição de recursos de uma unidade
- Horizontal (scale out/in): Adição/remoção de unidades de recursos

### 4.3 Elasticidade:

Capacidade de ajustar recursos automaticamente baseado na demanda

### 4.4 Agilidade:

Rápida implantação e configuração de recursos de nuvem

### 4.5 Distribuição Geográfica:

Data centers globalmente distribuídos para melhor desempenho e conformidade

### 4.6 Recuperação de Desastres:

Serviços de backup, replicação de dados e failover

## Considerações Econômicas

### 5.1 CapEx vs OpEx:

#### CapEx (Despesas de Capital):

- Investimento inicial significativo em infraestrutura física
- Custos previsíveis ao longo do tempo
- Depreciação de ativos ao longo dos anos
- Benefícios fiscais potenciais

#### OpEx (Despesas Operacionais):

- Modelo de pagamento baseado no consumo
- Custos variáveis e flexíveis
- Sem investimento inicial em infraestrutura
- Facilita a escalabilidade e adaptação rápida

### 5.2 Economia de Escala:

Redução de custos devido à eficiência operacional em larga escala

## Serviços Principais do Azure

### 6.1 Computação:

- VMs (Máquinas Virtuais): Servidores virtualizados para execução de aplicações
- Containers: Ambientes isolados e leves para execução de aplicações
- Kubernetes Service: Orquestração de containers para implantações em larga escala

### 6.2 Rede:

- Virtual Network: Redes privadas isoladas na nuvem
- Load Balancer: Distribuição de tráfego entre múltiplos recursos
- VPN Gateway: Conexão segura entre redes on-premises e Azure

### 6.3 Armazenamento:

- Blob Storage: Armazenamento de objetos não estruturados
- File Storage: Compartilhamentos de arquivos totalmente gerenciados
- Queue Storage: Armazenamento de mensagens para processamento assíncrono
- Table Storage: Armazenamento NoSQL para dados estruturados

### 6.4 Banco de Dados:

- SQL Database: Banco de dados relacional totalmente gerenciado
- Cosmos DB: Banco de dados multi-modelo globalmente distribuído
- MySQL: Versão gerenciada do MySQL para Azure

### 6.5 Identidade:

Azure Active Directory: Serviço de gerenciamento de identidade e acesso

### 6.6 Segurança:

- Key Vault: Gerenciamento seguro de chaves criptográficas e segredos
- DDoS Protection: Proteção contra ataques de negação de serviço distribuído

## Ferramentas de Gerenciamento e Governança

### 7.1 Azure Portal: 
Interface gráfica para gerenciamento de recursos

### 7.2 Azure PowerShell e CLI: 
Ferramentas de linha de comando

### 7.3 Azure Resource Manager: 
Implantação e gerenciamento de recursos

### 7.4 Azure Policy: 
Implementação de padrões e conformidade

###7.5 Azure Monitor: 
Monitoramento e análise de desempenho

## Segurança e Conformidade

### 8.1 Azure Security Center: 
Monitoramento unificado de segurança

### 8.2 Azure Sentinel: 
Solução SIEM (Security Information and Event Management)

### 8.3 Conformidade:

- GDPR: Regulamento Geral de Proteção de Dados da União Europeia
- HIPAA: Lei de Portabilidade e Responsabilidade de Seguros de Saúde dos EUA
- ISO 27001: Padrão internacional para sistemas de gestão de segurança da informação
- SOC 1 e SOC 2: Relatórios de controles de segurança e disponibilidade

## Controle de Versão e Colaboração

### 9.1 Git: Sistema de controle de versão distribuído

Mantém histórico completo de alterações no código

#### Principais comandos:

- git init: Inicia um novo repositório
- git clone: Copia um repositório existente
- git add: Adiciona alterações à área de staging
- git commit: Salva as alterações no repositório local
- git push: Envia alterações para um repositório remoto
- git pull: Obtém e mescla alterações de um repositório remoto

###9.2 GitHub: 
Plataforma de hospedagem de código e colaboração

- Facilita a colaboração em projetos open source
- Recursos: Issues, Pull Requests, Actions para CI/CD

### 9.3 Azure DevOps: 
Suite de ferramentas para desenvolvimento e implantação contínuos.

#### Colaboração em Projetos Open Source:

- Fork: Cria uma cópia pessoal de um projeto
- Branch: Desenvolve novas funcionalidades isoladamente
- Pull Request: Propõe alterações para o projeto original
- Code Review: Processo de revisão das alterações propostas
- Merge: Incorporação das alterações aprovadas ao projeto principal

## 10.1 Service Level Agreements (SLAs) 

SLAs são contratos formais entre um provedor de serviços (neste caso, a Microsoft Azure) e o cliente, que definem o nível de serviço esperado em termos de disponibilidade e desempenho.

### 10.2 Funcionamento:

- Estabelecem métricas específicas e mensuráveis para o serviço
- Geralmente expressos em porcentagem de tempo de atividade (por exemplo, 99,9% de disponibilidade)
- Definem compensações ou créditos de serviço caso os níveis acordados não sejam atingidos

### 10.3 Características Principais:

- Uptime Garantido: Porcentagem do tempo em que o serviço estará disponível
- Latência: Tempo de resposta do serviço
- Throughput: Capacidade de processamento de dados
- Suporte: Tempos de resposta para diferentes níveis de severidade de problemas
