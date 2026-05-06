💳 1. Princípios de Precificação

A AWS utiliza o modelo pay-as-you-go (pague apenas pelo uso). Os principais fatores que influenciam o custo são:

Computação: cobrança baseada no tempo de uso (por segundo ou por hora).
Armazenamento: custo calculado por GB utilizado ao longo do mês.
Transferência de dados:
Entrada (inbound): normalmente gratuita.
Saída (outbound): tarifada conforme o volume de dados enviado para fora da AWS.

📉 2. Custo Total de Propriedade (TCO)

O TCO serve para comparar o custo de infraestrutura local com o da nuvem:

On-premises: exige alto investimento inicial (CAPEX), incluindo servidores, espaço físico, energia e equipe de manutenção.
Nuvem: converte esses custos em despesas variáveis (OPEX), eliminando a necessidade de manter um data center físico.

🏢 3. AWS Organizations

Serviço que permite gerenciar várias contas AWS de forma centralizada:

Faturamento consolidado: reúne os custos de todas as contas, facilitando alcançar descontos por volume.
SCPs (Service Control Policies): definem limites de permissões para contas e usuários.
Estrutura hierárquica: organização das contas em Unidades Organizacionais (OUs).

🛠️ 4. Ferramentas de Controle Financeiro

AWS Pricing Calculator: usada antes da implementação para estimar custos.
AWS Budgets: cria alertas quando o gasto ultrapassa valores definidos.
AWS Cost Explorer: permite analisar padrões e históricos de uso.
AWS Cost and Usage Report: fornece dados detalhados de consumo e faturamento.

🆘 5. Planos de Suporte AWS

A AWS oferece diferentes níveis de suporte:

Básico: gratuito, com acesso à documentação e suporte para faturamento.
Developer: indicado para ambientes de desenvolvimento e testes.
Business: suporte 24/7 via chat, e-mail e telefone, ideal para produção.
Enterprise: inclui um gerente técnico dedicado (TAM).

💎 6. Serviços Gratuitos (camada base)

Alguns serviços não têm custo direto, mas os recursos criados por eles são cobrados:

IAM (controle de acesso)
Amazon VPC (rede virtual)
AWS CloudFormation (infraestrutura como código)
AWS Organizations
AWS Elastic Beanstalk

📌 Dica importante

Para a prova, lembre-se: Instâncias Reservadas oferecem desconto em troca de compromisso de uso (1 ou 3 anos). Existe também a opção No Upfront, onde não é necessário pagamento antecipado.