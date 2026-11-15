# 💸 App Questfinance de Organização de Finanças Pessoais com Vibe Coding
##PRD refinado com Gemini: 
```Markdown
Crie um aplicativo web de finanças pessoais gamificado estilo RPG chamado **QuestFinance RPG**, inspirado nas mecânicas de evolução do Habitica, com estética moderna de jogo em Dark Mode.

### 1. Identidade Visual e Layout
* **Tema:** Dark Mode sofisticado (tons de roxo profundo/ardósia `#1A1625` e `#262136` nos cards) com cores vibrantes para status: Dourado/Amarelo para XP e Moedas, Vermelho/Esmeralda para HP (Saúde Financeira) e Roxo/Índigo para botões principais.
* **Ícones:** Utilize exclusivamente ícones da biblioteca `lucide-react` (`Shield`, `Coins`, `Trophy`, `Sword`, `Heart`, `Sparkles`, `Scroll`, `Send`, `TrendingUp`, `Wallet`).
* **Responsividade:** Layout mobile-first centralizado (max-width de 900px no desktop) com navegação limpa por abas na parte inferior ou superior.

### 2. Header Persistente (Status do Jogador)
Fixo no topo da aplicação, exibindo:
* **Avatar & Identidade:** Ícone de personagem estilizado, Nome do Jogador ("Aventureiro Financeiro") e Badge de **Nível (Lvl 1)** + Título atual (ex: *"Aprendiz das Moedas"*).
* **Barra de HP (Saúde do Orçamento Mensal):** Começa em `100/100 HP`. Representa a saúde do orçamento mensal de R$ 3.000,00.
* **Barra de XP (Experiência):** Começa em `0/100 XP`. Ao atingir 100 XP, o jogador sobe de nível (`Level Up!`), zera o excesso de XP e ganha uma notificação comemorativa (toast).
* **Carteira & Ouro:** Exibe o **Saldo Financeiro Real (R$)** e as **Moedas de Ouro (Gold)** acumuladas.

### 3. Navegação e Telas Principais (Abas)
Crie 4 abas principais com transição fluida e dados iniciais pré-populados (mock data) para demonstrar o funcionamento imediatamente:

#### Aba 1: Taverna (Chat Mestre Financeiro - Tela Principal)
* Interface de chat interativa onde o usuário registra movimentações digitando frases naturais.
* **Lógica inteligente simulada (Parser no Front-end):** Ao enviar uma mensagem, o app deve identificar palavras-chave e valores numéricos automaticamente:
  * *Se contiver "investi", "guardei", "poupei" + valor:* Registra como **Investimento**, soma ao saldo investido, concede **+50 XP** e **+25 Gold**, e responde como um Mestre de RPG elogiando a disciplina.
  * *Se contiver "recebi", "salário", "ganhei" + valor:* Registra como **Receita**, aumenta o saldo em R$, concede **+20 XP** e responde comemorando o tesouro obtido.
  * *Se contiver "gastei", "comprei", "paguei" + valor:* Registra como **Despesa** (categorizando automaticamente entre Alimentação, Lazer, Transporte ou Outros com base nas palavras), desconta do saldo em R$ e concede **+10 XP** pela constância de registrar. *Regra de dano:* Se o total de gastos do mês ultrapassar o orçamento definido, subtrai **-15 HP** com alerta visual.
* Adicione 3 botões de "Ações Rápidas" acima do campo de texto para facilitar testes: *"Gastei 35 no almoço"*, *"Investi 200 hoje"*, *"Recebi 1500 de freela"*.

#### Aba 2: Quadro de Missões (Metas Financeiras)
* Lista de missões estilo pergaminho/card com barra de progresso e botão de interação:
  * **Missão 1:** *Reserva de Emergência* (Meta: R$ 1.000 | Atual: R$ 450) -> Recompensa: `+100 XP` e `+50 Gold`.
  * **Missão 2:** *Semana Sem Delivery* (Meta: 7 dias) -> Botão "Concluir Missão" que entrega `+80 XP`.
  * **Missão 3:** *Fechar o Mês no Azul* -> Botão "Simular Fechamento Positivo" que entrega `+200 XP` e dispara animação de Level Up.
* Botão **"+ Nova Missão"** para o usuário criar uma meta financeira personalizada com nome, valor alvo e recompensa em XP.

#### Aba 3: Loja da Guilda (Recompensas Cosméticas)
* Onde o usuário gasta suas **Moedas de Ouro (Gold)** ganhas por bons hábitos:
  * *Título: "Mestre do Orçamento"* (50 Gold)
  * *Título: "Lobo dos Investimentos"* (120 Gold)
  * *Poção de Cura (+30 HP)* para recuperar saúde financeira após um mês difícil (80 Gold)
  * *Escudo Anti-Impulso (Item decorativo no perfil)* (150 Gold)
* Ao comprar, desconta o Gold e equipa o item/título no Header do jogador.

#### Aba 4: Estatísticas (Mapa de Gastos)
* Cards resumindo: Total de Receitas, Total de Despesas e Total Investido no mês.
* Gráfico simples de barras ou rosca (usando `recharts`) mostrando gastos por categoria.
* Histórico completo das transações lançadas pelo chat, com opção de excluir um lançamento caso tenha sido digitado errado.

### 4. Requisitos Técnicos
* Utilize `localStorage` para salvar o progresso do jogador (Nível, XP, HP, Gold, transações e missões) para que nada se perca ao recarregar a página, incluindo um botão discreto "Resetar Jogo" no rodapé para testes.
* Adicione feedback visual rico com `sonner` (toasts) sempre que o usuário ganhar XP, perder HP, comprar um item ou subir de nível.

```
##Interações com Lovable
-Crie um aplicativo web de finanças pessoais gamificado estilo RPG chamado QuestFinance RPG, inspirado nas mecânicas de evolução do Habitica, com estética moderna de jogo em Dark Mode.
-Build Now

Resultado final no Lovable:  https://616dae3e607a4cc4860e0a20178da1b3.prod.enter.pro

<img width="883" height="624" alt="image" src="https://github.com/user-attachments/assets/1b577785-d9bf-489a-87b3-c6a41ede5deb" />

##Resumo do projeto 

# QuestFinance RPG

> **Transforme o controle financeiro em uma jornada épica.** Um aplicativo web de finanças pessoais que une interface conversacional (chat em linguagem natural) com mecânicas de RPG gamificadas inspiradas no *Habitica*.

---

## Visão Geral do Projeto

A maioria dos aplicativos de finanças falha na retenção porque exige entrada manual burocrática e torna o controle de gastos uma tarefa entediante. O **QuestFinance RPG** resolve esse problema substituindo formulários complexos por um **Chat Mestre Financeiro** e recompensando bons hábitos com progressão de personagem.

Este projeto foi desenvolvido como um MVP funcional utilizando conceitos de **PRD (Product Requirements Document)** e **Vibe Coding**.

---

## Funcionalidades Implementadas (MVP)

### 1. Status do Aventureiro (Header Persistente)
* **Identidade & Nível:** Exibe o avatar do jogador, nível atual (`Lvl`), título equipado (ex: *Aprendiz das Moedas*) e saldo financeiro em tempo real.
* **HP do Orçamento:** Barra de saúde financeira vinculada ao teto de gastos mensal[cite: 1]. Ultrapassar o limite causa dano ao personagem.
* **Experiência (XP) & Gold:** Barras de progresso que recompensam a constância financeira e permitem evoluir de nível.

### 2. Taverna (Chat Mestre Financeiro)
* **Processamento em Linguagem Natural:** O usuário registra movimentações digitando frases simples como *"gastei 50 no almoço"*, *"investi 200 hoje"* ou *"recebi 1500 de freela"*.
* **Categorização Automática:** Identifica receitas, investimentos e despesas (categorizando automaticamente em Alimentação, Lazer, Transporte, etc.).
* **Feedback Imediato:** Cada lançamento concede XP pela constância ou ouro (Gold) por aportes e investimentos.
* **Ações Rápidas:** Botões de atalho para agilizar registros frequentes.

### 3. Quadro de Missões (Metas Financeiras)
* Metas financeiras estruturadas como *Quests* com barras de progresso visual e recompensas definidas em XP e Gold (ex: *Reserva de Emergência*, *Semana Sem Delivery*, *Fechar o Mês no Azul*)].
* Criação de missões personalizadas pelo próprio usuário.

### 4. Loja da Guilda
* Espaço para trocar o **Gold** acumulado por recompensas cosméticas e utilitárias, como novos títulos de perfil (*Mestre do Orçamento*, *Lobo dos Investimentos*), itens decorativos (*Escudo Anti-Impulso*) e *Poções de Cura* para recuperar o HP do orçamento.

### 5. Estatísticas (Mapa de Gastos)
* Resumo mensal consolidado de **Receitas**, **Despesas** e **Total Investido**.
* Gráfico visual de distribuição de gastos por categoria.
* Histórico completo de lançamentos sincronizado com o chat, com opção de exclusão.

### 6. Persistência Local
* Todo o progresso do jogador (nível, XP, HP, Gold, transações e missões) é salvo automaticamente no navegador via `localStorage`, com opção de resetar o jogo a qualquer momento.

---

## Stack Tecnológica

* **Front-end:** React + TypeScript + Vite
* **Estilização:** Tailwind CSS (Dark Mode temático RPG)
* **Ícones:** Lucide React
* **Gráficos:** Recharts
* **Notificações:** Sonner

---

## Roadmap de Evolução (Próximos Passos)

- [ ] **Integração Automática Missões e Chat:** Vincular aportes registrados na Taverna diretamente ao progresso da missão *Reserva de Emergência*.
- [ ] **Orçamento Personalizável:** Permitir que o usuário edite o valor do teto mensal que define o HP máximo.
- [ ] **IA Generativa Real:** Conectar o chat a uma API de LLM (Gemini / OpenAI) para interpretações financeiras ainda mais complexas e conselhos personalizados.
- [ ] **Autenticação & Nuvem:** Migrar a persistência do `localStorage` para banco de dados em nuvem.

  
## Reflexão

###O que funcionou bem? 
O refinamento do prompt foi fundamental para conseguir com poucas interações o resultado obtido, pois são dados 100 créditos diário.

###O que não funcionou como o esperado?  
Inicialmente tive que fazer várias interações com o Gemini para chegar no prompt que mais chegava perto do que estava pensando para o app. 

###O que aprendeu sobre conversar com IAs?
Aprendi muito sobre quanto mais especifico for sobre o contexto e o que deseja obter mais assertiva será a Ia.
