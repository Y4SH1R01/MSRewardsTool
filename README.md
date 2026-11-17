# 🎮 Microsoft Rewards Tool

[![Versão](https://img.shields.io/badge/Versão-1.10.1-brightgreen)]()
[![Licença](https://img.shields.io/badge/Licença-GPL--3.0-blue)]()
[![Status](https://img.shields.io/badge/Status-Ativo-success)]()
[![Changelog](https://shields.io/badge/Changelog-blue)](https://github.com/Y4SH1R01/MSRewardsTool/releases)

**Ferramenta completa, moderna e leve para Microsoft Rewards — Feita especialmente para caçadores brasileiros.**

Uma Single-File Application (SFA) que roda direto no navegador, sem necessidade de servidores ou banco de dados, para acompanhar seus pontos diários, streak, quebra-cabeça semanal, meta mensal, metas de eventos sazonais, estatísticas profundas e conversão em reais.

<img width="1654" height="3114" alt="index.html" src="https://github.com/user-attachments/assets/e9034615-135a-4e35-b77b-b40784e6ac82" />

---

## ✨ Funcionalidades Principais

### 🎯 Metas e Progressão
- **Barra de Progresso Dinâmica:** A barra muda de cor automaticamente com base no seu avanço (🔴 Vermelha < 30%, 🟡 Amarela 30-70%, 🟢 Verde >= 70%) e exibe a porcentagem detalhada (ex: `33.5%`).
- **📍 Marca de Ritmo Ideal (Pacing Marker):** Marcador luminoso integrado à barra de progresso indicando o dia atual do calendário. Informa instantaneamente se você está adiantado (`🚀`) ou atrasado (`⚠️`) em relação ao fim do mês.
- **🏆 Nó de Checkpoint de 100% (Modo Excedente):** Ao bater e ultrapassar a meta, a barra libera valores acima de 100% sem travas, fixando uma cápsula neon dourada no ponto exato em que a meta foi concluída, acompanhada de celebração única por mês com chuva de confetes.
- **🎯 Meta para Data Específica (Modo Evento):** Modal preditivo integrado ao card de Estimativas para planejar o acúmulo mirando compras futuras (*Black Friday*, *Natal*, *Fim de Ano* ou o que você preferir, como lançamentos de jogos e assinaturas). Projeta seu montante final através da fórmula $\text{Saldo em Conta} + (\text{Média Diária} \times \text{Dias até lá})$, indicando a cobertura da meta, folga financeira ou a pontuação extra diária necessária.
- **Sistema de Níveis (Tiers):** Badge dinâmico (Membro 🥉, Prata 🥈, Gold 🥇) que atualiza com base nos seus pontos mensais, seguindo as regras oficiais do MS Rewards Brasil.
- **Estimativa Matemática Inteligente:** Média diária calculada sobre o mês ativo (com fallback seguro para o histórico registrado quando o mês ainda está no início). As projeções de *Faltam para meta* e *Projeção final* são liberadas com segurança a partir do 7º dia registrado para evitar distorções prematuras.

### ⭐ Sistema de Tracking de Atividades & 🧩 Quebra-Cabeça
- **Card Unificado Lado a Lado:** Rastreador semanal de atividades e tabuleiro de quebra-cabeça integrados em um único bloco compacto.
- **Ciclo de 7 Dias:** Acompanhamento de séries diárias (*Bing*, *Conjunto Diário*, *Edge*, *App Móvel* e *Pesquisa Visual*) com ajuste manual do dia (1 a 7) ao clicar no nome.
- **🎁 Destaque de Bônus no 7º Dia:** No dia decisivo do ciclo semanal, a atividade ganha animação dourada pulsante com a tag `🎁 Bônus Hoje!`, alternando para `🎁 Resgatado` após concluída.
- **🧩 Tabuleiro de Quebra-Cabeça (12 Peças = +1.000 pts):** Board SVG interativo com encaixe de peças que revela a recompensa conforme você avança. Entrega peças automaticamente ao concluir atividades no 7º dia e registrar os pontos do dia (suportando múltiplas atividades no mesmo dia), além de permitir clique direto nas peças, incremento rápido (`+`) ou ajuste manual (0 a 12) com fanfarra sonora e confetes duplos ao completar 12/12.
- **Virada Automática de Dia:** Avanço do ciclo de atividades, desmarcação das estrelas e reset do quebra-cabeça concluído ao cruzar a meia-noite ou reabrir a aba (`visibilitychange`), sem necessidade de recarregar a página (`F5`).

### 🔥 Streak Inteligente
- **Cálculo Contínuo Híbrido:** Modo **Automático** (padrão) com preservação da streak real histórica através de múltiplos meses arquivados (detectando quebras intermediárias e reversões por *Desfazer* com precisão), e modo **Manual** (`✏️`) para ajustes livres (digite `"auto"` para restaurar o cálculo dinâmico).
- **Aura de Fogo Animada & Celebração:** Ícone vetorial animado (`lottie-web`) e efeito visual radiante (*Streak Burst*) com confetes e fanfarra ao alcançar marcos (7, 14, 21, 28, 30+ dias).

### 📊 Estatísticas Avançadas e Análise
- **Gráfico de Tendência com Comparativo Interativo:** Curva procedural SVG com amplitude vertical destacada e seletor para comparar o mês atual contra o mês anterior ou arquivos passados. Balões flutuantes unificados exibem lado a lado o desempenho em pontos e Reais. Centralização precisa mesmo no 1º dia de registro.
- **🟩 Mini-Heatmap de Presença com Modo Calendário:** Grade do mês atual com 3 intensidades de verde, moldura dourada no dia de hoje e botão de alternância (`🗓️ Calendário / ⚡ Faixa`) para visualização clássica em formato de folhinha (Segunda a Domingo).
- **🗓️ Heatmap Anual Estilo GitHub (365 Dias):** Grade panorâmica de 52/53 semanas no modal de *Resumo Mensal*, compilando o histórico ativo somado a todos os meses arquivados. Dias da semana (Segunda a Domingo) perfeitamente alinhados, tooltip interativo em R$ e layout responsivo sem barras de rolagem no desktop.
- **📅 Diagnóstico por Dia da Semana:** Análise agregada revelando sua média real de pontos de Segunda a Domingo, com barras proporcionais e identificação automática do dia **👑 Mais Forte** e **📉 Mais Fraco**.
- **Extremos Detalhados:** Registro das datas exatas do Melhor e Pior Dia e conversão financeira do total mensal.

### 💰 Conversões e Gestão de Carteira
- **💼 Saldo na Conta Microsoft (Carteira em Tempo Real):** Módulo dedicado para registrar os pontos que você já possui guardados na conta oficial.
  - **Sincronização Automática:** Ao registrar os pontos do dia no histórico, o saldo é incrementado automaticamente. Edições ou exclusões reajustam a diferença na hora.
  - **Card Unificado no Topo:** Fusão harmoniosa do Saldo da Conta com a Taxa Base de Conversão em um único componente moderno com divisória sutil.
- **Conversor Dinâmico Pontos → Reais:** Taxa personalizável em tempo real *(Padrão: 5.165 pts = R$ 30,00)* com suporte a decimais, validação contra divisão por zero e tratamento automático de zeros à esquerda.

### 📸 Compartilhamento e Exportação Completa
- **Card de Conquista do Mês em Full HD (1200x700) com QR Code:** Gerador de imagem widescreen 16:9 via Canvas nativo, pronto para download e envio no Discord/WhatsApp. Desenha a curva real de pontos do mês, destaca os 4 maiores picos com coroa (`👑`) no recorde, exibe sua consistência mensal e inclui um QR Code dinâmico apontando para a ferramenta.
- **📦 Pacote Completo ZIP (`JSZip`):** Exportação em 1 clique reunindo o backup `.json`, a planilha Excel (`.xlsx`) e o Card de Conquista (`.png`) dentro de um único arquivo compactado.

### 📲 Sincronização Instantânea (PC ↔ Celular)
- **Sincronização via QR Code (Zero Backend):** Transfira saldo em conta, histórico completo, meses arquivados, streak, atividades, quebra-cabeça e meta por data do PC para o celular em segundos. Dados compactados via Base64/Deflate embutidos no hash da URL (`#s=...`), com ajuste automático para manter o QR Code legível mesmo em históricos grandes.
- **Link Direto:** Cópia rápida em 1 clique para envio via mensageiros.

### 📅 Histórico, Arquivamento e Backups
- **Calendário Interativo (`flatpickr`) & Histórico Completo:** Inserção, edição e exclusão de pontos com seletor de data estilizado nos temas claro/escuro, bolinhas verdes indicadoras nos dias já registrados e atualização automática após a meia-noite.
- **Feedback Imediato no Toast com *Desfazer* (`SweetAlert2`):** Notificação de confirmação com variação em relação ao dia anterior (`▲ +X` / `▼ -Y`) e botão rápido **Desfazer** para reverter o lançamento na hora.
- **Resumo Mensal Consolidado:** Análise de crescimento mês a mês (MoM), badges de evolução, histórico sanfona, **Total Histórico Consolidado** (livre de dupla contagem) e **Poder de Compra em 365 Dias**.
- **Virada de Mês com Estilo Nativo:** Modal automático com opções para *Resetar e Arquivar*, *Somente Arquivar* ou *Ignorar*.
- **Importação/Exportação JSON e Excel Nativo (`.xlsx`):** Geração de planilhas multi-aba (*Resumo*, *Histórico Atual* e *Meses Anteriores*) via `SheetJS` e importação inteligente com suporte a datas brasileiras (`DD/MM/AAAA`), ISO e datas seriais do Excel — tudo organizado em um menu sanfona retrátil (*Accordion*).
- **Sistema de Restauração Multi-Ponto Pré-Alteração:** Captura automaticamente até os últimos **5 estados anteriores** às suas modificações reais (com data, hora, motivo da alteração, saldo e contagem de registros), além do **Ponto Seguro Pré-Importação**.

### 🎨 Interface, Áudio e Experiência
- **🔀 Dashboard Personalizável (Drag & Drop):** Reordene livremente qualquer card pela alça visual (`⠿`) utilizando `SortableJS`, com salvamento automático da ordem e botão `🔀` no cabeçalho para restaurar o layout padrão.
- **🔊 Efeitos Sonoros Retrô (`Web Audio API`):** Central de áudio sintetizada em tempo real direto no navegador (sem arquivos externos), com feedback sonoro dedicado ao marcar atividades, encaixar peças, desfazer ações e completar marcos, além de botão mudo/ativar (`🔊 / 🔇`) no cabeçalho.
- **🎰 Contadores Animados (`CountUp.js`) & Animações de Lista (`auto-animate`):** Transições fluidas em placares de pontos e na movimentação dos itens do histórico.
- **💬 Painel Flutuante Arrastável para Dicas (`ℹ️`):** Tooltips não-bloqueantes posicionados contextualmente dentro dos limites visíveis da tela, com suporte a arraste livre.
- **🌌 Fundo Estelar Dinâmico (Starfield Canvas):** Motor procedural de partículas estelares com física contínua sincronizada via **Delta Time**, adaptando-se suavemente à taxa de quadros nativa do monitor (60Hz, 120Hz, 144Hz+).
- **Modo Claro de Alto Contraste & Modo Horizontal:** Paleta ergonômica para luz forte, layout expandido para telas largas e detecção automática de orientação em smartphones e tablets.
- **Sistema de Diálogos Assíncronos (`Dialog` Engine):** Modais modernos baseados em Promises com botões **Cancelar** e **Confirmar**, envio via `Enter` e fechamento via `ESC`.

---

## 🛠️ Tecnologias e Arquitetura

O projeto é construído como uma **Single-File Application (SFA)** focada em máxima performance e independência de infraestrutura.

- **HTML5 Semântico & CSS3 Moderno:** Flexbox, CSS Grid, variáveis `:root`/`body.light`, Glassmorphism e `backdrop-filter`.
- **Bibliotecas via CDN:** `SortableJS`, `CountUp.js`, `JSConfetti`, `@formkit/auto-animate`, `lottie-web`, `SheetJS (xlsx)`, `flatpickr`, `SweetAlert2`, `JSZip` e `QRCode.js`.
- **Vanilla JavaScript (ES6+ Modular):**
  - **`AppState`:** Centralização reativa de dados com persistência no `localStorage` e histórico automático de restauração pré-alteração.
  - **Áudio Procedural (`Web Audio API`):** Síntese de efeitos sonoros em tempo real sem dependências externas.
  - **Compressão de Payload via Streams:** Uso de `CompressionStream('deflate')` e Base64 URL-safe para sincronização completa entre aparelhos via URL/QR Code.
  - **Renderização Gráfica e Canvas 2D:** Curvas SVG em tempo real, tabuleiro jigsaw SVG e exportação procedural de cards Full HD (1200x700).
  - **Física Estelar Procedural:** Animação baseada em Delta Time independente do framerate do navegador.
  - **Sanitização e Validação:** Proteção contra XSS com `escapeHtml()` e validação numérica rigorosa.

---

## 🚀 Como Usar

Você não precisa compilar nem instalar nada:

1. Baixe o arquivo **`index.html`** (e mantenha o ícone `rewards.png` na mesma pasta para o ícone do cabeçalho).
2. Abra o `index.html` diretamente em qualquer navegador moderno (Edge, Chrome, Brave, Firefox, Safari).
3. Comece a registrar seus pontos. Tudo é salvo automaticamente no seu navegador!

**Ou use a versão online oficial hospedada no GitHub Pages:**  
👉 [https://y4sh1r01.github.io/MSRewardsTool/](https://y4sh1r01.github.io/MSRewardsTool/)

---

## 💡 Observações Importantes

- **Sincronização:** Para transferir dados entre computador e celular pelo QR Code, certifique-se de que o link gerado aponta para a versão atualizada do GitHub Pages.
- **Backup dos Dados:** Como o armazenamento utiliza o `localStorage`, limpar os dados de navegação pode apagar suas informações. Use regularmente o menu **📂 Opções de Backup e Transferência** (`📄 JSON`, `📗 Excel` ou `📦 Pacote ZIP`) para manter uma cópia física segura.
- **Cálculos de Média e Eventos:** As projeções dependem da sua consistência diária. Quanto mais dias forem registrados no histórico, mais precisas se tornam as estimativas de fechamento de mês e metas de eventos futuros.

---

## 🙌 Agradecimentos e Créditos

Projeto criado com carinho para a comunidade brasileira de caçadores do Microsoft Rewards. Inspirado originalmente em uma ideia compartilhada por [Augusto Masetti](https://x.com/augustomasetti) no X.

**Desenvolvido por Mateus ([Y4SH1R01](https://github.com/Y4SH1R01)) Com ajuda das IAs:**
* Assistência inicial: Grok 4.2.0-Quick Thinking e Specialist.
* Atualização v1.2.0: Kimi-k2.6 e Mistral 3.5b.
* Correções e features v1.2.1-1.2.2: GLM-5.1.
* Correções e features v1.3.0-1.3.1: GLM-5-Turbo.
* Correções e features v1.3.2: GLM-5.2-Deep Think Max.
* Correções e features v1.4.0: GLM-5.2-Deep Think Max & Gemini-3.7-flash.
* Correções e features v1.5.0-1.9.1a: Gemini-3.7/3.8-flash.
* Correções e features v1.10: Gemini-3.8-flash, Gemini-3.5-flash-lite *e* Gemini-3.1-Pro-Preview.
* Correções e features v1.10.1: Gemini-4-Hydrogen.

Se a ferramenta te ajuda na sua rotina diária de pontos, deixe uma ⭐ no repositório!

**Última atualização:** 16 de novembro de 2026.
