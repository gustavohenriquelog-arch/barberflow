# 💊 FarmaCode
Assistente Virtual de Vendas para Farmácias via WhatsApp

---

## 📌 Visão Geral

O FarmaCode é um assistente virtual inteligente desenvolvido para automatizar o atendimento e as vendas de farmácias através do WhatsApp.

O sistema atua como um “funcionário virtual”, capaz de atender clientes, consultar preços, verificar disponibilidade de produtos, realizar vendas e integrar com sistemas de pagamento.

Através da combinação de n8n (orquestração de fluxo), Evolution Go (integração com WhatsApp), Google Sheets/ERP (dados de produtos e estoque) e modelos avançados de IA (OpenAI), o FarmaCode proporciona um atendimento ágil, escalável e disponível 24/7.

---

## 🎯 Objetivo

Automatizar o processo de atendimento e vendas de farmácias, reduzindo a dependência de atendentes humanos e aumentando a eficiência operacional.

---

## 🚀 Funcionalidades

- Atendimento automático via WhatsApp
- Consulta de produtos
- Consulta de preços
- Verificação de estoque
- Sugestão de produtos similares
- Registro de pedidos
- Integração com sistemas de pagamento
- Registro de clientes
- Histórico de conversas

---

## 🔄 Fluxo Principal

Webhook → IF (filtro) → Tratamento → IA → Consulta Produto → Venda → Pagamento → Resposta

### Descrição:

- Webhook → recebe mensagem do cliente
- IF → valida mensagens (evita spam/status)
- Tratamento → organiza dados (nome, telefone, mensagem)
- IA → interpreta intenção do cliente
- Consulta Produto → busca preço e estoque
- Venda → registra pedido
- Pagamento → gera link ou integra com gateway
- Resposta → retorna ao cliente

---

## 🧠 Inteligência do Sistema

O assistente é capaz de:

- Interpretar pedidos em linguagem natural  
  Ex: “tem dipirona?”, “quanto custa paracetamol?”

- Sugerir alternativas  
  Ex: “não temos esse, mas temos similar”

- Conduzir o cliente até a compra

- Identificar intenção de compra

---

## 🔐 Segurança

- Cada cliente é identificado pelo número de telefone
- Dados de pedidos vinculados ao telefone
- Validação antes de confirmar pedidos
- Não expõe dados de outros clientes

---

## 💳 Pagamento

O sistema poderá integrar com:

- Pix (link ou QR Code)
- Gateway de pagamento
- Sistemas internos da farmácia

---

## 📊 Armazenamento

- Google Sheets (MVP)
- ERP da farmácia (fase avançada)

Dados armazenados:

- Nome do cliente
- Telefone
- Produto
- Quantidade
- Valor
- Status do pedido

---

## 🎯 Público-Alvo

- Farmácias de bairro
- Drogarias independentes
- Redes pequenas e médias
- Farmácias que vendem via WhatsApp

---

## 💡 Proposta de Valor

- Atendimento 24 horas
- Redução de custos com atendentes
- Aumento nas vendas
- Respostas rápidas e padronizadas
- Escalabilidade do atendimento

---

## 💰 Modelo de Negócio

### Planos:

**Básico — R$397/mês**
- Atendimento automático
- Consulta de preços
- Registro simples de pedidos

**Intermediário — R$597/mês**
- Consulta de estoque
- Sugestão de produtos
- Integração com pagamento

**Premium — R$797/mês**
- Integração com ERP
- Relatórios
- Automação completa de vendas

**Implementação — R$997**
- Configuração do sistema
- Integrações
- Personalização inicial

---

## 🚀 Status do Projeto

- [ ] Ideia estruturada
- [ ] Definição de fluxo
- [ ] MVP em desenvolvimento
- [ ] Integração com produtos
- [ ] Integração com pagamento
- [ ] Testes com usuários
- [ ] Pronto para venda

---

## 🔮 Próximos Passos

- Definir estrutura de produtos (base de dados)
- Criar fluxo de consulta de estoque
- Integrar pagamento (Pix)
- Construir MVP funcional
- Testar com farmácia real
