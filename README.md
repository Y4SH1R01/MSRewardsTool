# Microsoft Rewards Tool

**Calculadora completa para Microsoft Rewards — Feita especialmente para caçadores brasileiros.**

Uma ferramenta bonita, leve e totalmente funcional (ou era pra ser!) para acompanhar seus pontos do Microsoft Rewards no dia a dia.

![Preview](https://i.imgur.com/r9gmLh9.png)

## ✨ Funcionalidades

- **Meta Mensal** com barra de progresso (salva automaticamente)
- **Streak (sequência de dias)** editável
- **Conversor Pontos → Reais** em tempo real
- **Taxa de conversão** personalizável e dinâmica
- **Histórico completo** (até 30 dias)
  - Adicionar pontos do dia
  - Editar ou excluir itens individuais (clicando no registro)
  - Valor em reais exibido em amarelo dourado
  - Total acumulado visível
- **Estimativa inteligente** de dias restantes para bater a meta (baseada na média real)
- **Tempo restante no mês** (mostra dias ou "Xh Ymin" quando estiver perto do fim)
- **Dark Mode / Light Mode** com persistência
- **Animações suaves** (fade-in ao adicionar itens)
- **Totalmente responsivo** (otimizado para mobile)
- **Todos os dados salvos** no navegador (`localStorage`)

## 🛠 Tecnologias Utilizadas

- **HTML5**
- **CSS3** (com variáveis, Flexbox, Media Queries e animações)
- **JavaScript** (Vanilla JS — sem frameworks)
- `localStorage` para persistência de dados

**Projeto single-file** (apenas um arquivo `.html`).

## 🚀 Como usar

1. Baixe o arquivo `index.html`
2. Abra diretamente no navegador (Chrome, Edge, Firefox ou Safari)
3. Comece a usar! Tudo é salvo automaticamente no seu navegador.

**OU**

[Abra este link em Deployment na minha página do Github!](https://y4sh1r01.github.io/MSRewardsTool/)

## 📋 Como funciona a média diária, o exemplo de pontos, a inserção de sequência diária e como modificar eles

Esse exemplo é totalmente editável caso necessário ao caso da Microsoft aumentar ou abaixar os pontos necessários para comprar os gift cards de 15, 30 reais por exemplo, assim como todos os elementos com botões de edição.

⬇️⬇️⬇️

![Preview](https://i.imgur.com/ouerH23.png)

A ferramenta de média diária calcula a média usando **apenas os dias que você registrou** no histórico.  
Quanto mais dias você adicionar, mais precisa fica a projeção de quantos dias faltam para bater sua meta mensal, também inserível como na imagem abaixo.

⬇️⬇️⬇️

![Preview](https://i.imgur.com/gR9s6Vi.png)

**Ela também adiciona +1 na contagem de dias da sequência diária cada vez que você adicionar seus pontos diários no histórico e salva até 30 dias seguidos no mesmo.** 

⬇️⬇️⬇️

![Preview](https://i.imgur.com/df3ViWI.png)

## 📌 Versão Atual

**1.0-rc2** — Versão estável, algumas features não listadas em testes

## 📝 To Do List* 

- Uma maneira de Exportar/Importar Dados em json ou algo parecido, pela conveniência de talvez limpar o cache do PC e ter o histórico salvo
- Mudar a maneira de edição do histórico de pontos — invés de ser um click no valor, um botão.
- Atualizar a func do exemplo padrão para salvar á sua preferência/necessidade (caso a Microsoft mude os preços dos gifts!) no LocalStorage da mesma forma de outras funcs — no momento ele atualiza se você recarregar a página.
- Adicionar as explicações dadas neste README no próprio HTML para conviniência, assim como no card dos dias restantes.

*Talvez será adicionado, não dou certeza:*

- Um gráfico usando Chart.js ou algo parecido para visualizar o progresso da meta mensal. Isso aumentaria o tamanho do HTML de uma certa forma e eu não sei como ou se seria útil mas assumo eu que seria xd
- Modo Horizontal com suporte Desktop/Mobile.

*Não tenho um timeframe exato mas pretendo continuar modificando e atualizando isso aqui. Talvez adicionarei a change-log na própria HTML se necessário.

## 🙌 Agradecimentos

Feito com carinho para a comunidade brasileira de caçadores do Microsoft Rewards.
Agradecimento especial á quem se interessou á testar as versões betas que eu compartilhei via Discord.

Inspirado no software/calculadora de um Tweet do User [Augusto Masetti no X](https://x.com/augustomasetti)

Se você usa e gosta do projeto, considere dar uma ⭐ no repositório!

---

**Desenvolvido por:** Mateus (Y4SH1R01) com ajuda do Grok 4.20 Quick Thinking/Specialist.

**Data:** Março-Abril 2026
