# Laboratório 1 – Introdução ao AWS IAM

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