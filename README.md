# Design e Arquitetura de Software 2  
> Diogo Mazeika

### Aula 24/02/2025  
**Well-Architect Framework**  
- **Excelência Operacional**  
- **Segurança**  
- **Confiabilidade (Reliability)**  
- **Eficiência em Performance**  
- **Otimização de Custos**  
- **Sustentabilidade**

---

### Aula 27/02/2025  
**Conceitos Abordados:**  
- **Trade-off:**  
  - Escolher entre linguagens e abordagens de acordo com a necessidade (consistência, durabilidade, espaço) com base em dados empíricos.
- **Escalabilidade/Elasticidade:**  
  - Garantir que a aplicação suporte alta demanda.
- **Automatização para Auto-escalabilidade:**  
  - Automatizar processos e recursos para agilizar a resposta da aplicação.
- **Infraestrutura como Código (IaC):**  
  - Definir a infraestrutura via código, reduzindo erros de configuração e propagando mudanças de forma uniforme.
- **Recursos Descartáveis:**  
  - Tratar todos os recursos como temporários, facilitando substituição e manutenção.
- **Baixo Acoplamento e Design de Serviços:**  
  - Priorizar a criação de serviços (em vez de servidores) que possam funcionar de forma independente, facilitando a escolha do banco de dados adequado e evitando pontos únicos de falha.

*Exemplo prático:*  
Uso de Elastic Load Balancing (ELB) para permitir a substituição fácil de bancos de dados e garantir disponibilidade.

---

### Aula 06/03/2025  
**Tópicos Abordados:**  
- **Acoplamento:**  
  - *Anti-pattern:* Banco de dados com alto acoplamento.  
  - *Best practice:* Bancos que podem ser substituídos facilmente com o uso de ELB.
- **Arquiteto Frugal:**  
  - Profissional que prioriza a otimização de custos.
- **Segurança:**  
  - Uso de serviços gerenciados (como na AWS).  
  - Registro de acesso aos recursos.  
  - Isolamento das partes da infraestrutura.  
  - Criptografia e autenticação com múltiplos fatores.

---

### Aula 10/03/2025  
**Infraestrutura Global da AWS e Segurança:**  
- **Pontos de Presença (POPs) e Edge Locations:**  
  - Entrega de conteúdo com latência mínima.
- **Regional Cache:**  
  - Pontos intermediários para melhorar a performance na entrega dos dados.
- **Segurança e Modelo de Responsabilidade Compartilhada:**  
  - Separação de responsabilidades: a AWS cuida da infraestrutura física, enquanto o usuário gerencia sistemas, senhas e aplicações.
- **Princípio do Privilégio Mínimo e Uso de Roles:**  
  - Conceder apenas as permissões necessárias e usar roles para acesso temporário seguro.

---

### Aula 13/03/2025  
**Identity and Access Management (IAM):**  
- **Gerenciamento de Usuários:**  
  - Controle de acesso via console e acesso programático.
- **Autenticação e Autorização:**  
  - Ativação de MFA (autenticação multifatorial) e rotação de credenciais.
- **Modelo de Responsabilidade Compartilhada:**  
  - AWS cuida do hardware; você gerencia o software e as configurações.

---

### Aula 17/03/2025  
**Controle de Acesso e Armazenamento:**  
- **RBAC – Role Base Access Control:**  
  - Definição de políticas de acesso segundo o papel do usuário.
- **IAM Policies:**  
  - Determinação de permissões para acesso a recursos específicos.
- **Tipos de Armazenamento na AWS:**  
  - *Block Storage (EBS), File Storage (EFS ou FSx) e Object Storage (S3).*  
- **Amazon S3:**  
  - Conceitos de buckets, versionamento, lifecycle policies, CORS e criptografia.  
  - Criação de URLs pré-assinadas para acesso temporário.

---

### Aula 24/03/2025  
**Gerenciamento do S3:**  
- **Ciclo de Vida (Lifecycle Policies):**  
  - Regras de transição de classes e expiração de objetos.
- **S3 Versionamento:**  
  - Protege objetos contra sobregravações.
- **CORS e Consistência de Dados:**  
  - Configuração de headers e regras para o compartilhamento seguro de recursos.
- **Criptografia:**  
  - Implementação server-side e client-side para segurança dos dados.

---

### Aula 27/03/2025  
**Prática e Custos:**  
- **Códigos S3:**  
  - Exemplos práticos e testes com Python para conexão e manipulação de buckets.
- **Modelo de Custos da AWS:**  
  - "Pay for what you use" – o usuário paga somente pelos recursos efetivamente consumidos.

---

### Aula 03/04/2025  
**Computing:**  
- **EC2 (Elastic Compute Cloud):**  
  - Hospedagem e gerenciamento de servidores virtuais.
- **EBS (Elastic Block Storage):**  
  - Armazenamento persistente, diferenciado das instâncias temporárias.
- **AMI (Amazon Machine Image):**  
  - Imagem do servidor para criação de cópias idênticas e recuperação de sistemas.

---

### Aula 07/04/2025  
**Avanços em EC2 e Estratégias de Compra:**  
- **Placement Strategies:**  
  - Cluster, Spread e Partition para posicionamento físico dos recursos.
- **Modelos de Compra da EC2:**  
  - On-demand, reserved, savings plans e spot – opções adequadas a diferentes necessidades.

---

### Aula 10/04/2025  
**Bancos de Dados com RDS:**  
- **RDS (Relational Database Service):**  
  - Gerenciamento de bancos de dados relacionais e não relacionais.
- **Critérios de Escolha:**  
  - Decisões baseadas em requisitos de escalabilidade, performance e custo.

---

## Segundo Bimestre

### Aula 05/05/2025  
- **VPC (Virtual Private Cloud):**
  - Criação de uma rede virtual isolada na AWS, permitindo controle total de endereçamento e roteamento.  
- **CIDR (Classless Inter-Domain Routing):**
  - Planejamento flexível de blocos de endereços IP sem as limitações de classes tradicionais.  
- **Subnet Pública:**
  - Definição de sub-redes com rota para Internet Gateway, viabilizando o acesso público de recursos.

---

### Aula 19/05/2025  
- **VPC Peering:**
  - Conexão privada entre duas VPCs para roteamento direto de tráfego sem passar pela internet.  
- **AWS VPN Site-to-Site:**
  - Estabelecimento de túnel VPN IPSec entre rede on-premises e VPC, garantindo criptografia ponta a ponta.  
- **AWS Direct Connect:**
  - Link de rede dedicado de alta largura de banda e baixa latência entre data center local e AWS.

---

### Aula 26/05/2025  
- **IAM Groups:**
  - Agrupamento de usuários para gerenciamento coletivo de permissões e políticas.  
- **Roles – AWS STS (Security Token Service):**
  - Emissão de credenciais temporárias para assumir papéis com permissões específicas.  
- **AWS Cognito:**
  - Serviço de identidade e autenticação para aplicações web e mobile, suportando usuários e grupos.

---

### Aula 29/05/2025  
- **Criptografia Simétrica:**
  - Uso de uma única chave para cifrar e decifrar dados (ex.: AES), eficiente mas requer gestão segura das chaves.  
- **Criptografia Assimétrica:**
  - Par de chaves pública/privada (ex.: RSA), permitindo troca segura de chaves e assinaturas digitais.


🤠
