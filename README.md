# 🎮 Microsoft Rewards Tool

[![Versão](https://img.shields.io/badge/Versão-1.9.1a-brightgreen)]()
[![Licença](https://img.shields.io/badge/Licença-GPL--3.0-blue)]()
[![Status](https://img.shields.io/badge/Status-Ativo-success)]()
[![Changelog](https://shields.io/badge/Changelog-blue)](https://github.com/Y4SH1R01/MSRewardsTool/releases)

**Ferramenta completa, moderna e leve para Microsoft Rewards — Feita especialmente para caçadores brasileiros.**

Uma Single-File Application (SFA) que roda direto no navegador, sem necessidade de servidores ou banco de dados, para acompanhar seus pontos diários, streak, meta mensal, metas de eventos sazonais, estatísticas profundas e conversão em reais.

<img width="1511" height="2915" alt="y4sh1r01 github io_MSRewardsTool_" src="https://github.com/user-attachments/assets/a9d2df4b-5cb6-418c-bf8f-5a4e9d459417" />

---

## ✨ Funcionalidades Principais

### 🎯 Metas e Progressão
- **Barra de Progresso Dinâmica:** A barra muda de cor automaticamente com base no seu avanço (🔴 Vermelha < 30%, 🟡 Amarela 30-70%, 🟢 Verde > 70%) e exibe a porcentagem **exata** (ex: `33.505%`), sem arredondamentos arbitrários.
- **📍 Marca de Ritmo Ideal (Pacing Marker):** Marcador luminoso integrado à barra de progresso indicando o dia atual do calendário. Informa instantaneamente se você está adiantado (`🚀`) ou atrasado (`⚠️`) em relação ao fim do mês.
- **🏆 Nó de Checkpoint de 100% (Modo Excedente):** Ao bater e ultrapassar a meta, a barra libera valores acima de 100% sem travas, fixando uma cápsula neon dourada no ponto exato em que a meta foi concluída.
- **🎯 Meta para Data Específica (Modo Evento):** Modal preditivo integrado ao card de Estimativas para planejar o acúmulo mirando compras futuras (*Black Friday*, *Natal*, *Fim de Ano* ou oque você preferir (lançamentos de jogos, etc.). Projeta seu montante final através da fórmula $\text{Saldo em Conta} + (\text{Média Diária} \times \text{Dias até lá})$, indicando a cobertura da meta, folga financeira ou a pontuação extra diária necessária.
- **Sistema de Níveis (Tiers):** Badge dinâmico (Membro 🥉, Prata 🥈, Gold 🥇) que atualiza com base nos seus pontos mensais, seguindo as regras oficiais do MS Rewards Brasil.
- **Estimativa Matemática Sincronizada:** Média diária calculada estritamente sobre o mês ativo. As projeções de *Faltam para meta* e *Projeção final* são liberadas com segurança a partir do 7º dia registrado para evitar distorções prematuras.

### ⭐ Sistema de Tracking de Atividades
- **Ciclo de 7 Dias:** Acompanhamento de séries diárias (Bing, Conjunto Diário, Edge, App Móvel e Pesquisa Visual) para não perder as Séries de 1.000 pontos e peças de quebra-cabeça. Permite ajuste manual do dia (1 a 7) com um clique no nome.
- **🎁 Destaque de Bônus no 7º Dia:** No dia mais importante do ciclo semanal, a atividade ganha animação dourada pulsante com a tag `🎁 Bônus Hoje!`, alternando para `🎁 Resgatado` após concluída.
- **Trilha de Micro-Pílulas e Estrelas:** Pílulas visuais de progresso e estrelas com animação pop ao marcar a conclusão.
- **Virada Automática de Dia:** Avanço do ciclo e desmarcação automática das estrelas ao cruzar a meia-noite ou reabrir a aba (`visibilitychange`), sem necessidade de recarregar a página (F5).

### 🔥 Streak Inteligente
- **Cálculo Contínuo Híbrido:** Modo **Automático** (padrão) com preservação da streak real histórica mesmo através de múltiplos meses arquivados, e modo **Manual** (✏️) para ajustes livres (digite `"auto"` para restaurar o cálculo dinâmico).
- **Aura de Fogo e Celebração:** Efeito visual radiante (*Streak Burst*) com animação comemorativa ao bater marcos (7, 14, 21, 28, 30+ dias).

### 📊 Estatísticas Avançadas e Análise
- **Gráfico de Tendência com Comparativo Interativo:** Curva procedural SVG com amplitude vertical destacada e seletor para comparar o mês atual contra o mês anterior ou arquivos passados. Balões flutuantes unificados exibem lado a lado o desempenho em pontos e Reais. Centralização precisa mesmo no 1º dia de registro.
- **🟩 Mini-Heatmap de Presença com Modo Calendário:** Grade do mês atual com 3 intensidades de verde, moldura dourada no dia de hoje e botão de alternância (`🗓️ Calendário / ⚡ Faixa`) para visualização clássica em formato de folhinha (Segunda a Domingo).
- **🗓️ Heatmap Anual Estilo GitHub (365 Dias):** Grade panorâmica de 52/53 semanas no modal de Resumo Mensal, compilando o histórico ativo somado a todos os meses arquivados. Dias da semana (Segunda a Domingo) perfeitamente alinhados, tooltip interativo em R$ e layout responsivo sem barras de rolagem no desktop.
- **📅 Diagnóstico por Dia da Semana:** Análise agregada revelando sua média real de pontos de Segunda a Domingo, com barras proporcionais e identificação automática do dia **👑 Mais Forte** e **📉 Mais Fraco**.
- **Extremos Detalhados:** Registro das datas exatas do Melhor e Pior Dia e conversão financeira do total mensal.

### 💰 Conversões e Gestão de Carteira
- **💼 Saldo na Conta Microsoft (Carteira em Tempo Real):** Módulo dedicado para registrar os pontos que você já possui guardados na conta oficial.
  - **Sincronização Automática (v1.9.1a):** Ao registrar os pontos do dia no histórico, o saldo é incrementado automaticamente. Edições ou exclusões reajustam a diferença na hora.
  - **Card Unificado no Topo:** Fusão harmoniosa do Saldo da Conta com a Taxa Base de Conversão em um único componente moderno com divisória sutil.
- **Conversor Dinâmico Pontos → Reais:** Taxa personalizável em tempo real *(Padrão: 5.165 pts = R$ 30,00)* com descarte automático de zeros à esquerda.

### 📸 Compartilhamento e Imagens
- **Card de Conquista do Mês em Full HD (1200x700) com QR Code:** Gerador de imagem widescreen 16:9 via Canvas nativo, pronto para download e envio no Discord/WhatsApp. Desenha a curva real de pontos do mês, destaca os 4 maiores picos com coroa (`👑`) no recorde, exibe sua consistência mensal e inclui um QR Code dinâmico apontando para a ferramenta.

### 📲 Sincronização Instantânea (PC ↔ Celular)
- **Sincronização via QR Code (Zero Backend):** Transfira todo o seu histórico, streak, atividades e saldo do PC para o celular em segundos. Dados compactados via Base64/Deflate embutidos no hash da URL (`#s=...`).
- **Link Direto:** Cópia rápida em 1 clique para envio via mensageiros.

### 📅 Histórico, Arquivamento e Backups
- **Histórico Completo:** Inserção, edição e exclusão de pontos com seletor de data e cálculo instantâneo em Reais.
- **Feedback Imediato no Toast:** Notificação de confirmação com cálculo automático de oscilação em relação ao dia anterior (`▲ +X` / `▼ -Y`).
- **Resumo Mensal Consolidado:** Análise de crescimento mês a mês (MoM), badges de evolução, histórico sanfona e **Poder de Compra em 365 Dias** (projeção anual).
- **Virada de Mês com Estilo Nativo:** Modal automático com botões padronizados no design system do app e destaque em vermelho no botão *Ignorar*.
- **Importação/Exportação JSON e CSV:** Suporte total com compatibilidade para Microsoft Excel (`\uFEFF` UTF-8 BOM).
- **Ponto de Restauração Seguro (Safety Snapshot):** Cópia preventiva gerada automaticamente em segundo plano antes de qualquer importação de arquivos.

### 🎨 Interface e Experiência
- **🌌 Fundo Estelar Dinâmico (Starfield Canvas):** Motor procedural de partículas estelares com física contínua sincronizada via **Delta Time**, adaptando-se suavemente à taxa de quadros nativa do monitor (60Hz, 120Hz, 144Hz+).
- **Modais com Backdrop Blur e Fundo Sólido:** Janelas flutuantes com desfoque de fundo suave (`backdrop-filter: blur(2px)`) que preservam a visibilidade do Starfield, combinadas com interior opaco (`#121212`) para leitura sem vazamento de texto.
- **Modo Claro de Alto Contraste:** Paleta ergonômica (dourado `#92400e`, esmeralda `#15803d` e preto sólido) para visibilidade sob luz forte.
- **Modo Horizontal e Responsividade:** Ajuste fluido para telas largas e detecção automática de orientação em dispositivos móveis.
- **Sistema de Diálogos Assíncronos (`Dialog` Engine):** Pop-ups modernos e não-bloqueantes baseados em Promises com suporte a tecla `ESC`.

---

## 🛠️ Tecnologias e Arquitetura

O projeto é construído como uma **Single-File Application (SFA)** focada em máxima performance e independência de infraestrutura.

- **HTML5 Semântico & CSS3 Moderno:** Flexbox, CSS Grid, variáveis `:root`/`body.light`, Glassmorphism e `backdrop-filter`.
- **QRCode.js:** Biblioteca externa via CDN para geração vetorial procedural de códigos QR no Canvas.
- **Vanilla JavaScript (ES6+ Modular):**
  - **`AppState`:** Centralização reativa de dados com persistência imediata no `localStorage`.
  - **Compressão de Payload via Streams:** Uso de `CompressionStream('deflate')` e codificação Base64 URL-safe para serializar grandes históricos dentro de hashes de URL.
  - **Renderização Gráfica e Canvas 2D:** Desenho vetorial de curvas SVG em tempo real e exportação procedural de cards de conquista em alta resolução (1200x700).
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
- **Backup dos Dados:** Como o armazenamento utiliza o `localStorage`, limpar os dados de navegação pode apagar suas informações. Use regularmente o botão **📤 Exportar JSON** para manter uma cópia física segura.
- **Cálculos de Média e Eventos:** As projeções dependem da sua consistência diária. Quanto mais dias forem registrados no histórico, mais precisas se tornam as estimativas de fechamento de mês e metas de eventos futuros.

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
* Refatorações, novos módulos e versões v1.5.0-1.9.1a: Gemini-3.7/3.8-flash.

Se a ferramenta te ajuda na sua rotina diária de pontos, deixe uma ⭐ no repositório!

**Última atualização:** 06 de outubro de 2026.
