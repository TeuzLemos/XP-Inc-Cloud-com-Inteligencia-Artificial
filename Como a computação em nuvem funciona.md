# Como a Computação em Nuvem Funciona

## Modelos de Implantação de Infraestrutura de TI

Este documento reúne conceitos e detalhes essenciais sobre **On-Premise**, **Computação em Nuvem** e **Modelo Híbrido**, para facilitar seus estudos e servir como material de consulta.

---

### 1. On-Premise (Infraestrutura Local)

**Descrição:**

- Infraestrutura de TI instalada e operada dentro das dependências da própria organização. Inclui servidores físicos, storage, redes, sistemas operacionais e software gerenciados internamente.

**Características Principais:**

- **Controle Total:** Hardware e software são de propriedade da empresa.
- **Propriedade de Dados:** Dados sensíveis armazenados localmente.
- **Modelos de Custo:** Principalmente CAPEX (investimento de capital) para aquisição de equipamentos.
- **Manutenção e Suporte:** Equipe interna responsável por atualizações, backup e segurança física.

**Vantagens:**

- Controle completo sobre configuração e políticas de segurança.
- Desempenho dedicado, sem latência de conexão externa.
- Indicado para requisitos regulatórios rígidos (LGPD, SOX, PCI-DSS).

**Desvantagens:**

- Alto investimento inicial e custos com depreciação de hardware.
- Escalabilidade limitada – expansão requer compra de novos equipamentos.
- Manutenção contínua e necessidade de equipe especializada.

**Exemplos de Uso:**

- Sistemas bancários críticos.
- Ambientes com dados de saúde protegidos (prontuários eletrônicos).
- Data centers corporativos para aplicações legadas.

**Quando Escolher:**

- Organizações com altos requisitos de conformidade e latência.
- Ambientes que demandam customizações intensivas de segurança.

---

### 2. Computação em Nuvem (Cloud)

**Descrição:**

- Infraestrutura de TI provida por provedores externos (AWS, Azure, Google Cloud, etc.), acessada pela internet em modelo de serviço.

**Modelos de Serviço (Eixos de Serviço):**

- **IaaS (Infrastructure as a Service):** Servidores, storage e redes virtualizados (ex.: Amazon EC2, Azure VM).
- **PaaS (Platform as a Service):** Plataforma gerenciada para desenvolvimento e deploy de aplicações (ex.: AWS Elastic Beanstalk, Azure App Service).
- **SaaS (Software as a Service):** Aplicações prontas para uso (ex.: Office 365, Salesforce).

**Características Principais:**

- **OPEX (Custo Operacional):** Pagamento conforme uso.
- **Elasticidade:** Escala automática de recursos.
- **Alta Disponibilidade:** SLA garantido pelo provedor.
- **Manutenção Delegada:** Provedor cuida de patching, hardware e segurança física.

**Vantagens:**

- Rápida implementação de novos ambientes.
- Escalabilidade on-demand e global.
- Redução de custo inicial e necessidade de equipe especializada.
- Acesso remoto de qualquer lugar com internet.

**Desvantagens:**

- Dependência de conexão de internet e latência variável.
- Exposição a riscos compartilhados de segurança.
- Custo total pode aumentar sem boa governança de recursos.
- Menor controle físico sobre a infraestrutura.

**Exemplos de Uso:**

- Aplicações web de alto tráfego.
- Testes e desenvolvimento (ambientes temporários).
- Serviços de big data, machine learning e analytics.

**Quando Escolher:**

- Projetos que demandam escalabilidade rápida.
- Startups ou equipes com orçamento inicial limitado.
- Aplicações distribuídas geograficamente.

---

### 3. Modelo Híbrido (Hybrid Cloud)

**Descrição:**

- Combinação de ambientes On-Premise e Cloud, integrados de forma orquestrada para atender diferentes necessidades.

**Arquitetura e Integração:**

- **Rede e Conectividade:** VPNs ou conexões dedicadas (ex.: AWS Direct Connect, Azure ExpressRoute).
- **Orquestração e Gerenciamento:** Ferramentas como VMware vRealize, Azure Arc ou Kubernetes multicloud.
- **Replicação de Dados:** Sincronização entre datacenter local e storage em nuvem.

**Vantagens:**

- Otimização de custos: cargas de trabalho flexíveis em nuvem e sistemas críticos locais.
- Resiliência: failover automático entre ambientes.
- Adoção gradual da nuvem, mantendo legado no local.
- Compliance seletiva: dados sensíveis ficam on-premise.

**Desvantagens:**

- Complexidade de gestão e governança mista.
- Integração e segurança entre ambientes exigem planejamento robusto.
- Custos adicionais com ferramentas de orquestração e conectividade dedicada.

**Exemplos de Uso:**

- Processamento de picos de demanda em nuvem mantendo bancos de dados principais internos.
- Backup e recuperação de desastre (DR) na nuvem.
- Ambientes de desenvolvimento/teste em nuvem, produção local.

**Melhores Práticas:**

- Definir claramente quais workloads ficam em cada ambiente.
- Implementar políticas de segurança unificadas (Identity Federation, IAM).
- Monitoramento centralizado e automação de deploy.

---

**Referência de Escolha**

| Critério | On-Premise | Cloud | Híbrido |
| --- | --- | --- | --- |
| Controle | Máximo | Moderado | Balanceado |
| Investimento (CAPEX) | Elevado | Baixo (OPEX) | Médio |
| Escalabilidade | Limitada | Alta | Alta |
| Flexibilidade | Baixa | Alta | Alta |
| Complexidade de Gestão | Média | Baixa | Alta |
| Compliance | Facilmente auditável | Compartilhada | Personalizável |
