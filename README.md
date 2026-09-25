# 🎮 Microsoft Rewards Tool

[![Versão](https://img.shields.io/badge/Versão-1.8.0-brightgreen)]()
[![Licença](https://img.shields.io/badge/Licença-GPL--3.0-blue)]()
[![Status](https://img.shields.io/badge/Status-Ativo-success)]()
[![Changelog](https://shields.io/badge/Changelog-blue)](https://github.com/Y4SH1R01/MSRewardsTool/releases)

**Ferramenta completa, moderna e leve para Microsoft Rewards — Feita especialmente para caçadores brasileiros.**

Uma Single-File Application (SFA) que roda direto no navegador, sem necessidade de servidores ou banco de dados, para acompanhar seus pontos diários, streak, meta mensal, estatísticas profundas e conversão em reais.

<img width="1654" height="2630" alt="1 8 0" src="https://github.com/user-attachments/assets/c85f31c7-ed7d-4e88-9408-bd47caa71b56" />


---

## ✨ Funcionalidades Principais

### 🎯 Metas e Progressão
- **Meta Mensal:** Barra de progresso em tempo real que salva automaticamente.
- **Barra de Progresso Dinâmica:** A barra muda de cor automaticamente com base no seu avanço (🔴 Vermelha < 30%, 🟡 Amarela 30-70%, 🟢 Verde > 70%) e exibe a porcentagem **exata** (ex: `33.505%`), sem arredondamentos arbitrários.
- **Sistema de Níveis (Tiers):** Badge dinâmico (Membro 🥉, Prata 🥈, Gold 🥇) que atualiza com base nos seus pontos mensais, seguindo as regras oficiais do MS Rewards Brasil.
- **Estimativa Matemática Blindada:** Projeção precisa de dias necessários para bater a meta e **Projeção Final de Pontos** baseada no calendário real (detecta se o dia de hoje já foi registrado e calcula a média diária estritamente sobre o ritmo do mês atual).

### ⭐ Sistema de Tracking de Atividades
- **Ciclo de 7 dias:** Sistema visual para acompanhar sua série de atividades diárias e não se perder nas Séries de 1.000 pontos / peças de quebra-cabeça. Você pode clicar no texto da atividade para ajustar o dia do ciclo (1 a 7) manualmente quando quiser.
- **Trilha de Micro-Pílulas:** Acompanhamento visual com micro-pílulas dinâmicas e estrelas animadas (pulsam quando pendentes e brilham em dourado com efeito pop ao concluir).
- **Virada de Dia Automática (Sem F5):** O app monitora a passagem da meia-noite e a reabertura da aba via `visibilitychange`, avançando o dia do ciclo e desmarcando as estrelas sozinho, sem você precisar recarregar a página.

### 🔥 Streak Inteligente
- **Sistema Híbrido e Contínuo:** No modo **Automático** (padrão), o streak é calculado de forma contínua pelo histórico e reseta ao pular um dia. No modo **Manual**, você ajusta o valor livremente via botão ✏️ (ou digita `"auto"` para restaurar o cálculo dinâmico).
- **Aura de Fogo e Celebração:** Efeito visual de gradiente no card e animação comemorativa (*Streak Burst*) com sombreado radiante ao bater marcos (7, 14, 21, 28, 30 dias...).

### 📊 Estatísticas Avançadas e Análise
- **Gráfico de Tendência SVG Dinâmico:** Gráfico de linha procedural com gradiente suave e nós circulares, agora com **amplitude vertical expandida (72px)** para evidenciar com nitidez a diferença entre dias altos e baixos. No modo horizontal, estende automaticamente para exibir até 25 dias com resolução dobrada.
- **Tooltips Flutuantes Táteis (Mobile-Friendly):** Balões flutuantes interativos ao passar o mouse ou tocar nas bolinhas do gráfico, com área de toque ampliada (hitbox invisível de 16px) e trava anti-vazamento nas bordas da tela.
- **🟩 Mini-Heatmap de Presença no Mês (Estilo GitHub):** Grade mensal interativa (1 ao 30/31) com 3 intensidades de verde conforme a pontuação do dia, destaque de moldura dourada para o dia atual e dias futuros tracejados. Exibe a taxa percentual de presença do mês e detalhes de pontos ao tocar em qualquer quadradinho.
- **📅 Diagnóstico por Dia da Semana:** Modal dedicado que compila todo o histórico para revelar sua média real de pontos de Segunda a Domingo. Exibe barras relativas de rendimento, conversão em R$, recorde histórico e identifica automaticamente seu dia **👑 Mais Forte** e seu dia **📉 Mais Fraco** (todos os 7 dias visíveis sem scroll).
- **Extremos Detalhados:** O card de estatísticas exibe as datas exatas em que ocorreram seu Melhor e Pior Dia, além de traduzir o Total no Mês em Reais com fonte sutil.

### 💰 Conversões e Resgate
- **Conversor Pontos → Reais:** Taxa personalizável e dinâmica em tempo real *(Padrão inicial: 5.165 pts = R$ 30,00)*. Trata números em tempo real e descarta zeros à esquerda automaticamente.

### 📲 Sincronização Instantânea (PC ↔ Celular)
- **Sincronização via QR Code (Zero Backend):** Transfira todo o seu histórico, streak e configurações do PC para o celular em 3 segundos. O app compacta os dados em formato ultraleve via Base64/Deflate embutido no link `#s=...`. Basta apontar a câmera do celular, abrir a página e confirmar a importação!
- **Link Direto de Compartilhamento:** Botão de 1 clique para copiar o link de sincronização e colar em mensageiros (WhatsApp Web, Telegram).

### 📅 Histórico e Arquivamento
- **Histórico com Seletor de Data:** Adicione, edite ou exclua registros de qualquer data com cálculo instantâneo do valor em Reais. No modo horizontal, exibe confortavelmente ao menos 5 itens de uma vez.
- **Detecção Inteligente de Novo Mês:** Modal automático na virada do mês oferecendo as opções *Resetar e Arquivar*, *Somente Arquivar* ou *Ignorar*.
- **📊 Resumo Mensal com Comparativo Mês a Mês (MoM):** O modal de histórico analisa o crescimento entre os meses arquivados exibindo badges de evolução (`▲ +X pts (+Y%)` ou `▼ -X pts (-Y%)`), registro da streak final atingida no mês e sanfona expansível com a listagem diária detalhada.
- **Importação e Exportação Total:** Suporte completo para **JSON** e **CSV** (compatível com Excel e Google Sheets), preservando tanto o mês ativo quanto todos os arquivos retroativos.
- **Backup Automático:** Rotina preventiva em segundo plano que salva cópias automáticas no `localStorage`, com restauração rápida pelo rodapé.

### 🎨 Interface e Experiência
- **Modo Claro de Alto Contraste:** Tematização refinada com paleta ergonômica (dourado escuro `#92400e`, verde esmeralda `#15803d` e preto sólido para valores), eliminando textos desbotados e garantindo legibilidade perfeita sob o sol.
- **Layout com Zero Salto (Sem FOUC):** Abertura instantânea no modo vertical ao carregar ou dar F5, sem piscar em tela cheia.
- **Modo Horizontal:** Alternância suave para telas largas com organização em duas colunas e rodapé com alinhamento simétrico (linha única de 6 botões no horizontal e grid 3x2 no vertical).
- **Sistema de Diálogos Assíncronos (`Dialog` Engine):** Substituição definitiva dos pop-ups bloqueantes nativos do navegador (`prompt`/`confirm`) por modais modernos baseados em Promises que fecham com tecla `ESC` ou clique fora.

---

## 🛠️ Tecnologias e Arquitetura

O projeto é construído como uma **Single-File Application (SFA)** focada em máxima performance e independência de infraestrutura. ~~**(FUNCIONA SEM INTERNET!?!)**~~

Nesse projeto usamos:
- **HTML5 Semântico & CSS3 Moderno:** Layout híbrido com Flexbox e Grid, variáveis CSS completas em `:root` e `body.light`, e transições suaves de aceleração por hardware.
- **QRCode.js:** Biblioteca externa embutida via CDN para renderização procedural de códigos QR vetoriais diretamente no canvas do navegador.
- **Vanilla JavaScript (ES6+ Modular):**
  - **`AppState`:** Centralização reativa de estado em objeto único com auto-persistência e rotinas de backup.
  - **Compressão de Payload:** Uso de `TextEncoder` / `TextDecoder` combinados com codificação Base64 URL-safe para serializar centenas de registros dentro de hashes de URL sem estourar limites de QR Code.
  - **Renderização SVG Dinâmica:** O gráfico é desenhado proceduralmente com coordenadas calculadas em tempo de execução, interpolação de caminho e hitboxes transparentes táteis.
  - **Algoritmo Multi-Fase de Sequência:** O cálculo de dias consecutivos percorre o histórico do mês corrente e transpassa meses anteriores arquivados sem quebrar a contagem.
  - **Segurança e Sanitização:** Sanitização estrita com `escapeHtml()` contra injeções XSS e validação de limites numéricos com `validatePositiveNumber()`.

---

## 🚀 Como Usar

Você não precisa compilar nem instalar nada:

1. Baixe o arquivo **`index.html`** (e mantenha o ícone `rewards.png` na mesma pasta se quiser o ícone funcionando na header kkk).
2. Abra o `index.html` diretamente em qualquer navegador moderno (Edge, Chrome, Brave, Firefox(?)).
3. Comece a registrar seus pontos. Tudo é salvo automaticamente no seu navegador!

**Ou use a versão online oficial hospedada no GitHub Pages:**  
👉 [https://y4sh1r01.github.io/MSRewardsTool/](https://y4sh1r01.github.io/MSRewardsTool/)

---

## 💡 Observações Importantes

- **Sincronização:** Para transferir dados entre computador e celular pelo QR Code, certifique-se de que o link gerado aponta para a sua versão atualizada no GitHub Pages.
- **Backup dos Dados:** Como o armazenamento utiliza o `localStorage` do navegador, limpar o cache/dados de navegação pode apagar suas informações. Use com frequência o botão **📤 Exportar JSON** para manter uma cópia física segura no seu dispositivo.
- **Cálculos de Média:** As estimativas dependem da sua consistência diária. Quanto mais dias forem registrados sem faltas, mais exata se torna a projeção de pontos no final do mês.

---

## 🙌 Agradecimentos e Créditos

Projeto criado com carinho para a comunidade brasileira de caçadores do Microsoft Rewards. Inspirado originalmente em uma ideia compartilhada por [Augusto Masetti](https://x.com/augustomasetti) no X.

**Desenvolvido por Mateus ([Y4SH1R01](https://github.com/Y4SH1R01))**
* Assistência inicial: Grok 4.2.0-Quick Thinking e Specialist.
* Atualização v1.2.0: Kimi-k2.6 e Mistral 3.5b.
* Correções e features v1.2.1-1.2.2: GLM-5.1.
* Correções e features v1.3.0-1.3.1: GLM-5-Turbo.
* Correções e features v1.3.2: GLM-5.2-Deep Think Max.
* Correções e features v1.4.0: GLM-5.2-Deep Think Max & Gemini-3.7-flash.
* Refatorações, novos módulos e versões v1.5.0-1.8.0: Gemini-3.7/3.8-flash.

Se a ferramenta te ajuda na sua rotina diária de pontos, deixe uma ⭐ no repositório!

**Última atualização:** 25 de setembro de 2026.
