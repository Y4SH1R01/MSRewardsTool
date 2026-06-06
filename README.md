# Microsoft Rewards Tool

**Ferramenta completa e bonita para Microsoft Rewards — Feita especialmente para caçadores brasileiros.**

Uma ferramenta leve, moderna e totalmente funcional para acompanhar seus pontos diários, streak, meta mensal e conversão em reais.

<img width="882" height="812" alt="image" src="https://github.com/user-attachments/assets/80287fb1-542d-48da-9433-872e15d3fc8c" />

## ✨ Funcionalidades

### Principais recursos
- **Meta Mensal** com barra de progresso em tempo real (salva automaticamente).
- **Sistema de Streak Híbrido (Automático/Manual):** No modo **Automático** (padrão), o streak calcula dinamicamente pelo histórico e reseta se pular um dia. No modo **Manual**, você ajusta o valor livremente via botão ✏️. Animação especial ao atingir milestones.
- **Seção de Estatísticas:** Card integrado ao final da dashboard exibindo o seu **Melhor dia**, **Pior dia** e o **Total acumulado no mês** em um layout em grid de 3 colunas.
- **Detecção Inteligente de Novo Mês:** Modal automático na virada do mês que permite *Resetar e Arquivar*, *Somente Arquivar* ou *Ignorar*, guardando o histórico e exportando um JSON de backup automaticamente para você acompanhar sua performance mês a mês.
- **Conversor Pontos → Reais** em tempo real com taxa personalizável e dinâmica.
  > **Nota:** Exemplo inicial de 5.165 pts = R$ 30,00, modificável para qualquer valor. Entrada otimizada com `debounce` para máxima fluidez e formatação de moeda correta (ex: R$ 1.500,00).
- **Estimativa Avançada:** Projeção de dias para bater a meta (a partir do 7º dia registrado) e uma caixa de **Projeção Final** calculando quantos pontos você terá no fim do mês baseado na sua média atual.
- **Histórico Completo com Seletor de Data:** Adicione pontos a qualquer dia passado usando o seletor de datas, edite ou exclua itens com valor em reais e total acumulado. A lista é ordenada cronologicamente de forma inteligente, mesmo ao adicionar dias fora de ordem. Ação de limpar histórico reforçada (reseta também o streak atual).
- **Backup e Restauração:** Criação de backups preventivos automáticos em segundo plano e botão **"💾 Restaurar Backup"** no footer para recuperação rápida.
- **Importação e Exportação Total:** Salve ou restaure backups completos via **JSON** e envie/traga seus dados diretamente de planilhas via **CSV** (Excel, Google Sheets).
- **Tooltips Enriquecidos:** Modais explicativos detalhados em todos os cards (regras do Nível 2, vantagens de busca, cashback, funcionamento das médias e tabela completa de bônus do Streak).
- **Interface Otimizada:** Tema Dark/Light persistente, modo horizontal (Landscape) para desktop/tablet, layout *full-bleed* (sem fendas laterais) e animações suaves.

### Dados salvos automaticamente
Tudo fica encapsulado com segurança na arquitetura interna (`AppState`) e guardado no `localStorage` do seu navegador: meta, streak (e seu modo atual), histórico, arquivos mensais (`monthlyArchives`), backups, exemplo de conversão e preferência de tema.

## 🛠️ Tecnologias e Arquitetura

O projeto é estruturado como uma **Single-File Application (SFA)**, concentrando toda a interface, estilização e lógica de negócios em um único arquivo `index.html`, rodando de forma 100% nativa e sem dependências externas.

### 🌐 HTML5 & CSS3 (Interface e Responsividade)
- **Layout Híbrido (Flex & Grid):** Uso de Flexbox para o alinhamento fluido dos cards da dashboard e **CSS Grid Layout** para organizar a seção de Estatísticas em uma malha responsiva de 3 colunas.
- **Design Adaptável:** Media queries otimizadas para smartphones e suporte ao **Modo Horizontal (Landscape)** para desktops ou tablets.
- **Tematização Nativa:** Gerenciamento dos temas Dark e Light controlado via **Variáveis CSS (`:root`)**, garantindo trocas de cores instantâneas e sem atrasos visuais.
- **Micro-interações:** Uso de transições suaves e animações customizadas via `@keyframes`, como o efeito visual de impacto ao atingir um marco de sequência (*Streak Milestone*).

### ⚡ Vanilla JavaScript (ES6+ e Lógica)
A lógica da aplicação é estruturada utilizando padrões modernos de manipulação do DOM e gerenciamento de dados:

- **Centralização de Estado (`AppState`):** Toda a inteligência do app fica encapsulada em um único objeto global de estado, funcionando como uma fonte única de verdade e eliminando conflitos de escopo.
- **Tratamento de Fuso Horário Local:** Funções dedicadas (`getLocalDateString`) para cálculo de datas que previnem bugs de conversão UTC (especialmente ao registrar pontos à noite), garantindo que a data salva seja sempre a local.
- **Persistência e Backup Automático:** Sincronização imediata de dados com o `localStorage`. Conta com uma rotina probabilística que gera **backups preventivos automáticos** em segundo plano durante as operações de salvamento.
- **Manipulação de Arquivos (JSON/CSV):** Uso nativo das APIs `FileReader` e `Blob` do navegador, permitindo a importação e exportação bidirecional de dados em JSON e planilhas CSV.
- **Otimização com Debounce:** O conversor de pontos utiliza uma função de *debounce de 300ms* no campo de entrada, evitando re-renderizações excessivas enquanto o usuário digita valores grandes.
- **Segurança e Sanitização:** Inclusão das funções utilitárias `escapeHtml()` para mitigar brechas de XSS e `validatePositiveNumber()` para blindar os cálculos matemáticos contra valores corrompidos ou negativos.

## 🚀 Como usar

1. Baixe o arquivo **`index.html`**
2. Abra diretamente no seu navegador (Recomendados: Edge ou Chrome, provavelmente funciona no Firefox)
3. Comece a registrar seus pontos diários — tudo é salvo automaticamente e seus dados antigos continuam preservados após as atualizações.

### OU

**Versão online (GitHub Pages):**
→ [https://y4sh1r01.github.io/MSRewardsTool/](https://y4sh1r01.github.io/MSRewardsTool/)

## 📋 Versão Atual, Change-Log, To-Do:

1.2.1

[Ver change-log completo nas Releases](https://github.com/Y4SH1R01/MSRewardsTool/releases)

*To-Do atual:*
- Remover/modificar informações de/e modals como: a antiga descrição das contagens de dias consecutivos com os marcos e bônus reais do MS Rewards Brasil anterior (3º, 8º, 13º, 20º, 27º dia e +150 pts a cada 10 dias após o 34º) e o bônus do baú, já que foram removidos na atualização.
- Adicionar um link direto pro novo Sobre feito pela MS na página do rewards (verificar se precisa estar logado pra visualizar)
- *Pensar em novas melhorias.*

## 📌 Observações

- A ferramenta usa **apenas os dias que você registra** para calcular a média diária e as projeções finais.
- Quanto mais consistente você for em adicionar os pontos, mais precisa fica a projeção da meta.
- No modo automático, o streak conta os dias consecutivos no histórico e **é zerado** se pular um dia. Você pode alternar para o modo manual a qualquer momento clicando em ✏️.

## 🙌 Agradecimentos

Feito com carinho para a comunidade brasileira de caçadores do Microsoft Rewards.

Inspirado originalmente em uma ferramenta mostrada num tweet do usuário [Augusto Masetti](https://x.com/augustomasetti) no X.

Desenvolvido por **Mateus (Y4SH1R01)** com assistência inicial do Grok 4.2.0-Quick Thinking e Specialist. Atualizações da v1.2.0 feitas com auxílio do Kimi-k2.6 e Mistral 3.5b. Correções e features adicionadas na v1.2.1 com auxílio da GLM-5.1.

Se você usa e gosta do projeto, considere dar uma ⭐ no repositório!

---

**Licença:** GPL-3.0

**Última atualização:** Junho de 2026.
