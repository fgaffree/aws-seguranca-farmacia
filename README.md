# Projeto: Recomendação de Ferramentas AWS para Segurança de Sistema em Farmácia

## Descrição
Este projeto tem como objetivo recomendar e explicar a implementação de **três serviços da AWS focados em aumentar a segurança de sistemas** utilizados por uma farmácia fictícia. A ideia é demonstrar como aplicar recursos nativos da nuvem para proteger dados sensíveis, controlar acessos e detectar comportamentos suspeitos.

---

## Contexto
A farmácia fictícia passou por um processo de digitalização e está hospedando seu sistema de gestão de estoque e vendas na nuvem. Com o aumento no tráfego de informações e dados confidenciais de clientes (como dados pessoais e de pagamento), a empresa busca **reforçar a segurança da sua infraestrutura**.

---

## Ferramentas recomendadas

### 1. **AWS IAM (Identity and Access Management)**
**Justificativa:** Permite a **criação e o gerenciamento de usuários, grupos e permissões de acesso**. Com ele, é possível definir exatamente quem pode acessar quais recursos dentro da AWS.

**Implementação:**
- Criar grupos por função (ex: administradores, desenvolvedores, analistas)
- Atribuir permissões de forma granular com IAM Policies
- Ativar **MFA (autenticação multifator)** para todos os usuários

---

### 2. **AWS KMS (Key Management Service)**
**Justificativa:** Garante a **criptografia dos dados em repouso e em trânsito**, aumentando a proteção de informações sensíveis como histórico de compras, cadastros e dados de pagamento.

**Implementação:**
- Utilizar chaves gerenciadas pela AWS para criptografar dados armazenados em RDS, S3 e EBS
- Integrar o KMS com serviços que armazenam dados sensíveis
- Definir permissões de uso de chaves com IAM ou roles específicas

---

### 3. **Amazon GuardDuty**
**Justificativa:** Serviço de **detecção inteligente de ameaças**, que analisa continuamente logs e eventos para identificar comportamentos maliciosos ou anômalos na conta AWS.

**Implementação:**
- Ativar o GuardDuty na região onde os serviços estão sendo usados
- Integrar com CloudWatch para notificações e respostas automáticas
- Acompanhar alertas diretamente no console e implementar remediação com Lambda

---

## Conclusão
Com a implementação das ferramentas **IAM**, **KMS** e **GuardDuty**, a farmácia fictícia passa a ter uma base sólida de segurança na nuvem: desde o **controle de acessos**, passando pela **proteção de dados sensíveis**, até a **detecção proativa de ameaças**. Essa abordagem eleva o nível de conformidade e resiliência da empresa frente a riscos digitais.

---

> Projeto criado com propósito educacional para exercício prático na plataforma Web DIO.
