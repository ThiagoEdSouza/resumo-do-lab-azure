
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

A alta disponibilidade na nuvem é crucial para garantir que os serviços permaneçam operacionais e acessíveis, mesmo em face de falhas de hardware ou software.

- SLAs (Service Level Agreements):
- Contratos que definem o nível de serviço garantido pelo provedor de nuvem.
- Geralmente expressos em porcentagem de tempo de atividade (ex: 99,99% de uptime).
- Podem incluir compensações financeiras se os níveis acordados não forem atingidos.

#### Implementação técnica:

##### - Redundância: 
Múltiplas instâncias de recursos críticos em diferentes zonas de disponibilidade.

#### - Balanceamento de carga: 
Distribuição inteligente de tráfego entre instâncias para evitar sobrecarga.

##### - Failover automático: 
Sistemas que detectam falhas e redirecionam tráfego para recursos saudáveis.

##### - Monitoramento contínuo: 
Sistemas de alerta que identificam e respondem a problemas em tempo real.

### 4.2 Escalabilidade:

A escalabilidade permite que os sistemas se adaptem a mudanças na demanda, garantindo performance e eficiência de custos.

#### - Escalabilidade Vertical (scale up/down):
- Envolve aumentar ou diminuir os recursos de uma única unidade (ex: CPU, RAM).
- Útil para aplicações que não podem ser facilmente distribuídas.
- Limitada pelo hardware máximo disponível em uma única máquina.
Exemplo: Aumentar a RAM de uma VM de 8GB para 16GB.

#### - Escalabilidade Horizontal (scale out/in):
- Adiciona ou remove unidades de recursos (ex: servidores, containers).
- Ideal para aplicações distribuídas e microserviços.
- Praticamente ilimitada, dependendo apenas da capacidade do provedor de nuvem.
- Requer arquiteturas de aplicação que suportem processamento distribuído.
Exemplo: Aumentar o número de instâncias de um servidor web de 2 para 5.

### 4.3 Elasticidade:

A elasticidade vai além da escalabilidade, oferecendo ajustes automáticos e dinâmicos baseados na demanda em tempo real.

#### - Características:
- Monitoramento contínuo de métricas de performance (CPU, memória, tráfego de rede).
- Regras de auto-scaling que definem quando adicionar ou remover recursos.
- Capacidade de responder rapidamente a picos de tráfego imprevistos.
- Otimização de custos ao reduzir recursos durante períodos de baixa demanda.

#### - Implementação:
- Uso de grupos de auto-scaling que gerenciam conjuntos de recursos.
- Integração com balanceadores de carga para distribuir tráfego entre recursos elásticos.
- Políticas de escalabilidade baseadas em tempo ou métricas de performance.

### 4.4 Agilidade:

A agilidade na nuvem refere-se à capacidade de provisionar e configurar recursos rapidamente, acelerando o desenvolvimento e implantação de aplicações.

#### - Características:
- Provisionamento rápido de recursos através de interfaces web ou APIs.
- Uso de templates e infraestrutura como código para configuração consistente.
- Capacidade de experimentar e iterar rapidamente com novos serviços e arquiteturas.
- Redução do tempo entre a concepção e a implementação de novos recursos ou aplicações.

#### - Benefícios:
- Aceleração do time-to-market para novos produtos e serviços.
- Facilidade em testar e implementar novas tecnologias.
- Resposta rápida a mudanças nas necessidades do negócio ou do mercado.

### 4.5 Distribuição Geográfica:

A distribuição geográfica de data centers permite melhor desempenho global e conformidade com regulamentações locais.

#### - Vantagens:
- Redução da latência ao servir usuários de diferentes regiões geográficas.
- Maior resiliência contra falhas regionais ou desastres naturais.
- Capacidade de atender a requisitos de soberania de dados e conformidade regulatória.

#### - Implementação:
- Uso de CDNs (Content Delivery Networks) para distribuição eficiente de conteúdo estático.
- Replicação de dados entre regiões para redundância e acesso local.
- Estratégias de geo-routing para direcionar usuários ao data center mais próximo.

### 4.6 Recuperação de Desastres:

Serviços e estratégias para garantir a continuidade do negócio em caso de falhas graves ou catástrofes.

#### - Componentes principais:
##### - Backup: 
Cópias regulares de dados e configurações de sistema.
##### - Replicação de dados: 
Sincronização contínua de dados entre sites primários e secundários.
##### - Failover: 
Capacidade de transferir operações para um site secundário em caso de falha do primário.

#### - Estratégias:
##### - RTO (Recovery Time Objective): 
Tempo máximo aceitável para restaurar um sistema após um desastre.
##### - RPO (Recovery Point Objective): 
Quantidade máxima aceitável de perda de dados medida em tempo.
- Testes regulares de recuperação para garantir a eficácia do plano de DR.

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

Redução de custos devido à eficiência operacional em larga escala.

#### - Como funciona na nuvem:
- Provedores de nuvem operam em escala massiva, permitindo eficiências operacionais significativas.
- Custos de hardware, rede, e operações são distribuídos entre um grande número de clientes.
- Poder de compra dos provedores de nuvem resulta em melhores preços de hardware e energia.

#### - Benefícios para clientes:
- Acesso a tecnologias e níveis de serviço que seriam proibitivamente caros para implementar individualmente.
- Preços competitivos que diminuem ao longo do tempo à medida que a eficiência do provedor aumenta.
- Capacidade de aproveitar recursos de nível empresarial sem o investimento inicial correspondente.

## Serviços Principais do Azure

### 6.1 Computação:

#### - VMs (Máquinas Virtuais):
- Servidores virtualizados que emulam hardware físico.
- Flexibilidade para escolher SO, configuração de hardware e software.
- Ideal para migração lift-and-shift de aplicações existentes.
- Opções de VMs otimizadas para computação, memória, armazenamento ou GPU.

#### - Containers:
- Ambientes isolados e leves para execução de aplicações.
- Encapsulam aplicação e suas dependências.
- Inicialização rápida e consumo eficiente de recursos.
- Portabilidade entre diferentes ambientes de desenvolvimento e produção.

#### - Kubernetes Service (AKS):
- Plataforma gerenciada para orquestração de containers.
- Automatiza implantação, escalonamento e gerenciamento de aplicações containerizadas.
- Integração com ferramentas de CI/CD e monitoramento do Azure.
- Suporte a deployments complexos, incluindo canary releases e blue-green deployments.

### 6.2 Rede:

#### - Virtual Network:
- Redes privadas isoladas na nuvem Azure.
- Permite segmentação de recursos em subnets.
- Controle granular sobre tráfego de rede usando Network Security Groups (NSGs).
- Suporte a peering de VNet para conectar redes virtuais.

#### - Load Balancer:
- Distribui tráfego de entrada entre múltiplos recursos.
- Suporte a balanceamento de carga de Camada 4 (TCP, UDP).
- Opções para balanceamento interno (dentro da VNet) ou público (internet-facing).
- Recursos avançados como sessão persistente e health probes.

#### - VPN Gateway:
- Estabelece conexões seguras entre redes on-premises e Azure.
- Suporte a VPNs site-to-site e point-to-site.
- Opções de criptografia e protocolos (IKEv2, OpenVPN).
- Integração com ExpressRoute para conexões dedicadas de alta velocidade.

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
