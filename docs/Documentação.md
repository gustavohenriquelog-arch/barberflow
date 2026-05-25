# 🚀 Assistente Virtual BarberFlow
Sistema inteligente de atendimento e agendamento via WhatsApp

---

## 📌 Documentation Index
Documentação do projeto em evolução contínua. Esta versão apresenta a estrutura inicial, funcionalidades principais e arquitetura do sistema.

---

## 🧠 Visão Geral

O **Assistente Virtual BarberFlow** é uma solução de automação de atendimento desenvolvida para barbearias, com foco em agendamentos via WhatsApp de forma rápida, eficiente e escalável.

Construído com tecnologias modernas de automação e inteligência artificial, o sistema integra atendimento automatizado, gestão de agenda e interação humanizada com clientes em tempo real, proporcionando ganho de produtividade e padronização no atendimento.

Através da combinação de **n8n (orquestração de fluxo)**, **Evolution Go (integração com WhatsApp)**, **modelos avançados de IA (OpenAI)**, além da integração com **Google Calendar (gestão de agenda)** e **Google Sheets (armazenamento e controle de dados)**, o Assistente Virtual BarberFlow oferece uma experiência de atendimento contínua, automatizada e organizada, reduzindo a necessidade de intervenção manual e aumentando a eficiência operacional.

O sistema é projetado como uma solução escalável, permitindo evolução contínua e adaptação conforme as necessidades do negócio.

---

## 🎯 Proposta de Valor

O sistema é projetado para:

- Automatizar o atendimento inicial ao cliente, garantindo respostas rápidas e padronizadas  
- Gerenciar agendamentos de forma inteligente, com validação de horários em tempo real  
- Garantir organização e controle da agenda através da integração com Google Calendar  
- Registrar automaticamente os dados dos clientes no Google Sheets, criando uma base organizada para gestão e relacionamento  
- Reduzir falhas humanas no processo de marcação e controle de horários  
- Proporcionar uma experiência profissional, fluida e consistente para o cliente final  

---

## 🔄 Fluxo Principal

O fluxo de processamento do Assistente Virtual Barber Code segue uma arquitetura sequencial, garantindo controle, validação e resposta eficiente ao cliente.

---

### ⚙️ Fluxo de Execução

**Webhook**  
Responsável por receber as mensagens enviadas pelos clientes via WhatsApp, atuando como ponto de entrada do sistema.

**IF (Filtro de Segurança e Validação)**  
Realiza a validação das mensagens recebidas, garantindo que apenas interações válidas sejam processadas.  
Filtra eventos indevidos como status, mensagens do próprio sistema e dados incompletos.

**Tratamento de Dados**  
Organiza e padroniza as informações recebidas, preparando os dados para interpretação da inteligência artificial.

**IA (Inteligência Artificial)**  
Responsável por interpretar a intenção do cliente, conduzir a conversa e decidir a próxima ação, como agendamento, cancelamento ou resposta informativa.

**HTTP (Envio de Resposta)**  
Realiza o envio da resposta final ao cliente via WhatsApp, garantindo a comunicação contínua e automatizada.

---

### 📊 Visão Geral do Processo

- Processamento estruturado das mensagens  
- Validação e segurança nas interações  
- Respostas rápidas e consistentes  
- Separação clara de responsabilidades entre os componentes  

---

### 🔧 Observação Técnica

A arquitetura modular permite fácil manutenção e evolução do sistema, possibilitando a inclusão de novas etapas, integrações ou regras de negócio sem impacto direto no fluxo principal.

---

## 📈 Modelo de Negócio

Estrutura de monetização baseada em modelo SaaS (Software como Serviço), com cobrança recorrente e taxa de implantação.

---

### 🎯 Público-Alvo

- Barbearias de pequeno e médio porte  
- Profissionais autônomos (barbeiros)  
- Negócios com alto volume de atendimento via WhatsApp  

---

### 💡 Problema Resolvido

- Demora no atendimento ao cliente  
- Perda de agendamentos por falta de resposta rápida  
- Falta de organização na agenda  
- Erros manuais em marcações  
- Dependência de atendimento humano  

---

### 🚀 Solução Oferecida

- Atendimento automático 24 horas  
- Agendamento inteligente com validação de horário  
- Organização completa da agenda  
- Registro e controle de clientes  
- Padronização do atendimento  

---

### 💰 Estrutura de Planos

**Plano Básico — R$ 97/mês**  
Versão essencial para automação de atendimento e agendamentos simples.

**Plano Intermediário — R$ 147/mês**  
Inclui funcionalidades adicionais e maior controle de agenda e atendimento.

**Plano Premium — R$ 247/mês**  
Versão completa, com todos os recursos disponíveis e maior nível de automação.

---

### ⚙️ Taxa de Implementação

**Setup inicial — R$ 397 (pagamento único)**

Inclui:

- Configuração do sistema  
- Integração com WhatsApp  
- Ajuste do fluxo de atendimento  
- Personalização inicial  

---

## 👊 Status do Projeto

- Fluxo principal funcional  
- Integração com WhatsApp ativa  
- IA configurada e respondendo  
- Sistema pronto para validação com clientes reais  

---

## 🔮 Próximos Passos

- Implementar validação por telefone (segurança)  
- Criar controle de agendamentos por ID  
- Melhorar tratamento de erros  
- Otimizar custo de tokens  
- Validar com clientes reais  
- Evoluir planos e funcionalidades  

---
