
## Módulo 1 – Visão Geral dos Conceitos de Nuvem

### Conceitos principais
A computação em nuvem permite acessar recursos de TI pela internet, sem necessidade de infraestrutura física.

### Tipos de computação em nuvem
- Nuvem pública  
- Nuvem privada  
- Nuvem híbrida  

### Vantagens da nuvem
- Pagamento sob demanda  
- Escalabilidade  
- Elasticidade  
- Alta disponibilidade  
- Redução de custos  
- Agilidade  

### AWS Cloud Adoption Framework (CAF)
Framework que orienta a adoção da nuvem em 6 perspectivas:
- Negócios  
- Pessoas  
- Governança  
- Plataforma  
- Segurança  
- Operações  

#### Segurança
- Controle de acesso  
- Proteção de dados  
- Monitoramento  
- Resposta a incidentes  

#### Operações
- Monitoramento de serviços  
- Gestão de recursos  
- Controle de mudanças  
- Recuperação de desastres  

### Principais aprendizados
- A adoção da nuvem exige planejamento  
- O AWS CAF organiza a transição  
- Diferentes áreas participam do processo  

### Questão exemplo
Pergunta: Por que a AWS é mais econômica para workloads variáveis?  
Resposta: C - Execução sob demanda  

---

## Módulo 2 – Economia e Faturamento da Nuvem

### Conceitos principais
- Modelo de pagamento conforme uso  
- Redução de custos com infraestrutura física  

### Custo Total de Propriedade (TCO)
- Compara custos entre nuvem e ambiente tradicional  
- Considera custos diretos e indiretos  

### Calculadora de Preços da AWS
Permite:
- Estimar custos mensais  
- Simular soluções  
- Identificar economia  

### Ferramentas de faturamento
- AWS Billing  
- AWS Cost Explorer  
- AWS Budgets  
- Relatórios de custos e uso  

### Planos de suporte
- Basic: sem suporte técnico  
- Developer: suporte para desenvolvimento  
- Business: suporte para produção  
- Enterprise: suporte completo  

#### Enterprise
- Suporte especializado  
- Acompanhamento proativo  
- TAM (Technical Account Manager) dedicado  

### Severidade de chamados
- Crítico  
- Urgente  
- Alto  
- Normal  
- Baixo  

### Principais aprendizados
- Controle e planejamento de custos  
- Uso de ferramentas financeiras  
- Importância do suporte adequado  

### Questão exemplo
Pergunta: Qual serviço fornece recomendações de otimização?  
Resposta: C - AWS Trusted Advisor  

---

## Módulo 3 – Infraestrutura Global da AWS

### Objetivo
Compreender como funciona a infraestrutura global da AWS e navegar no console.

---

### Conceitos principais

#### Regiões
- Áreas geográficas onde os serviços são hospedados  

#### Zonas de Disponibilidade (AZs)
- Data centers isolados dentro de uma região  

#### Locais de borda
- Usados para entregar conteúdo com baixa latência  

---

### Atividade prática
Durante a atividade no console da AWS, foram realizadas as seguintes ações:
- Exploração do menu de serviços  
- Identificação de categorias de serviços  
- Navegação entre regiões  
- Análise de recursos como VPC e Subnets  

---

### Respostas da atividade

1. IAM pertence à categoria:  
Segurança, identidade e conformidade  

2. Amazon VPC pertence à categoria:  
Redes e entrega de conteúdo  

3. Subnets existem no nível:  
Zona de Disponibilidade  

4. VPC existe no nível:  
Região  

5. Serviços globais:
- IAM  
- Route 53  

Serviços regionais:
- EC2  
- Lambda  

---

### Principais aprendizados
- Diferença entre região e zona de disponibilidade  
- Identificação de serviços globais e regionais  
- Organização dos serviços no console AWS  

---

### Questão exemplo
Pergunta: Qual componente garante baixa latência no CloudFront?  
Resposta: B - Locais de borda  

---

## Conclusão Geral

Durante os módulos 1 a 3, foi possível aprender:
- Conceitos fundamentais da computação em nuvem  
- Estrutura de custos e faturamento da AWS  
- Funcionamento da infraestrutura global  
- Navegação no console da AWS  

Esses conhecimentos servem como base para o uso do IAM e demais serviços da AWS.


### Laboratório 1 – Introdução ao AWS IAM MODULO 4

## Objetivo
Este laboratório teve como objetivo compreender o funcionamento do Amazon Web Services IAM, explorando usuários, grupos e permissões.

---

## Etapas realizadas

### 1. Exploração inicial
- Acessado o serviço IAM no console da AWS  
- Visualizados os usuários:
  - user-1  
  - user-2  
  - user-3  

- Verificado que:
  - user-1 não possuía permissões diretas  
  - Nenhum usuário estava inicialmente em grupos  

---

### 2. Análise dos grupos
Foram analisados os seguintes grupos:

- EC2-Support  
  - Política: AmazonEC2ReadOnlyAccess  
  - Permissão: visualizar recursos EC2  

- S3-Support  
  - Política: AmazonS3ReadOnlyAccess  
  - Permissão: visualizar recursos S3  

- EC2-Admin  
  - Política em linha  
  - Permissão: visualizar, iniciar e parar instâncias EC2  

---

### 3. Associação de usuários aos grupos
Conforme o cenário proposto:

| Usuário  | Grupo        | Permissão |
|----------|-------------|----------|
| user-1   | S3-Support  | Leitura no S3 |
| user-2   | EC2-Support | Leitura no EC2 |
| user-3   | EC2-Admin   | Controle do EC2 |

---

### 4. Testes de acesso

#### user-1
- Acesso ao S3 (visualização de buckets)  
- Sem acesso ao EC2  

#### user-2
- Acesso ao EC2 (somente leitura)  
- Não pode iniciar ou parar instâncias  
- Sem acesso ao S3  

#### user-3
- Acesso total ao EC2  
- Conseguiu parar a instância LabHost  

---

### 5. URL de login do IAM
- Foi utilizada a URL de login específica da conta IAM  
- Login testado em janela anônima com diferentes usuários  

---

## Conclusão
- O IAM permite controle centralizado de acesso  
- Permissões são atribuídas principalmente via grupos  
- Políticas definem o que cada usuário pode fazer  
- O uso de grupos facilita organização e escalabilidade  

---

## Resultado final
O laboratório foi concluído com sucesso, validando:
- Análise de usuários  
- Associação a grupos  
- Aplicação de políticas  
- Testes práticos de permissões  