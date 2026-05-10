# 🎨 opendesigner — INCONFORMADOS

## brief

Criar um ecossistema digital de transformação social e formação humana. PWA gamificado para jovens de 12-18 anos em Salvador. O app funciona como: plataforma de evolução pessoal, rede social positiva, sistema de gamificação, ferramenta de acompanhamento comportamental e ambiente educacional/comunitário.

O sistema deve: promover evolução pessoal, estimular disciplina e responsabilidade, criar pertencimento, incentivar impacto social, registrar evolução comportamental e integrar IA inteligente de acompanhamento.

## alma do projeto

- **essência**: Ecossistema digital de transformação social através de gamificação positiva e formação de caráter.
- **público-alvo**: Jovens de 12-18 anos em Salvador, conectados a igrejas/comunidades/escolas. Liderados por mentores, coordenadores e admins.
- **tom/energia**: Energético, motivacional, acolhedor, cristão/valores positivos. NUNCA tóxico, competitivo de forma negativa ou excludente.
- **diferencial**: Foco em formação integral (disciplina, liderança, impacto social), streak de consistência, diário de evolução pessoal com 4 blocos metodológicos, IA de acompanhamento comportamental.

## stack detectada

- linguagem: typescript
- framework: react + vite (planejado)
- runtime: node 25 / bun 1.3
- ui atual: nenhuma (projeto novo)
- banco: supabase (postgresql)
- ia: openai api (moderação + análise comportamental)
- hospedagem: vercel (frontend) + supabase (backend)

## superfícies de design detectadas

### 1. Área do Usuário

- [x] **Home (Tela Inicial)** — saudação, nível, XP, barra de evolução, streak, missão do dia, desafio semanal, progresso mensal, notificações, mensagens da IA
- [x] **Perfil do Usuário** — nome, foto, idade, escola/núcleo, cidade, responsável, nível atual, índice de evolução
- [x] **Dashboard de Evolução** — índice de disciplina, índice social, índice emocional, índice de liderança, participação, desafios concluídos, evolução mensal
- [x] **Linha do Tempo** — histórico cronológico de evolução, atividades, missões, alertas, conquistas, comportamento

### 2. Sistema de Gamificação

- [x] **Sistema de XP** — login diário, desafios, encontros, atividade física, ações sociais, interação positiva, trilhas, streak
- [x] **6 Níveis Visuais** — ⚪ Despertar, 🟢 Construção, 🟡 Posicionamento, 🟠 Influência, 🔴 Liderança, 👑 Voz da Geração
- [x] **Streak System** — 4 tiers: 7 dias, 15 dias, 30 dias, 90 dias (com badges animados)
- [x] **Desafios Semanais** — rotina, disciplina, leitura, atividade física, ação social, espiritualidade
- [x] **Medalhas** — 🥉 Disciplina, 🥈 Influência, 🥇 Liderança, 🏆 Transformação

### 3. Sistema Social

- [x] **Comunidades** — grupos por escola, bairro, núcleo, cidade, equipe
- [x] **Feed Social** — publicar evolução, compartilhar conquistas, comentar, reagir, compartilhar ações sociais
- [x] **Chat** — individual, grupo, envio de mídia, monitorado por IA

### 4. Sistema "Levante Um" (Convite)

- [x] **Tela de Convite** — código compartilhável, status dos convidados
- [x] **Acompanhamento** — cadastro, participação, frequência, evolução dos convidados
- [x] **Perfil de Impacto** — jovens impactados, evolução dos convidados, nível de influência
- [x] **XP Passivo** — ganha XP baseado na permanência e evolução dos convidados

### 5. Diário do Inconformado (4 Blocos)

- [x] **🧠 Consciência** — como estou me sentindo? (emoji picker)
- [x] **⚔️ Confronto** — checklist de disciplina, ações do dia
- [x] **🔥 Ajuste** — reflexões, aprendizados, o que preciso melhorar
- [x] **🚀 Meta** — objetivos para o próximo dia

### 6. Sistema de Missões

- [x] **Missões Diárias** — acordar cedo, evitar reclamação, ajudar alguém, concluir tarefa, autocontrole
- [x] **Missões Mensais** — "Impacte sua geração" (jovens impactados, permanência, evolução coletiva)

### 7. IA Inteligente

- [x] **Moderação de Chat/Feed** — detecta: palavrões, agressividade, bullying, conteúdo impróprio, discurso tóxico
- [x] **Ações Automáticas** — alerta leve, mensagem privada, ocultação automática, encaminhamento ao moderador
- [x] **Acompanhamento Comportamental** — analisa frequência, rotina, engajamento, emocional, disciplina
- [x] **Mensagens Motivacionais** — baseadas no streak e evolução ("Você está pegando fogo!", "Volte ao caminho")
- [x] **Relatórios Automáticos** — semanal, mensal, alertas de comportamento, tendências emocionais

### 8. Painel Administrativo

- [x] **Perfis Admin** — Super Admin, Líder, Escola, Coordenador Comunitário
- [x] **Dashboard Admin** — usuários ativos, engajamento, ranking saudável, risco de evasão, comportamento coletivo
- [x] **Gestão de Usuários** — criar, editar, remover, ver evolução, dar medalhas, ajustar XP
- [x] **Criação de Desafios e Eventos**
- [x] **Moderação de Comunidade**

### 9. Relatórios

- [x] **Relatório Individual** — evolução, comportamento, disciplina, liderança, participação, tendências emocionais
- [x] **Relatório Coletivo** — por escola, núcleo, comunidade, cidade

### 10. Modos Especiais

- [x] **Modo Escola** — acompanhamento escolar, desafios pedagógicos, relatórios educacionais, frequência
- [x] **Modo Responsáveis** — acompanhar evolução, receber alertas, ver participação

### 11. Experiência

- [x] **Evento de Celebração** — "Festa dos Inconformados" mensal com premiações
- [x] **Loading States** — skeletons, toasts, animações motivacionais
- [x] **Onboarding + LGPD** — cadastro com consentimento, proteção de menores

## design system sugerido

**referência principal**: Duolingo meets Discord meets Notion

- Gamificação acessível (não infantil demais, jovem-adulto)
- Dark mode como padrão (atrai o público jovem)
- Cores vibrantes mas não saturadas
- Cards com bordas suaves, sombras sutis
- Micro-interações motivacionais

**paleta de cores**:

| Token | Hex | Uso |
|-------|-----|-----|
| Background | `#0A0A0A` | Fundo principal |
| Surface | `#141414` | Cards, elementos elevados |
| Surface-hover | `#1F1F1F` | Hover states |
| Primary | `#10B981` | Verde — progresso, disciplina, XP |
| Secondary | `#8B5CF6` | Roxo — comunidade, perfil, nível |
| Accent | `#F59E0B` | Amarelo — conquistas, medalhas, streak |
| Warning | `#EF4444` | Vermelho — alertas, atenção |
| Text | `#FAFAFA` | Texto principal |
| Text-muted | `#A1A1AA` | Texto secundário |
| Border | `#27272A` | Bordas sutis |

**níveis por cor**:

| Nível | Emoji | Cor |
|-------|-------|-----|
| Despertar | ⚪ | `#9CA3AF` (cinza) |
| Construção | 🟢 | `#10B981` (verde) |
| Posicionamento | 🟡 | `#F59E0B` (amarelo) |
| Influência | 🟠 | `#F97316` (laranja) |
| Liderança | 🔴 | `#EF4444` (vermelho) |
| Voz da Geração | 👑 | `#8B5CF6` (roxo) |

## skill sugerida

`mobile-app` com foco em PWA gamificado completo

## direção visual

`warm-soft` — energético mas acolhedor. Cores vibrantes em ambiente escuro, cantos arredondados (rounded-xl a rounded-2xl), micro-interações motivacionais. NUNCA brutalista ou frio.

## instruções específicas

### Filosofia de Design

1. **Mobile-first absoluto** — simular tela 390x844px, max-width 430px centralizado em desktop
2. **Bottom Navigation fixa** — 5 tabs: Home, Diário, Feed, Levantar, Perfil (ícones lucide-react)
3. **Dark mode padrão** — backgrounds escuros (#0A0A0A) com texto claro
4. **Gamificação pervasiva** — XP/XP bar em todo lugar, badges visíveis, streak como orgulho
5. **Tom motivacional** — linguagem positiva, nunca acusatória ("Você está evoluindo!" vs "Você falhou")
6. **Hierarquia clara** — o que importa aparece primeiro (nível, streak, missões)

### Componentes do Sistema de Gamificação

```
// XP System
- XPBar (barra com gradiente, % atual, número exato)
- XPBadge (número pequeno com ícone de raio)
- XPGainedToast (+50 XP animation)

// Level System
- LevelBadge (emoji + nome do nível + cor)
- LevelProgress (card mostrando nível atual e próximo)
- LevelUpModal (celebração quando sobe de nível)

// Streak System
- StreakCounter (🔥 + número + texto "dias")
- StreakBadge (7/15/30/90 dias com tier)
- StreakCalendar (grid mostrando dias consecutivos)
- StreakWarningToast (quando está perto de perder)

// Medals/Badges
- MedalCard (emoji + nome + descrição)
- MedalGrid (grid 3 colunas das medalhas conquistadas)
- MedalLocked (versão cinza/bloqueada)
- NewMedalModal (celebração ao desbloquear)

// Missions
- DailyMissions (lista com checkboxes interativos)
- WeeklyChallenge (card destacado do desafio semanal)
- MissionCard (título, XP reward, checkbox, completed state)

// Challenges
- ChallengeCard (nome, descrição, prazo, reward)
- ChallengeProgress (barras de progresso)
```

### Componentes da Área do Usuário

```
// Home
- WelcomeHeader (avatar, saudação "Bom dia, [nome]!", streak atual)
- StatsOverview (4 cards: XP, Nível, Streak, Missões)
- DailyProgress (barra circular do dia)
- TodayMissions (lista de missões com checkbox)
- WeeklyChallengeCard (desafio da semana destacado)
- NotificationsList (IA messages, alertas)
- QuickActions (botões: Diário, Feed, Convidar)

// Perfil
- ProfileHeader (foto grande, nome, nível, núcleo)
- StatsGrid (disciplina, social, emocional, liderança)
- EvolutionChart (gráfico de linha temporal)
- Timeline (feed cronológico de atividades)
- MedalsCollection (grid de medalhas com unlock status)
- EditProfileModal

// Dashboard de Evolução
- RadarChart (6 eixos: disciplina, social, emocional, liderança, participação, impacto)
- MonthlyProgress (barras por semana)
- InsightsList (mensagens da IA sobre evolução)
- AchievementsTimeline
```

### Componentes do Diário (4 Blocos)

```
// DiarioScreen
- EmojiMoodPicker (grid de emojis com seleção)
- BlockConsciência (🧠 emoji + título + emoji picker)
- BlockConfronto (⚔️ emoji + checklist de disciplina)
- BlockAjuste (🔥 emoji + textarea de reflexão)
- BlockMeta (🚀 emoji + input de meta)
- SaveDiaryButton (com loading e toast de XP)
- PastEntriesCalendar (navegar diários passados)
```

### Componentes do Sistema Social

```
// Feed
- NewPostInput ("Compartilhe sua vitória..." placeholder)
- PostCard (autor, avatar, tempo, conteúdo, imagem opcional, selo, likes, comments)
- LikeButton (coração com animação de pulse)
- CommentSection (expandir com lista de comentários)
- CreatePostModal
- SealBadge (badge de evolução no post)

// Comunidades
- CommunityCard (nome, foto, membros, botão entrar)
- CommunityHeader
- CommunityFeed

// Chat
- ChatList (conversas recentes)
- ChatRoom (mensagens, input, send button)
- ChatBubble (mensagem com timestamp)
- AIIoderationNotice ("Mensagem ocultada pela moderação")
```

### Componentes do Sistema "Levante Um"

```
- InviteCodeCard (código grande + botão copiar)
- ShareButtons (WhatsApp, Instagram, etc)
- ImpactedList (lista de amigos convidados com status)
- ImpactStats (jovens impactados, evolução total)
- PassiveXPCard (ganhos passivos por convite)
- InfluenceLevel (nível de influência)
```

### Componentes do Painel Admin

```
// Dashboard Admin
- AdminStatsCards (total usuários, ativos, riscos, engajamento)
- ActiveUsersChart (gráfico de linha)
- RiskAlertList (alertas de comportamento)
- RecentActivityFeed

// User Management
- UsersTable (foto, nome, nível, streak, status)
- UserSearchBar
- UserDetailModal (ver evolução, dar medalhas, ajustar XP, remover)
- BulkActionsToolbar

// Challenge/Event Creation
- CreateChallengeForm
- EventCard

// Moderation
- ModerationQueue (conteúdo reportado)
- AIAlertsList
- UserWarningsList
```

### Componentes de Relatórios

```
- IndividualReportView (gráficos, métricas, IA insights)
- CollectiveReportView (filtro por grupo,导出)
- ExportPDFButton
- WeeklyReportCard
- MonthlyTrendChart
```

### Componentes de Loading e Feedback

```
- SkeletonCard (card pulsante cinza)
- SkeletonList (lista de skeletons)
- Toast (notificação flutuante, auto-dismiss)
- LoadingSpinner
- XPGainedAnimation (+50 XP com animação)
- LevelUpCelebration (confetti + modal)
- PullToRefresh
```

### Componentes de Onboarding

```
- WelcomeSlide (título, ilustração, descrição)
- AuthForm (email, senha, nome, idade)
- LGPDCheckbox (termos obrigatório com link)
- ProfileSetup (foto, núcleo, escola)
- TutorialOverlay (spots educacionais)
```

### Tipografia

- **Headers**: Bold, 20-28px, tracking tight
- **Subheaders**: SemiBold, 16-18px
- **Body**: Regular, 14-16px, line-height 1.5
- **Labels**: Medium, 12px, uppercase para badges
- **Caption**: Regular, 12px, text-muted
- **Usar Inter ou system fonts**

### Ícones

- **Biblioteca**: lucide-react
- **Tamanho padrão**: 20-24px
- **Strokes**: 1.5-2px

### Espaçamento

- Base unit: 4px
- Padding cards: 16px (p-4)
- Gap entre cards: 12px (gap-3)
- Border radius: rounded-xl (12px) para cards, rounded-full para avatares/badges

### Animações

- **Micro-interações**: scale on press (0.97), 150ms
- **Page transitions**: fade 200ms
- **XP gained**: float up + fade, 1s
- **Level up**: confetti burst + modal scale
- **Toast**: slide up from bottom, 300ms

## prompt final para o open-design

---

Crie um PWA gamificado completo chamado "Inconformes" para jovens de 12-18 anos. Mobile-first (390x844px, max-width 430px centralizado), dark mode padrão.

**PALETA DE CORES**:
```
Background: #0A0A0A
Surface: #141414
Surface-hover: #1F1F1F
Primary (verde): #10B981 — progresso, disciplina
Secondary (roxo): #8B5CF6 — comunidade, perfil
Accent (amarelo): #F59E0B — conquistas, streak
Warning (vermelho): #EF4444 — alertas
Text: #FAFAFA
Text-muted: #A1A1AA
Border: #27272A

Níveis: ⚪Despertar #9CA3AF | 🟢Construção #10B981 | 🟡Posicionamento #F59E0B | 🟠Influência #F97316 | 🔴Liderança #EF4444 | 👑Voz da Geração #8B5CF6
```

**TELAS PRINCIPAIS**:

**1. HomeDashboard**
- Header: avatar, "Bom dia, [nome]!", streak com 🔥
- 4 cards de stats: XP atual, Nível, Streak dias, Missões concluídas
- Barra circular de progresso diário
- Card do desafio semanal (destaque amarelo)
- Lista de missões do dia com checkboxes interativos
- Notificações da IA (mensagens motivacionais)
- Quick actions: Diário, Feed, Convidar

**2. PerfilScreen**
- Header: foto grande circular, nome, núcleo/escola, badge de nível
- 4 stats em grid: Disciplina, Social, Emocional, Liderança
- Gráfico de evolução (radar ou linha temporal)
- Timeline de atividades recentes
- Grid de medalhas (3 colunas, desbloqueadas em cor, bloqueadas cinza)
- Botão editar perfil

**3. DiarioScreen (4 blocos metodológicos)**
- **🧠 Consciência**: grid de emojis para humor (😊😐😢😤😴🥰😰💪)
- **⚔️ Confronto**: checklist de disciplina (Acordei no horário ☑️, Evitei reclamação ☑️, Ajudei alguém ☑️)
- **🔥 Ajuste**: textarea para reflexões e aprendizados
- **🚀 Meta**: input para objetivo do próximo dia
- Botão "Salvar Diário" com loading → toast "+50 XP ganhos"
- Calendário para ver diários passados

**4. FeedScreen**
- Campo minimalista no topo: "Compartilhe sua vitória hoje..."
- Post cards com: avatar + nome, timestamp, conteúdo, selo de evolução, ❤️ likes, 💬 comentários
- Pull to refresh
- Filtro por comunidade

**5. LevantarScreen ("Levante Um")**
- Card destacado: "Transforme-se em influência positiva"
- Código de convite grande + botão "Copiar"
- Botões de compartilhar (WhatsApp, Instagram)
- Lista de "Meus Impactados" (avatares + nomes + níveis)
- Card de XP passivo: "Ganhe XP pela evolução dos seus amigos"
- Nível de influência (bar progress)

**6. ChatScreen**
- Lista de conversas (avatar, nome, última mensagem, timestamp)
- Chat individual: bolhas de mensagem, timestamp, input com send
- Badge de moderação da IA quando aplicável

**7. AdminDashboard**
- 4 cards de métricas: Total Jovens, Ativos na Semana, Riscos de Evasão, Engajamento
- Gráfico de engajamento
- Lista de alertas da IA
- Lista de jovens com pesquisa
- Modal de ação: ver evolução, dar medalhas, ajustar XP

**8. OnboardingFlow**
- Tela de boas-vindas (logo, título motivacional)
- Formulário: email, senha, nome completo, idade
- Checkbox LGPD obrigatório ("Li e aceito os Termos de Uso e Política de Privacidade")
- Validação de idade (12-18 anos)
- Tela de criação de perfil (foto, núcleo, escola)

**COMPONENTES REUTILIZÁVEIS**:

```
AppShell — container mobile + bottom nav 5 tabs (Home, Diário, Feed, Levantar, Perfil)
XPBar — barra com gradiente verde→roxo, número de XP
XPBadge — número pequeno com ícone ⚡
LevelBadge — emoji + nome + cor do nível
StreakCounter — 🔥 + número + texto "dias"
StreakBadge — tier 7/15/30/90 dias
MedalCard — emoji + nome + descrição
MedalGrid — grid 3 colunas das medalhas
MissionCard — checkbox + título + XP reward
PostCard — avatar + autor + conteúdo + likes + comentários
ToastNotification — mensagem flutuante com dismiss
SkeletonLoader — card cinza pulsante
StatCard — número grande + label
EmojiPicker — grid de emojis selecionáveis
ProgressRing — círculo de progresso
ChatBubble — mensagem + timestamp
UserSearchBar — input com ícone de lupa
Modal — overlay com card centralizado
```

**ESTILO GERAL**:
- cantos arredondados: rounded-xl (12px) para cards, rounded-full para avatares
- sombras: shadow-sm ou nenhuma
- botões primários: bg-primary (verde), rounded-xl, text-white
- botões secundários: bg-surface, border, rounded-xl
- inputs: bg-surface, border-border, rounded-xl
- NUNCA glassmorphism
- NUNCA métricas negativas (ranking público, "perdeu streak" em destaque)
- TODA linguagem motivacional e positiva
- lucide-react para ícones

---

## ⚠️ restrições

1. **NÃO** usar glassmorphism ou blur excessivo
2. **NÃO** usar cores saturadas demais (sempre muted/dark)
3. **NÃO** criar ranking público ou competição tóxica
4. **NÃO** mostrar "perdeu streak" em destaque — streak perdido é informação privada
5. **NÃO** infantilizar — jovens de 14-18 anos, tom jovem-adulto
6. **NÃO** usar linguagem acusatória ("Você falhou", "Você está mal")
7. **SEMPRE** usar linguagem motivacional ("Você está evoluindo!", "Continue assim!")
8. **PRESERVAR** mobile-first em TODAS as telas
9. **PRESERVAR** dark mode como padrão
10. **TODAS** as telas devem funcionar em 390x844px sem scroll horizontal