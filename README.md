# 🎮 Microsoft Rewards Tool

[![Versão](https://img.shields.io/badge/Versão-1.2.2-brightgreen)]()
[![Licença](https://img.shields.io/badge/Licença-GPL--3.0-blue)]()
[![Status](https://img.shields.io/badge/Status-Ativo-success)]()

**Ferramenta completa, moderna e leve para Microsoft Rewards — Feita especialmente para caçadores brasileiros.**

Uma Single-File Application (SFA) que roda direto no navegador, sem dependências, para acompanhar seus pontos diários, streak, meta mensal e conversão em reais.

<img width="891" height="821" alt="image" src="https://github.com/user-attachments/assets/7ef6b865-ba1d-4f8f-aae2-92bd900d228e" />

---

## ✨ Funcionalidades Principais

### 🎯 Metas e Progressão
- **Meta Mensal:** Barra de progresso em tempo real que salva automaticamente.
- **Sistema de Níveis (Tiers):** Badge dinâmico (Membro 🥉, Prata 🥈, Gold 🥇) que atualiza com base nos seus pontos mensais, seguindo as regras do MS Rewards Brasil.
- **Estimativa Avançada:** Projeção de dias para bater a meta (ativa a partir do 7º dia) e **Projeção Final** estimando seu saldo no fim do mês.

### 🔥 Streak Inteligente
- **Sistema Híbrido:** No modo **Automático** (padrão), o streak calcula dinamicamente pelo histórico e reseta se pular um dia. No modo **Manual**, você ajusta o valor livremente via botão ✏️.
- **Celebração de Marcos:** Animação especial (Streak Burst) ao atingir milestones (7, 14, 21, 28, 30 dias...).

### 💰 Conversões e Estatísticas
- **Conversor Pontos → Reais:** Taxa personalizável e dinâmica em tempo real. *(Padrão inicial: 5.165 pts = R$ 30,00)*.
- **Estatísticas Detalhadas:** Grid mostrando seu Melhor Dia, Pior Dia e Total Acumulado no mês.

### 📅 Histórico e Dados
- **Histórico com Seletor de Data:** Adicione, edite ou exclua pontos de qualquer dia passado. Ordenação inteligente e exibição do valor em Reais.
- **Detecção de Novo Mês:** Modal automático na virada do mês permitindo *Resetar e Arquivar*, *Somente Arquivar* ou *Ignorar*.
- **Importação e Exportação Total:** Suporte completo para **JSON** e **CSV** (Excel, Google Sheets).
- **Backup Automático:** Rotina preventiva que salva backups em segundo plano, com botão de restauração rápida no footer.

### 🎨 Interface e Experiência
- **Temas Dark/Light:** Persistente com transições suaves via CSS Variables.
- **Layout Adaptável:** Modo Vertical (padrão) e **Modo Horizontal** para Desktops/Tablets.
- **Tooltips Enriquecidos:** Modais explicativos (ℹ️) detalhando regras de níveis, cálculos e dicas da comunidade.

---

## 🛠️ Tecnologias e Arquitetura

Este projeto foi construído como uma **Single-File Application (SFA)**. Toda a interface, estilização e lógica vivem dentro de um único `index.html`, rodando de forma 100% nativa no navegador, **sem dependências externas**.

- **HTML5 & CSS3:** Layout híbrido (Flex & Grid), Design Responsivo via Media Queries e Tematização nativa com Variáveis CSS (`:root`).
- **Vanilla JavaScript (ES6+):**
  - **`AppState`:** Fonte única de verdade. Toda a inteligência e estado do app ficam encapsulados em um objeto global, eliminando conflitos de escopo.
  - **Correção de Fuso Local:** A função `getLocalDateString` previne bugs de conversão UTC (garantindo que pontos registrados à noite não vazem para o dia anterior).
  - **Debounce:** O conversor usa *debounce de 300ms* para evitar re-renderizações excessivas durante a digitação.
  - **Sanitização e Validação:** Funções como `escapeHtml()` (mitigação de XSS) e `validatePositiveNumber()` (blinda cálculos contra valores inválidos).
  - **APIs Nativas:** Uso de `FileReader` e `Blob` para manipulação de arquivos (Import/Export) e `localStorage` para persistência de dados e backups.

---

## 🚀 Como Usar

Você não precisa instalar nada! Basta:

1. Baixe o arquivo **`index.html`** (e o ícone `rewards.png` na mesma pasta caso queira xd).
2. Abra o `index.html` diretamente no seu navegador (Recomendados: Edge ou Chrome/Brave. Funciona(?) no Firefox).
3. Comece a registrar seus pontos diários. Tudo é salvo automaticamente no seu navegador!

**Ou use a versão online (GitHub Pages):**
👉 [https://y4sh1r01.github.io/MSRewardsTool/](https://y4sh1r01.github.io/MSRewardsTool/)

---

## 📋 Versão Atual e Change-Log

**Versão Atual:** 1.2.2

[Ver change-log completo nas Releases](https://github.com/Y4SH1R01/MSRewardsTool/releases)

### 📌 To-Do

- [ ] Pensar em novas melhorias e features para a comunidade.

---

## 💡 Observações Importantes

- A ferramenta usa **apenas os dias que você registra** para calcular a média diária e as projeções finais. Quanto mais consistente, mais precisa a projeção.
- No modo automático, o streak conta os dias consecutivos no histórico e **é zerado** se pular um dia. Você pode alternar para o modo manual a qualquer momento clicando em ✏️.
- Seus dados são salvos no `localStorage` do navegador. Se você limpar os dados de navegação, eles serão apagados (use a função de Exportar JSON para manter backups seguros em disco).

---

## 🙌 Agradecimentos

Feito com carinho para a comunidade brasileira do Microsoft Rewards. Inspirado originalmente em uma ferramenta mostrada num tweet do usuário [Augusto Masetti](https://x.com/augustomasetti) no X.

**Desenvolvido por Mateus (Y4SH1R01)**
* Assistência inicial: Grok 4.2.0-Quick Thinking e Specialist.
* Atualização v1.2.0: Kimi-k2.6 e Mistral 3.5b.
* Correções e features v1.2.1/v1.2.2: GLM-5.1.

Se você usa e gosta do projeto, considere dar uma ⭐ no repositório!

Última atualização: Junho de 2026.
