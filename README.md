# 💰 FinAI Chat

> Aplicativo de organização financeira pessoal com Inteligência Artificial e interface conversacional.

---

# 📖PRD Otimizado Pelo Copilot

O **FinAI Chat** é um aplicativo de finanças pessoais baseado em conversação natural, criado para ajudar usuários a registrar receitas, despesas e metas financeiras sem a necessidade de planilhas complexas ou formulários extensos.

O usuário interage com um assistente inteligente através de um chat, utilizando linguagem simples e natural.

Exemplos:

> "Gastei R$ 50 no mercado"

> "Recebi R$ 3.000 de salário"

> "Quero economizar R$ 500 até dezembro"

A IA interpreta automaticamente as mensagens, categoriza as transações e apresenta insights financeiros personalizados.

---

# 🎯 Objetivo do Produto

Tornar o controle financeiro simples, acessível e intuitivo para pessoas que não possuem familiaridade com aplicativos financeiros tradicionais.

---

# 🚨 Problema

Muitas pessoas abandonam o controle financeiro porque:

- Consideram os aplicativos complexos;
- Precisam preencher muitos dados manualmente;
- Não entendem relatórios financeiros;
- Não recebem orientações personalizadas.

O FinAI Chat resolve esse problema através de uma experiência conversacional guiada por IA.

---

# 👥 Público-Alvo

### Persona 1

**João, 28 anos**

- Funcionário CLT
- Nunca utilizou aplicativos financeiros
- Deseja entender para onde o dinheiro está indo

### Persona 2

**Maria, 42 anos**

- Autônoma
- Faz controle financeiro mentalmente
- Busca dicas práticas para reduzir gastos

---

# ✅ Hipótese de Produto

Usuários iniciantes terão maior aderência ao controle financeiro quando puderem registrar seus gastos por meio de conversa natural em vez de formulários tradicionais.

---

# 🧠 Conceito Vibe Coding

Este projeto seguirá o conceito de **Vibe Coding**, focando em:

- MVP extremamente enxuto
- Entrega rápida
- Baixo consumo de créditos no Lovable
- Reaproveitamento máximo de componentes
- Validação antes de adicionar novas funcionalidades

## Fora do Escopo do MVP

❌ Open Finance

❌ Integrações bancárias

❌ OCR de comprovantes

❌ Cartões de crédito

❌ Investimentos

❌ Planejamento patrimonial

❌ Multiusuários

---

# 🚀 Funcionalidades do MVP

## 1. Registro Financeiro por Chat

O usuário registra receitas e despesas utilizando linguagem natural.

### Exemplo

Entrada:

```text
Gastei R$ 80 no mercado
```

Saída:

```text
Despesa registrada com sucesso.
Categoria: Alimentação
Valor: R$ 80,00
```

---

## 2. Categorização Automática

A IA identifica automaticamente a categoria da transação.

### Categorias Iniciais

- Alimentação
- Transporte
- Moradia
- Saúde
- Educação
- Lazer
- Salário
- Outros

---

## 3. Metas Financeiras

Permitir que usuários definam objetivos de economia.

### Exemplo

```text
Quero economizar R$ 1000 até dezembro
```

Resultado:

- Meta criada
- Valor alvo definido
- Acompanhamento automático

---

## 4. Relatórios Simplificados

Resumo visual das finanças.

### Informações

- Receitas totais
- Despesas totais
- Saldo atual
- Gastos por categoria

---

## 5. Agente Financeiro IA

A IA analisa hábitos financeiros e gera sugestões personalizadas.

### Exemplos

```text
Você gastou 38% da sua renda com alimentação este mês.
```

```text
Reduzindo 10% dos gastos com delivery você poderá atingir sua meta 20 dias antes.
```

---

# 🎨 Design Universal

O aplicativo deve seguir os princípios de Design Universal para garantir acessibilidade e inclusão.

## Requisitos

### Simplicidade

Máximo de três ações principais por tela.

### Legibilidade

- Fonte mínima de 16px
- Alto contraste

### Acessibilidade

- Compatibilidade com leitores de tela
- Navegação por teclado
- Textos alternativos para elementos visuais

### Inclusão Cognitiva

Evitar termos financeiros complexos.

Utilizar:

✅ Dinheiro recebido

✅ Dinheiro gasto

✅ Economia acumulada

Em vez de:

❌ Liquidez

❌ Patrimônio

❌ Fluxo de caixa

---

# 📱 Telas do MVP

## 1. Chat

Tela principal da aplicação.

### Componentes

- Histórico de mensagens
- Campo de entrada
- Sugestões rápidas

Botões:

- Registrar gasto
- Registrar receita
- Criar meta
- Ver relatório

---

## 2. Metas

Exibição das metas financeiras.

### Card da Meta

- Título
- Valor alvo
- Valor acumulado
- Percentual concluído

---

## 3. Relatórios

Resumo financeiro.

### Indicadores

- Receitas
- Despesas
- Saldo

### Visualizações

- Gráfico de pizza
- Resumo de categorias

---

## 4. Perfil

Dados básicos do usuário.

### Campos

- Nome
- Renda mensal
- Objetivo financeiro principal

---

# 🏗 Arquitetura Técnica

## Frontend

- React
- TypeScript
- Tailwind CSS
- Shadcn/UI

## Backend

### Supabase

Utilizar:

- Authentication
- PostgreSQL
- Row Level Security

---

# 🤖 Inteligência Artificial

Modelo inicial:

- OpenAI GPT-4o Mini

Responsabilidades:

- Extração de valores monetários
- Identificação de categorias
- Interpretação de linguagem natural
- Geração de recomendações financeiras

---

# 🗄 Estrutura do Banco de Dados

## users

```sql
id UUID PRIMARY KEY
name TEXT
email TEXT
monthly_income NUMERIC
goal_type TEXT
created_at TIMESTAMP
```

## transactions

```sql
id UUID PRIMARY KEY
user_id UUID
type TEXT
amount NUMERIC
category TEXT
description TEXT
transaction_date DATE
created_at TIMESTAMP
```

## goals

```sql
id UUID PRIMARY KEY
user_id UUID
title TEXT
target_amount NUMERIC
current_amount NUMERIC
target_date DATE
created_at TIMESTAMP
```

---

# 📊 Métricas de Validação

## Métrica Principal

Usuário registrar pelo menos:

```text
5 transações
```

durante a primeira semana.

## Métricas Secundárias

- Metas criadas
- Relatórios visualizados
- Retenção após 7 dias
- Volume de mensagens enviadas

---

# 🛣 Roadmap Futuro

## Fase 2

- Open Finance
- Importação de extratos
- OCR de comprovantes
- IA preditiva

## Fase 3

- Investimentos
- Planejamento financeiro
- Múltiplas contas
- Assistente financeiro avançado

---

# 🎯 Prompt Inicial para Lovable

```text
Crie um aplicativo chamado FinAI Chat.

Objetivo:
Permitir que usuários registrem receitas, despesas e metas financeiras utilizando linguagem natural através de um chat inteligente.

Tecnologias:
- React
- TypeScript
- Tailwind
- Supabase

Telas:
1. Chat
2. Metas
3. Relatórios
4. Perfil

Funcionalidades:
- Cadastro/Login
- Registro de receitas e despesas via chat
- Categorização automática
- Gestão de metas financeiras
- Dashboard de receitas, despesas e saldo
- Interface mobile first

Requisitos:
- Design Universal
- Alto contraste
- Fontes mínimas de 16px
- Componentes reutilizáveis
- Estrutura preparada para integração futura com IA

Não implementar:
- Open Finance
- Integrações bancárias
- OCR
- Investimentos

Primeiro gere toda a interface com dados mockados.
```

---

# 💡 Estratégia de Economia de Créditos no Lovable

1. Gerar primeiro apenas a interface completa.
2. Validar navegação.
3. Conectar Supabase.
4. Criar banco de dados.
5. Implementar autenticação.
6. Implementar chat com dados simulados.
7. Conectar IA apenas na etapa final.

Essa abordagem minimiza retrabalho e reduz significativamente o consumo de créditos durante o desenvolvimento.

---

# 💬 Interações com o Lovable

Durante o desenvolvimento do MVP, foram realizadas algumas interações estratégicas com o Lovable para maximizar o uso dos créditos disponíveis e validar rapidamente as principais funcionalidades.

## Prompt Inicial

```text
Crie um App de Finanças Pessoais com base no seguinte PRD (Product Requirements Document): {PRD}
```

---
<img width="473" height="424" alt="image" src="https://github.com/user-attachments/assets/d66b080d-c2b4-438b-a8e4-4c7a35c22dc2" />


## Refinamento Realizado

Durante os testes, foi identificado um possível problema relacionado à criação de metas financeiras.

### Solicitação

```text
Tentei criar uma meta chamada Reserva de Emergência, mas ela não apareceu no componente. A impressão que tive foi que apenas o Assistente Financeiro a reconheceu, poderia verificar?

Além disso, onde vejo os gráficos e extrato?
```

### Resposta

```text
Sim (Quer que eu adicione uma tela de relatórios com gráficos e extrato detalhado das transações?)
```

Essa interação permitiu identificar funcionalidades que ainda não estavam visíveis na interface e direcionou a evolução do MVP.

---

# 🎯 Resultado Final

Protótipo funcional desenvolvido no Lovable:

### acrescentar aqui o link lovable

---

# 🔍 Funcionalidades Implementadas

## 1. Dashboard Financeiro

Exibe um panorama geral das finanças do usuário.

### Informações apresentadas

- Receitas totais
- Despesas totais
- Saldo disponível

### Benefícios

- Visão rápida da situação financeira
- Interface simples e intuitiva
- Fácil compreensão para usuários iniciantes

---

## 2. Assistente Financeiro

Assistente conversacional responsável por acompanhar o usuário ao longo da sua jornada financeira.

### Recursos

- Conversação em linguagem natural
- Sugestões de organização financeira
- Incentivo à criação de metas
- Mensagens motivacionais e educativas

---

## 3. Registro de Transações via Chat

Permite registrar movimentações financeiras diretamente pela conversa.

### Exemplos

```text
Gastei R$ 80 no mercado
```

```text
Recebi R$ 2.500 de salário
```

### Benefícios

- Não exige formulários
- Experiência mais natural
- Menor barreira de entrada

---

## 4. Metas Financeiras

Área destinada à criação e acompanhamento de objetivos financeiros.

### Funcionalidades

- Criar metas financeiras
- Acompanhar progresso
- Visualizar evolução da economia

### Exemplo

```text
Reserva de Emergência
Meta: R$ 5.000
```

---

## 5. Relatórios Personalizados

Apresentação visual dos dados financeiros.

### Recursos

- Resumo financeiro
- Evolução das metas
- Acompanhamento dos gastos
- Visualização simplificada para tomada de decisão

---

## 6. Design Universal

O aplicativo foi concebido para atender diferentes perfis de usuários.

### Principais características

- Linguagem simples
- Navegação intuitiva
- Alto contraste
- Interface limpa
- Compatibilidade com leitores de tela
- Estrutura preparada para comandos por voz
- Feedbacks visuais para facilitar a utilização

---

# 🧠 Reflexão

## O que funcionou bem?

O refinamento prévio do PRD utilizando o Microsoft Copilot foi extremamente importante para aumentar a qualidade das respostas geradas pelo Lovable.

Como os créditos diários disponíveis eram limitados, possuir um documento bem estruturado reduziu retrabalho e permitiu direcionar melhor as interações.

---

## O que não funcionou como esperado?

A expectativa inicial era realizar mais interações gratuitas com o Lovable.

Entretanto, os créditos foram consumidos rapidamente durante o processo de refinamento e ajustes da aplicação.

Mesmo assim, as interações realizadas foram suficientes para validar conceitos importantes do projeto.

---

## O que aprendi sobre conversar com IAs?

A principal lição foi que interagir com uma IA é muito parecido com interagir com uma pessoa.

Quanto mais contexto, clareza, objetivos e detalhes são fornecidos, melhores tendem a ser as respostas obtidas.

Além disso:

- Um PRD bem estruturado reduz retrabalho.
- Prompts específicos economizam créditos.
- Limitar o escopo do MVP acelera a validação.
- Iterações pequenas produzem melhores resultados que grandes solicitações genéricas.

---

# 🚀 Conclusão

O FinAI Chat demonstrou que uma experiência financeira baseada em conversação natural pode simplificar significativamente o controle financeiro pessoal.

A combinação entre Design Universal, Inteligência Artificial e Vibe Coding permitiu construir um MVP funcional, validando rapidamente a proposta de valor do produto com um consumo reduzido de créditos na plataforma Lovable.
``
