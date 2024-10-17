
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

#### 6.3.1 Serviços de armazenamento

##### - Blob Storage: 
- Otimizado para armazenamento massivo de dados não estruturados (texto ou binários).
- Ideal para: imagens, vídeos, backups, big data.
- Três tipos: Block Blobs, Page Blobs, e Append Blobs.

##### - Disco do Azure:
- Fornece discos virtuais para VMs e aplicativos.
- Tipos: HDD Standard, SSD Standard, SSD Premium, Ultra Disks.
- Suporta discos gerenciados e não gerenciados.

##### - Fila do Azure:
- Armazenamento de mensagens para comunicação assíncrona.
- Capacidade de até 64 KB por mensagem.
- Útil para desacoplar componentes de aplicações.

##### - Arquivos do Azure:
- Compartilhamento de arquivos de rede totalmente gerenciado.
- Usa protocolo SMB (Server Message Block).
- Pode ser montado simultaneamente por implantações na nuvem e on-premises.

##### - Tabelas do Azure:
- Armazenamento NoSQL para dados estruturados não relacionais.
- Design sem esquema para flexibilidade.
- Acesso rápido usando chave/atributo.

#### 6.3.2 Opções de redundância

##### - LRS (Locally Redundant Storage):
- 3 cópias dos dados em um único data center.
- 11 noves de durabilidade.

##### - ZRS (Zone-Redundant Storage):
- 3 cópias em zonas de disponibilidade separadas na mesma região.
- Proteção contra falhas de data center.

##### - GRS (Geo-Redundant Storage):
- 6 cópias: 3 na região primária (LRS) e 3 na região secundária.
- 16 noves de durabilidade.

##### - GZRS (Geo-Zone-Redundant Storage):
- Combina ZRS na região primária com replicação para uma região secundária.
- Máxima proteção e disponibilidade.

#### 6.3.3 Gerenciamento e migração de arquivos

##### - AzCopy:
- Utilitário de linha de comando.
- Para copiar blobs ou arquivos de/para conta de armazenamento.
- Suporta sincronização unidirecional.

##### - Gerenciador de Armazenamento do Azure:
- Interface gráfica (similar ao Windows Explorer).
- Compatível com Windows, MacOS e Linux.
- Gerencia múltiplos tipos de armazenamento.

##### - Sincronização de Arquivos do Azure:
- Sincronização bidirecional entre Azure e servidores on-premises.
- Suporta "cloud tiering" para otimizar espaço local.

#### 6.3.4 Armazenamento: domínio de objetivo

##### 6.3.4.1 Comparação dos serviços de armazenamento do Azure

- Cada serviço (Blob, Disk, File, Queue, Table) tem casos de uso específicos.
- Diferem em estrutura de dados, latência, e capacidade.

##### 6.3.4.2 Camadas de armazenamento

###### - Hot: 
- Para dados acessados frequentemente.
###### - Cool: 
- Para dados acessados com menos frequência (pelo menos 30 dias).
###### - Archive: 
- Para dados raramente acessados (pelo menos 180 dias).

##### 6.3.4.3 Opções de conta de armazenamento

###### - Standard General-purpose v2: 
- Para maioria dos cenários.
###### - Premium block blobs: 
- Para alto desempenho em blobs.
###### - Premium file shares: 
- Para compartilhamentos de arquivos de alto desempenho.
###### - Premium page blobs: 
- Para discos de VM de alto desempenho.

##### 6.3.4.4 Opções de migração

###### - Migrações para Azure:
- Plataforma unificada para migração.
- Ferramentas integradas para avaliação e migração.
- Suporta migrações de servidores, bancos de dados, e aplicações web.

###### - Azure Data Box:
- Para transferências offline de grandes volumes de dados (até 80 TB).
- Útil para backups, migração inicial, ou retorno de dados do Azure.
- Seguro e robusto para transporte físico.

##### 6.3.5 Contas de Armazenamento

- Requerem nome globalmente único.
- Fornecem acesso mundial via internet.
- Determinam serviços disponíveis e opções de redundância.

##### 6.3.6 Pontos de extremidade públicos do serviço de armazenamento

- Cada serviço (blob, file, queue, table) tem um endpoint único.
- Formato geral: https://..core.windows.net

##### 6.3.7 Migrações para o Azure

- Avaliação de ambiente on-premises.
- Planejamento e execução de migração.
- Suporte a diversos cenários de migração.

##### 6.3.8 Opções de gerenciamento de arquivos

- AzCopy: Para operações em lote e scripts.
- Gerenciador de Armazenamento: Para operações visuais e exploração.
- Sincronização de Arquivos: Para manter consistência entre on-premises e nuvem.

### 6.4 Banco de Dados:

- SQL Database: Banco de dados relacional totalmente gerenciado
- Cosmos DB: Banco de dados multi-modelo globalmente distribuído
- MySQL: Versão gerenciada do MySQL para Azure

### 6.5 Identidade, Acesso e Segurança:

#### 6.5.1 Microsoft Entra ID (anteriormente Azure Active Directory)

Serviço de gerenciamento de identidades e acesso baseado em nuvem.

##### 6.5.1.1 Principais funcionalidades:

###### Autenticação: 
Verifica identidades para acesso a recursos.
###### Logon único (SSO): 
Permite acesso a múltiplos aplicativos com uma única autenticação.
###### Gerenciamento de aplicativos: 
Controla acesso e políticas para aplicativos corporativos.
###### Business-to-Business (B2B): 
Facilita colaboração segura com parceiros externos.
###### Gerenciamento de dispositivos: 
Integra controle de acesso baseado em dispositivos.

#### 6.5.2 Microsoft Entra Domain Services

- Fornece serviços de domínio gerenciados na nuvem.

##### 6.5.2.1 Benefícios:

- Elimina necessidade de gerenciar controladores de domínio.
- Suporta aplicativos legados que requerem autenticação tradicional.
- Sincronização automática com Microsoft Entra ID.

#### 6.5.3 Métodos de Autenticação

##### 6.5.3.1 SSO (Single Sign-On):

- Permite acesso a múltiplos aplicativos com uma única autenticação.
- Melhora experiência do usuário e segurança.

##### 6.5.3.2 MFA (Autenticação Multifator):

Requer dois ou mais elementos para autenticação completa:

- Algo que você sabe (senha)
- Algo que você possui (telefone)
- Algo que você é (biometria)

##### 6.5.3.3 Autenticação sem senha:

- Utiliza métodos como Windows Hello, FIDO2 security keys, ou Microsoft Authenticator.

#### 6.5.4 Identidades Externas e Acesso de Convidado

##### 6.5.4.1 B2B do Microsoft Entra External ID:

- Permite colaboração segura com parceiros externos.
- Usuários externos acessam recursos com suas próprias credenciais.

##### 6.5.4.2 B2C do Identidades Externas do Azure AD:

- Gerencia identidades e acesso para clientes.
- Personalização de experiências de login e registro.

#### 6.5.5 Acesso Condicional do Entra

- Ferramenta para tomar decisões de acesso baseadas em múltiplos fatores:
- Associação de usuário ou grupo
- Localização do IP
- Dispositivo
- Aplicativo
- Detecção de risco

#### 6.5.6 Controle de Acesso Baseado em Função (RBAC)

- Gerenciamento de acesso granular.
- Permite atribuir permissões específicas baseadas em funções.
- Aplicável no portal Azure e no controle de recursos.

#### 6.5.7 Conceito de Confiança Zero

Princípio de "nunca confiar, sempre verificar".

##### 6.5.7.1 Elementos-chave:

- Verificar explicitamente
- Usar acesso com privilégio mínimo
- Assumir violação

#### 6.5.8 Modelo de Defesa em Profundidade

Abordagem em camadas para segurança.

##### 6.5.8.1 Múltiplos níveis de proteção:

- Segurança física
- Identidade e acesso
- Perímetro
- Rede
- Computação
- Aplicação
- Dados

#### 6.5.9 Microsoft Defender para Nuvem

Serviço de monitoramento de segurança para Azure e ambientes on-premises.

##### 6.5.9.1 Funcionalidades:

- Fornece recomendações de segurança.
- Detecta e bloqueia malware.
- Analisa e identifica potenciais ataques.
- Oferece controle de acesso just-in-time para portas.

#### 6.5.10 Autenticação vs. Autorização

##### 6.5.10.1 Autenticação:

- Identifica quem está tentando acessar um recurso.
- Verifica credenciais legítimas.

##### 6.5.10.2 Autorização:

- Determina o que um usuário autenticado pode fazer.
- Define níveis de acesso e permissões.

##### 6.6 Segurança:

###### - Key Vault: 
Gerenciamento seguro de chaves criptográficas e segredos

###### - DDoS Protection: Proteção contra ataques de negação de serviço distribuído


## Gerenciamento e Governança

### 7.1 Gerenciamento de Custos

Fatores que afetam os custos no Azure:

#### 7.1.1 Tipo de recurso:

##### - Computação: 
VMs cobradas por segundo de uso, com preços variando por tamanho e sistema operacional.
##### - Armazenamento: 
Cobrado por GB armazenado, com preços diferentes para Hot, Cool e Archive tiers.
##### - Rede: 
Custos para transferência de dados, IP público, VPN Gateway, etc.

#### 7.1.2 Consumo:

##### - Modelo pay-as-you-go: 
Cobra apenas pelos recursos utilizados.
##### - Exemplo: 
Uma VM ligada 24/7 custará mais que uma ligada apenas 8 horas por dia.

#### 7.1.3 Manutenção:

- Custos indiretos como tempo de equipe para gerenciamento.
- Ferramentas de monitoramento e diagnóstico (ex: Azure Monitor).

#### 7.1.4 Área Geográfica:

- Preços variam significativamente entre regiões.
##### Exemplo: 
Serviços na região Leste dos EUA geralmente são mais baratos que na Europa Ocidental.

#### 7.1.5 Tráfego de Rede:

- Ingress (entrada de dados) geralmente gratuito.
- Egress (saída de dados) cobrado por GB, com taxas variando por região.

#### 7.1.6 Assinatura:

##### - Enterprise Agreement: 
Preços negociados para grandes volumes.
##### Pay-As-You-Go: 
Preços padrão de varejo.
##### CSP (Cloud Solution Provider): 
Preços definidos pelo parceiro.

### 7.2 Calculadora de Preços

- Interface web interativa para estimar custos.
- Permite configurar detalhes específicos:
- Tipo de instância de VM (ex: D2s v3, F4s v2).
- Horas de operação por mês.
- Sistema operacional (Windows ou Linux).
- Opções de licenciamento (PAYG ou Hybrid Benefit).
- Fornece estimativas detalhadas, incluindo custos mensais e anuais.

### 7.3 Calculadora de TCO (Total Cost of Ownership)

- Compara custos on-premises vs. Azure ao longo de um período (geralmente 3-5 anos).

#### Inputs incluem:

##### - Servidores: 
Quantidade, especificações, utilização.
##### - Bancos de dados: Tipo (SQL, Oracle), tamanho.
##### - Armazenamento: 
Capacidade, tipo (SAN, NAS).
##### - Rede: 
Largura de banda de saída.

#### Outputs:

- Comparação lado a lado de custos on-premises vs. Azure.
- Detalhamento por categoria (computação, armazenamento, rede, mão de obra).

### 7.4 Ferramenta de Gerenciamento de Custos do Azure

#### Relatórios:
- Visualizações detalhadas de gastos por serviço, recurso, tag.
- Análises de tendências ao longo do tempo.

####Enriquecimento de Dados:
- Adiciona metadados como centro de custo, projeto.
- Permite alocação de custos compartilhados.

#### Orçamentos:
- Define limites de gastos por assinatura, grupo de recursos ou serviço.
- Pode ser configurado para reset mensal, trimestral ou anual.

#### Alertas:
- Notificações por email ou integração com Azure Action Groups.
- Configurável para diferentes níveis (ex: 80%, 100% do orçamento).

#### Recomendações:
- Identifica VMs subutilizadas.
- Sugere compra de instâncias reservadas.
- Recomenda mudança para tiers de armazenamento mais econômicos.

### 7.5 Marcas (Tags)

#### - Formato: 
chave:valor (ex: "Departamento:Marketing").
- Limite de 50 tags por recurso.

#### - Usos avançados:
##### - Automação: 
Usar tags para acionar Azure Automation runbooks.
##### - Políticas: 
Enforçar tagging obrigatório via Azure Policy.
##### - RBAC: 
Controlar acesso baseado em tags.

### 7.6 Azure Marketplace

#### Tipos de ofertas:
- Soluções SaaS.
- Imagens de VM pré-configuradas.
- Containers.
- Serviços de consultoria.

#### - Processo de publicação rigoroso:
- Verificação de segurança.
- Testes de compatibilidade.
- Revisão de documentação.

#### - Modelos de preços:
- PAYG (Pay-As-You-Go).
- Licenças trazidas pelo cliente (BYOL).
- Versões de avaliação gratuitas.

### Considerações Adicionais

#### Otimização de Custos:

##### Azure Advisor: 
Fornece recomendações personalizadas.
##### Azure Reservations: 
Desconto significativo para compromissos de 1 ou 3 anos.
##### Spot VMs: 
VMs com grande desconto, mas que podem ser desalocadas a qualquer momento.

#### Governança:

##### Azure Policy: 
Define e enforça regras para recursos (ex: regiões permitidas, SKUs de VM).
##### Management Groups: 
Organiza assinaturas em hierarquias para aplicação de políticas e RBAC.
##### Blueprints: 
Define conjuntos repetíveis de recursos que aderem aos padrões organizacionais.

#### Monitoramento Contínuo:
##### Azure Monitor: 
Coleta e analisa telemetria de aplicações e infraestrutura.
##### Log Analytics: 
Ferramenta para consulta e análise de logs.
##### Application Insights: 
Monitoramento e diagnóstico específico para aplicações web.

#### Planejamento Financeiro:

##### Forecasting: 
Usa machine learning para prever gastos futuros baseado em padrões históricos.
##### Chargeback e Showback: 
Alocação de custos para unidades de negócio internas.
##### FinOps: 
Prática de otimização contínua de custos em colaboração entre equipes financeiras e técnicas.

### 8.1 Governança e Conformidade no Azure

#### 8.1.1  Azure Policy

Azure Policy é uma ferramenta crucial para manter o controle e a conformidade em ambientes Azure.

##### 8.1.1.1 Características principais:

- Impõe regras e efeitos sobre os recursos.
- Avalia recursos existentes para conformidade com políticas.
- Fornece relatórios de conformidade.

##### 8.1.1.2 Funcionalidades:

###### - Definições de Política:
Regras predefinidas ou personalizadas.
####### Exemplos: 
regiões permitidas, SKUs de VM permitidos, tags obrigatórias.

###### Iniciativas:
- Agrupamentos de políticas relacionadas.
- Facilita o gerenciamento de múltiplas políticas.

###### Atribuições:
- Aplica políticas ou iniciativas a escopos específicos (assinaturas, grupos de recursos).

###### Efeitos:
####### - Deny: 
Bloqueia a criação/modificação de recursos não conformes.
####### - Audit: 
Permite a criação, mas marca como não conforme.
####### - Append: 
Adiciona informações ao recurso (ex: tags).
####### - DeployIfNotExists: 
Cria recursos relacionados automaticamente.

###### Conformidade:
- Avaliação regular de recursos.
- Dashboards e relatórios de conformidade.

##### Benefícios:

- Consistência na configuração de recursos.
- Aplicação de padrões de segurança e conformidade regulatória.
- Controle de custos (ex: limitando SKUs caros).
- Governança em larga escala.

#### 8.1.2 Bloqueios de Recurso

Bloqueios de recurso são uma camada adicional de proteção contra modificações ou exclusões acidentais.

##### 8.1.2.1 Tipos de bloqueio:

###### CanNotDelete (Excluir):
- Permite leitura e modificação.
- Impede exclusão do recurso.

###### ReadOnly (Leitura):
- Permite apenas leitura.
- Impede modificações e exclusões.

##### 8.1.2.2 Características:

###### Aplicáveis em diferentes níveis: 
assinatura, grupo de recursos, recurso individual.
###### Herança: 
Bloqueios em níveis superiores são herdados por recursos abaixo.
###### Permissões: 
Requer privilégios de "Proprietário" ou "Administrador de Acesso do Usuário" para gerenciar bloqueios.

##### 8.1.2.3 Uso comum:

- Proteção de recursos críticos.
- Garantia de continuidade de serviços essenciais.
- Imposição de políticas de governança.

##### 8.1.2.4 Considerações:

- Podem ser contornados por usuários com permissões adequadas.
- Não substituem RBAC (Controle de Acesso Baseado em Função).
- Afetam todas as operações, incluindo automações.

#### 8.1.3 Portal de Confiança do Serviço

O Portal de Confiança do Serviço é um recurso centralizado para informações de conformidade, segurança e privacidade da Microsoft.

##### 8.1.3.1 Conteúdo:

###### Relatórios de auditoria e certificações:
ISO, SOC, PCI DSS, etc.
###### Documentação de conformidade:
Detalhes sobre como os serviços Microsoft atendem a diferentes regulamentações.
###### Mapeamentos de controle:
Como os controles de segurança da Microsoft se alinham com padrões da indústria.
###### Informações de privacidade e proteção de dados:
Políticas e práticas de proteção de dados da Microsoft.
###### Recursos adicionais:
White papers, FAQs, estudos de caso.

##### 8.1.3.2 Benefícios:

- Transparência sobre práticas de segurança e conformidade da Microsoft.
- Facilita demonstrações de conformidade para auditores e reguladores.
- Acesso a informações atualizadas sobre conformidade de serviços em nuvem.

#### 8.1.4 Microsoft Purview

Microsoft Purview é uma solução abrangente para governança de dados e conformidade.

##### 8.1.4.1 Principais componentes:

###### Mapa de Dados:
- Descoberta automatizada de dados em múltiplas fontes.
- Criação de catálogo de dados unificado.
- Classificação e Rotulagem:
- Identificação automática de dados sensíveis.
- Aplicação de rótulos de sensibilidade.

###### Linhagem de Dados:
- Rastreamento da origem e transformações dos dados.
- Visualização de fluxos de dados end-to-end.

###### Gerenciamento de Políticas:
- Definição e aplicação de políticas de governança de dados.
- Monitoramento de conformidade.

###### Insights e Relatórios:
- Dashboards para visibilidade do estado de governança.
- Relatórios de conformidade e riscos.

##### Funcionalidades adicionais:

- Integração com Azure Synapse Analytics para análise de dados.
- Conexão com fontes de dados on-premises e multi-cloud.
- Suporte a regulamentações como GDPR, CCPA, HIPAA.

#### Benefícios:

- Visão unificada de dados em ambientes heterogêneos.
- Melhoria na qualidade e confiabilidade dos dados.
- Facilitação da conformidade regulatória.
- Aprimoramento da segurança de dados.

## Ferramentas de Gerenciamento e Implantação no Azure

### 9.1 Portal do Azure

#### 9.1.1 Características avançadas:

- Suporte a múltiplos idiomas e localidades.
- Integração com Azure Monitor para visualizações de métricas em tempo real.
- Resource Graph Explorer para consultas complexas em recursos.
- Cloud Shell integrado para operações rápidas de CLI/PowerShell.

#### 9.1.2 Personalizações:

- Criação de dashboards personalizados com widgets customizáveis.
- Favoritos e atalhos para rápido acesso a recursos frequentemente usados.
- Temas escuro e claro para preferência visual.

#### 9.1.3 Segurança:

- Suporte a autenticação multifator (MFA).
- Logs de atividade detalhados para auditoria.
- Integração com Azure AD para controle de acesso baseado em roles (RBAC).

### 9.2 Azure Cloud Shell

#### 9.2.1 Azure CLI:

- Sintaxe consistente: 'az '
- Extensões para funcionalidades adicionais (ex: azure-devops, databricks)
- Modo interativo para exploração de comandos e parâmetros.

#### 9.2.2 Azure PowerShell:

- Cmdlets seguem padrão 'Verb-AzNoun' (ex: Get-AzVM, New-AzResourceGroup)
- Suporte a PowerShell Remoting para gerenciamento remoto.
- Módulos específicos para diferentes serviços Azure (Az.Compute, Az.Storage, etc.)

#### 9.2.3 Características avançadas do Cloud Shell:

- Integração com VSCode para desenvolvimento remoto.
- Suporte a ferramentas adicionais como kubectl, Terraform, Ansible.
- Personalização do ambiente com .bashrc ou $profile.

### 9.3 Azure Arc

#### 9.3.1 Cenários de uso avançado:

- Gerenciamento de conformidade em ambientes multi-cloud.
- Implementação de políticas de segurança consistentes em ambientes híbridos.
- Execução de Azure Functions em ambientes edge.

#### 9.3.2 Azure Arc Data Services:

##### - SQL Managed Instance: 
SQL Server como serviço gerenciado em qualquer infraestrutura.
##### - PostgreSQL Hyperscale: 
Banco de dados PostgreSQL escalável em ambientes híbridos.

#### 9.3.3 Integrações:

- Azure Policy para governança consistente.
- Azure Monitor e Log Analytics para monitoramento unificado.
- Azure Sentinel para segurança em ambientes híbridos.

### 9.4 Azure Resource Manager (ARM)

#### 9.4.1 Funcionalidades avançadas:

- Suporte a implantações incrementais e completas.
- Uso de funções e expressões para lógica complexa em modelos.
- Linked templates para modularização de implantações grandes.

#### 9.4.2 Segurança:

- Integração com Azure Key Vault para gerenciamento seguro de segredos.
- Uso de managed identities para autenticação segura de recursos.

#### 9.4.3 Governança:

##### - Policy as Code: 
Definição e aplicação de políticas Azure via ARM.
##### - Blueprints: Orquestração de implantações complexas com conformidade.

### 9.5 Modelos ARM

#### 9.5.1 Técnicas avançadas:

- Uso de variáveis e parâmetros para flexibilidade.
- Loops e condicionais para implantações dinâmicas.
- Nested templates para estruturação complexa.
- Output para passagem de informações entre templates.

#### 9.5.2 Melhores práticas:

- Uso de arquivos de parâmetros para diferentes ambientes.
- Implementação de naming conventions consistentes.
- Testes automatizados com ARM TTK (Template Test Kit).

#### 9.5.3 Integração com DevOps:

- Uso em pipelines de CI/CD para implantação contínua.
- Armazenamento em repositórios de código para versionamento.

### 9.6 Bicep

#### 9.6.1 Recursos avançados:

- Decorators para extensão de funcionalidades (ex: @allowed(), @description()).
- Modules para reutilização de código e organização.
- Integração nativa com Azure Policy as Code.

#### 9.6.2 Ferramentas de desenvolvimento:

- Bicep Playground para testes rápidos online.
- Extensão VSCode com intellisense e validação em tempo real.
- Bicep decompiler para converter JSON ARM para Bicep.

#### 9.6.3 Melhores práticas:

- Uso de symbolic names para melhor legibilidade.
- Implementação de loops e condicionais para implantações dinâmicas.
- Utilização de targetScope para definir escopo de implantação.
- Infraestrutura como Código (IaC) - Considerações Avançadas

#### 9.6.4 Padrões de implementação:

- Imutabilidade: Criar novos recursos em vez de modificar existentes.
- Idempotência: Garantir resultados consistentes em execuções repetidas.
- Separação de preocupações: Dividir configurações por função ou serviço.

#### 9.6.5 Gestão de estados:

- Uso de backends remotos (ex: Azure Storage) para armazenar estados do Terraform.
- Implementação de estratégias de lock para prevenir conflitos em equipes.

#### 9.6.6 Testes e validação:

- Unit testing de módulos IaC.
- Integration testing com implantações em ambientes de sandbox.
- Uso de ferramentas como Terratest para automação de testes.

#### 9.6.7 Segurança em IaC:

- Scanning de código para detecção de má configurações de segurança.
- Implementação de least privilege principle em todas as implantações.
- Uso de ferramentas como Checkov para análise estática de segurança.

## Ferramentas de Gerenciamento do Azure

As ferramentas de gerenciamento do Azure formam um ecossistema robusto para monitorar, otimizar e manter a saúde dos recursos e serviços Azure. O Assistente do Azure oferece recomendações proativas, a Integridade do Serviço fornece visibilidade do status operacional, e o Azure Monitor oferece insights profundos através de coleta e análise de telemetria. Juntas, essas ferramentas permitem uma gestão eficiente e eficaz de ambientes Azure, desde pequenas implantações até grandes infraestruturas empresariais.

### 10.1 Assistente do Azure

O Assistente do Azure é uma ferramenta proativa de análise e otimização que fornece recomendações personalizadas para melhorar as implantações do Azure.

#### 10.1.1 Principais características:

- Análise contínua dos recursos implantados.
- Recomendações baseadas em práticas recomendadas da Microsoft.

##### Foco em cinco áreas críticas:
- Confiabilidade:
- Garante alta disponibilidade e resiliência dos sistemas.
- Recomendações para backup, redundância e recuperação de desastres.

##### Segurança:
- Identifica vulnerabilidades e sugere melhorias.
- Recomendações para configurações de firewall, criptografia e políticas de acesso.

###### Desempenho:
- Otimiza a velocidade e eficiência dos recursos.
- Sugestões para dimensionamento adequado de VMs, configurações de cache, etc.

##### Custo:
- Identifica oportunidades de economia.
- Recomendações para recursos subutilizados, reservas e opções de licenciamento.

##### Excelência Operacional:
- Melhora a eficiência operacional.
- Sugestões para automação, monitoramento e práticas de DevOps.

#### 10.1.2 Funcionamento:

- Integração nativa com o portal Azure.
- Painéis personalizáveis com visão geral das recomendações.
- Opções para implementar recomendações diretamente ou agendá-las.

#### 10.1.3 Benefícios:

- Redução proativa de riscos e problemas.
- Otimização contínua do ambiente Azure.
- Alinhamento com as melhores práticas do setor.

### 10.2 Integridade do Serviço do Azure

A Integridade do Serviço do Azure é um conjunto de ferramentas que fornecem informações sobre o estado de saúde da infraestrutura Azure e dos serviços individuais.

#### 10.2.1 Componentes principais:

##### Status do Azure:
- Visão global da saúde de todos os serviços Azure.
- Atualizado em tempo real.
- Mostra problemas em todas as regiões do Azure.

##### Integridade do Serviço:
- Foco nos serviços e regiões específicos que você está usando.
- Filtra informações não relevantes para sua infraestrutura.
- Fornece detalhes sobre incidentes e manutenções planejadas.

##### Resource Health:
- Visão personalizada da saúde de recursos individuais.
- Mostra o histórico de saúde de recursos específicos.
- Fornece insights sobre problemas específicos de recursos.

#### 10.2.2 Características:

- Notificações personalizáveis para alertar sobre problemas de serviço.
- Integração com Azure Monitor para correlação com métricas e logs.
- Relatórios de incidentes post-mortem para análise detalhada.

#### 10.2.3 Benefícios:

- Visibilidade em tempo real do status da infraestrutura Azure.
- Capacidade de diferenciar entre problemas do Azure e problemas específicos da aplicação.
- Suporte a SLAs e gerenciamento de incidentes.

### 10.3 Azure Monitor

Azure Monitor é uma plataforma abrangente para coleta, análise e ação sobre dados de telemetria de ambientes de nuvem e on-premises.

#### 10.3.1 Componentes principais:

##### Coleta de Dados:
- Métricas de plataforma: Dados de desempenho de recursos Azure.
- Logs de atividade: Registros de operações realizadas em recursos Azure.
- Logs de recursos: Dados detalhados sobre o funcionamento interno dos recursos.

##### Dados de aplicação: 
Telemetria personalizada de aplicações.

##### Azure Log Analytics:
- Repositório central para todos os logs.
- Poderosa linguagem de consulta (Kusto Query Language - KQL).
- Análises avançadas e visualizações personalizadas.

##### Alertas do Azure Monitor:
- Configuração de regras de alerta baseadas em métricas ou logs.
- Suporte a diferentes tipos de ações (e-mail, SMS, webhooks, etc.).
- Integração com sistemas de gerenciamento de incidentes.

##### Application Insights:
- Monitoramento específico para aplicações web.
- Rastreamento de desempenho, exceções e uso de recursos.
- Mapeamento de dependências e análise de usuários.

#### 10.3.2 Funcionalidades adicionais:

- Dashboards personalizáveis para visualização de dados.
- Integração com Azure Automation para ações corretivas automáticas.
- Suporte a cenários híbridos e multi-cloud.

#### 10.3.3 Benefícios:

- Visibilidade end-to-end da infraestrutura e aplicações.
- Detecção e diagnóstico rápido de problemas.
- Insights acionáveis para otimização de desempenho e custos.

#### 10.3.4 Casos de uso comuns:

- Monitoramento de disponibilidade e desempenho de aplicações.
- Análise de tendências de uso de recursos.
- Troubleshooting de problemas de infraestrutura.
- Planejamento de capacidade baseado em dados históricos.


## Controle de Versão e Colaboração

### 11.1 Git: Sistema de controle de versão distribuído

Mantém histórico completo de alterações no código

#### Principais comandos:

- git init: Inicia um novo repositório
- git clone: Copia um repositório existente
- git add: Adiciona alterações à área de staging
- git commit: Salva as alterações no repositório local
- git push: Envia alterações para um repositório remoto
- git pull: Obtém e mescla alterações de um repositório remoto

###11.2 GitHub: 
Plataforma de hospedagem de código e colaboração

- Facilita a colaboração em projetos open source
- Recursos: Issues, Pull Requests, Actions para CI/CD

### 12.1 Azure DevOps: 
Suite de ferramentas para desenvolvimento e implantação contínuos.

#### Colaboração em Projetos Open Source:

- Fork: Cria uma cópia pessoal de um projeto
- Branch: Desenvolve novas funcionalidades isoladamente
- Pull Request: Propõe alterações para o projeto original
- Code Review: Processo de revisão das alterações propostas
- Merge: Incorporação das alterações aprovadas ao projeto principal

## 13.1 Service Level Agreements (SLAs) 

SLAs são contratos formais entre um provedor de serviços (neste caso, a Microsoft Azure) e o cliente, que definem o nível de serviço esperado em termos de disponibilidade e desempenho.

### 13.2 Funcionamento:

- Estabelecem métricas específicas e mensuráveis para o serviço
- Geralmente expressos em porcentagem de tempo de atividade (por exemplo, 99,9% de disponibilidade)
- Definem compensações ou créditos de serviço caso os níveis acordados não sejam atingidos

### 13.3 Características Principais:

- Uptime Garantido: Porcentagem do tempo em que o serviço estará disponível
- Latência: Tempo de resposta do serviço
- Throughput: Capacidade de processamento de dados
- Suporte: Tempos de resposta para diferentes níveis de severidade de problemas
