# 🔥 Inconformados — Guia de Vibe Coding (PWA)

> Ecossistema digital de transformação social e formação humana.

## 📋 Como Usar Este Guia

1. Copie o **prompt final** do `opendesigner.md`
2. Cole no [open-design](https://github.com/nexu-io/open-design)
3. Iterate até满意 (satisfeito)
4. Copie o código gerado para `/src/screens/`
5. Compose no AppShell

---

## 🎯 Estratégia MVP vs Versão Completa

| Fase | Escopo | Prazo |
|------|--------|-------|
| **MVP** | Cadastro, Perfil, Gamificação, Desafios, Diário, Feed, Admin básico, IA básica | 3 meses |
| **v2** | IA avançada, Relatórios inteligentes, Modo Escola, Sistema de Liderança, Análise emocional | Pós-lançamento |

### Enxugamentos do MVP

- **IA no MVP**: Passiva (mensagens motivacionais baseadas em streak) + moderação de chat via Supabase Edge Function (OpenAI)
- **Chat no MVP**: Apenas feed social, chat individual/group fica para v2
- **Modo Escola/Responsável**: v2
- **Comunidades**: v2
- **Relatórios avançados**: v2
- **XP Hardcoded**: Mock data no front-end, integra Supabase depois

---

## 🏗️ Estrutura de Pastas

```
inconformados/
├── src/
│   ├── components/
│   │   ├── ui/                    # Componentes base
│   │   │   ├── Button.tsx
│   │   │   ├── Card.tsx
│   │   │   ├── Input.tsx
│   │   │   ├── Modal.tsx
│   │   │   ├── Toast.tsx
│   │   │   ├── Skeleton.tsx
│   │   │   ├── Avatar.tsx
│   │   │   └── Badge.tsx
│   │   ├── gamification/         # Sistema de XP
│   │   │   ├── XPBar.tsx
│   │   │   ├── XPBadge.tsx
│   │   │   ├── LevelBadge.tsx
│   │   │   ├── StreakCounter.tsx
│   │   │   ├── StreakBadge.tsx
│   │   │   ├── MedalCard.tsx
│   │   │   └── MedalGrid.tsx
│   │   ├── mission/              # Missões
│   │   │   ├── MissionCard.tsx
│   │   │   ├── DailyMissions.tsx
│   │   │   └── WeeklyChallenge.tsx
│   │   ├── diario/              # Diário
│   │   │   ├── MoodPicker.tsx
│   │   │   ├── DisciplineChecklist.tsx
│   │   │   ├── ReflectionTextarea.tsx
│   │   │   └── MetaInput.tsx
│   │   └── layout/              # Layout
│   │       ├── AppShell.tsx
│   │       ├── BottomNav.tsx
│   │       └── Header.tsx
│   ├── screens/
│   │   ├── onboarding/           # Fluxo de cadastro
│   │   │   ├── WelcomeScreen.tsx
│   │   │   ├── AuthScreen.tsx
│   │   │   └── ProfileSetup.tsx
│   │   ├── HomeScreen.tsx
│   │   ├── DiarioScreen.tsx
│   │   ├── FeedScreen.tsx
│   │   ├── LevantarScreen.tsx
│   │   ├── ChatScreen.tsx        # v2
│   │   ├── ProfileScreen.tsx
│   │   └── admin/               # Painel Admin
│   │       ├── DashboardAdmin.tsx
│   │       ├── UsersAdmin.tsx
│   │       ├── ChallengesAdmin.tsx
│   │       └── ModerationAdmin.tsx
│   ├── hooks/
│   │   ├── useAuth.ts
│   │   ├── useXP.ts
│   │   ├── useStreak.ts
│   │   ├── useMissions.ts
│   │   └── useToast.ts
│   ├── lib/
│   │   ├── supabase.ts
│   │   ├── xp.ts
│   │   ├── levels.ts
│   │   └── mockData.ts
│   ├── contexts/
│   │   ├── AuthContext.tsx
│   │   ├── XPContext.tsx
│   │   └── ThemeContext.tsx
│   ├── types/
│   │   └── index.ts
│   ├── App.tsx
│   └── main.tsx
├── public/
│   ├── manifest.json
│   ├── icons/
│   └── sw.js                    # Service Worker
├── supabase/
│   ├── migrations/
│   └── functions/
│       └── moderate-content/    # Edge Function IA
└── package.json
```

---

## 🚀 Fluxo de Build

### Fase 1: Setup + Design System (Semana 1-2)

```bash
# Criar projeto
bun create vite inconformados --template react-ts
cd inconformados

# Dependências core
bun add tailwindcss @tailwindcss/vite lucide-react clsx

# Dependências de estado
bun add zustand

# PWA
bun add vite-plugin-pwa

# Inicializar Tailwind
bunx tailwindcss init -p
```

**Config tailwind.config.js**:
```js
export default {
  content: ['./index.html', './src/**/*.{js,ts,jsx,tsx}'],
  theme: {
    extend: {
      colors: {
        background: '#0A0A0A',
        surface: '#141414',
        'surface-hover': '#1F1F1F',
        primary: '#10B981',
        secondary: '#8B5CF6',
        accent: '#F59E0B',
        warning: '#EF4444',
        border: '#27272A',
      },
      borderRadius: {
        xl: '12px',
        '2xl': '16px',
      },
    },
  },
  plugins: [],
};
```

### Fase 2: Layout Base + Onboarding (Semana 3-4)

**Entregas**:
- [ ] AppShell com Bottom Navigation (5 tabs)
- [ ] Tema dark configurado
- [ ] Tela de Boas-vindas
- [ ] Tela de Cadastro/Login
- [ ] Checkbox LGPD funcional
- [ ] Validação de idade (12-18)
- [ ] Mock de auth funcionando

### Fase 3: Dashboard + Gamificação (Semana 5-7)

**Entregas**:
- [ ] Home com XP bar e streak
- [ ] Sistema de 6 níveis com cores
- [ ] Missões diárias com checkboxes
- [ ] Desafio semanal
- [ ] Toast de "+50 XP"
- [ ] Modal de level up

### Fase 4: Diário (Semana 8)

**Entregas**:
- [ ] 4 blocos metodológicos completos
- [ ] Emoji mood picker
- [ ] Checklist de disciplina
- [ ] Salvar com XP toast
- [ ] Calendário de diários passados

### Fase 5: Feed Social (Semana 9-10)

**Entregas**:
- [ ] Campo de postar
- [ ] Post cards com likes
- [ ] Comentários (v2: chat)
- [ ] Pull to refresh
- [ ] Mock de posts

### Fase 6: Perfil + Levantar (Semana 11)

**Entregas**:
- [ ] Perfil com stats
- [ ] Grid de medalhas
- [ ] Linha do tempo
- [ ] Código de convite
- [ ] Lista de impactados

### Fase 7: Admin + Polish (Semana 12)

**Entregas**:
- [ ] Dashboard admin com métricas
- [ ] Lista de usuários
- [ ] Modal de ações
- [ ] Skeleton loaders
- [ ] PWA manifest + service worker

---

## 📁 Mock Data Structure

```typescript
// types/index.ts
export interface User {
  id: string;
  name: string;
  email: string;
  age: number;
  avatar: string;
  nucleus: string;
  school: string;
  level: Level;
  xp: { current: number; max: number };
  streak: number;
  stats: {
    discipline: number;
    social: number;
    emotional: number;
    leadership: number;
  };
  medals: Medal[];
  createdAt: string;
}

export interface Level {
  id: number;
  emoji: string;
  name: string;
  color: string;
  minXP: number;
}

export interface Medal {
  id: string;
  emoji: string;
  name: string;
  description: string;
  tier: 'bronze' | 'silver' | 'gold' | 'diamond';
  unlocked: boolean;
  unlockedAt?: string;
}

export interface Mission {
  id: string;
  title: string;
  description: string;
  xp: number;
  type: 'daily' | 'weekly';
  completed: boolean;
  deadline?: string;
}

export interface DiaryEntry {
  id: string;
  userId: string;
  date: string;
  mood: string;
  discipline: {
    wokeUpOnTime: boolean;
    avoidedComplaints: boolean;
    helpedSomeone: boolean;
    finishedTasks: boolean;
    practicedSelfControl: boolean;
  };
  reflection: string;
  goal: string;
  xpEarned: number;
}

export interface Post {
  id: string;
  authorId: string;
  author: Pick<User, 'name' | 'avatar' | 'level'>;
  content: string;
  image?: string;
  seal?: string;
  likes: number;
  likedBy: string[];
  comments: Comment[];
  createdAt: string;
}

export interface Comment {
  id: string;
  authorId: string;
  author: Pick<User, 'name' | 'avatar'>;
  content: string;
  createdAt: string;
}
```

```typescript
// lib/mockData.ts

export const LEVELS = [
  { id: 1, emoji: '⚪', name: 'Despertar', color: '#9CA3AF', minXP: 0 },
  { id: 2, emoji: '🟢', name: 'Construção', color: '#10B981', minXP: 500 },
  { id: 3, emoji: '🟡', name: 'Posicionamento', color: '#F59E0B', minXP: 1500 },
  { id: 4, emoji: '🟠', name: 'Influência', color: '#F97316', minXP: 3500 },
  { id: 5, emoji: '🔴', name: 'Liderança', color: '#EF4444', minXP: 7000 },
  { id: 6, emoji: '👑', name: 'Voz da Geração', color: '#8B5CF6', minXP: 15000 },
];

export const MEDALS = [
  { id: '1', emoji: '🔥', name: 'Primeiros Passos', description: 'Concluiu o primeiro diário', tier: 'bronze', unlocked: true },
  { id: '2', emoji: '📖', name: 'Leitor', description: '5 diários completados', tier: 'bronze', unlocked: true },
  { id: '3', emoji: '💪', name: 'Disciplinado', description: '7 dias de streak', tier: 'silver', unlocked: true },
  { id: '4', emoji: '🌟', name: 'Impacto', description: 'Convidou o primeiro amigo', tier: 'silver', unlocked: false },
  { id: '5', emoji: '👑', name: 'Líder', description: '30 dias de streak', tier: 'gold', unlocked: false },
  { id: '6', emoji: '🏆', name: 'Transformação', description: '90 dias de streak', tier: 'diamond', unlocked: false },
];

export const DAILY_MISSIONS = [
  { id: '1', title: 'Diário matinal', description: 'Registre como você está', xp: 20, completed: false },
  { id: '2', title: 'Evite reclamações', description: 'Sem reclamar o dia inteiro', xp: 15, completed: false },
  { id: '3', title: 'Ajude alguém', description: 'Faça uma boa ação hoje', xp: 30, completed: false },
  { id: '4', title: 'Conclua uma tarefa', description: 'Termine algo que precisa fazer', xp: 20, completed: false },
  { id: '5', title: 'Pratique autocontrole', description: 'Mantenha a calma sob pressão', xp: 25, completed: false },
];

export const WEEKLY_CHALLENGE = {
  title: 'Semana da Disciplina',
  description: 'Complete todas as missões diárias desta semana',
  reward: 200,
  progress: 3,
  total: 7,
  deadline: '2024-01-21',
};

export const mockUser: User = {
  id: '1',
  name: 'João Silva',
  email: 'joao@email.com',
  age: 15,
  avatar: 'https://api.dicebear.com/7.x/avataaars/svg?seed=joao',
  nucleus: 'Igreja Central',
  school: 'Colégio Batista',
  level: LEVELS[1],
  xp: { current: 1200, max: 2000 },
  streak: 5,
  stats: {
    discipline: 78,
    social: 65,
    emotional: 82,
    leadership: 45,
  },
  medals: MEDALS,
  createdAt: '2024-01-01',
};

export const mockPosts: Post[] = [
  {
    id: '1',
    authorId: '2',
    author: { name: 'Maria Santos', avatar: 'https://api.dicebear.com/7.x/avataaars/svg?seed=maria', level: LEVELS[2] },
    content: 'Consegui acordar cedo todos os dias desta semana! Estou orgulhosa do meu progresso 🏆',
    seal: 'Disciplina',
    likes: 24,
    likedBy: ['1', '3'],
    comments: [
      { id: 'c1', authorId: '3', author: { name: 'Pedro', avatar: 'https://api.dicebear.com/7.x/avataaars/svg?seed=pedro' }, content: 'Isso aí! Continue assim!', createdAt: '2h' },
    ],
    createdAt: '2h',
  },
  {
    id: '2',
    authorId: '4',
    author: { name: 'Lucas Oliveira', avatar: 'https://api.dicebear.com/7.x/avataaars/svg?seed=lucas', level: LEVELS[1] },
    content: 'Terminei de ler o livro que meu líder indicou. Recomendo muito! 📚',
    seal: 'Leitor',
    likes: 18,
    likedBy: ['1'],
    comments: [],
    createdAt: '5h',
  },
];

export const mockImpacted = [
  { id: '1', name: 'Ana Costa', avatar: 'https://api.dicebear.com/7.x/avataaars/svg?seed=ana', level: LEVELS[0], status: 'active' },
  { id: '2', name: 'Carlos Reis', avatar: 'https://api.dicebear.com/7.x/avataaars/svg?seed=carlos', level: LEVELS[1], status: 'active' },
  { id: '3', name: 'Julia Mendes', avatar: 'https://api.dicebear.com/7.x/avataaars/svg?seed=julia', level: LEVELS[0], status: 'inactive' },
];
```

---

## 🎨 XP System

```typescript
// lib/xp.ts

export const XP_ACTIONS = {
  dailyLogin: 10,
  completeDiary: 50,
  completeMission: 20,
  helpSomeone: 30,
  weeklyChallenge: 200,
  inviteFriend: 100,
  friendLevelUp: 50,
  streak7: 100,
  streak15: 250,
  streak30: 500,
  streak90: 1000,
};

export function calculateLevel(xp: number): typeof LEVELS[number] {
  for (let i = LEVELS.length - 1; i >= 0; i--) {
    if (xp >= LEVELS[i].minXP) {
      return LEVELS[i];
    }
  }
  return LEVELS[0];
}

export function getXPProgress(xp: number): { current: number; max: number; percentage: number } {
  const level = calculateLevel(xp);
  const nextLevel = LEVELS[level.id] || LEVELS[LEVELS.length - 1];
  const currentInLevel = xp - level.minXP;
  const neededForLevel = nextLevel.minXP - level.minXP;
  
  return {
    current: currentInLevel,
    max: neededForLevel,
    percentage: Math.min((currentInLevel / neededForLevel) * 100, 100),
  };
}
```

---

## 📊 Estrutura do Supabase (Schema)

```sql
-- Tabelas principais para MVP

-- Perfis de usuário
create table profiles (
  id uuid references auth.users primary key,
  name text not null,
  email text not null unique,
  age integer check (age >= 12 and age <= 18),
  avatar text,
  nucleus text,
  school text,
  parent_name text,
  parent_contact text,
  role text default 'user' check (role in ('user', 'leader', 'admin', 'super_admin')),
  xp integer default 0,
  streak integer default 0,
  last_login date,
  created_at timestamp default now()
);

-- Níveis
create table levels (
  id serial primary key,
  name text not null,
  emoji text not null,
  color text not null,
  min_xp integer not null
);

-- Medalhas
create table medals (
  id serial primary key,
  emoji text not null,
  name text not null,
  description text,
  tier text check (tier in ('bronze', 'silver', 'gold', 'diamond'))
);

-- Medalhas conquistadas
create table user_medals (
  user_id uuid references profiles,
  medal_id integer references medals,
  unlocked_at timestamp default now(),
  primary key (user_id, medal_id)
);

-- Missões diárias
create table daily_missions (
  id serial primary key,
  title text not null,
  description text,
  xp integer default 20,
  active boolean default true
);

-- Missões concluídas
create table completed_missions (
  user_id uuid references profiles,
  mission_id integer references daily_missions,
  completed_at timestamp default now(),
  primary key (user_id, mission_id)
);

-- Desafios semanais
create table weekly_challenges (
  id serial primary key,
  title text not null,
  description text,
  reward_xp integer,
  start_date date,
  end_date date,
  active boolean default true
);

-- Diário
create table diary_entries (
  id uuid primary key default gen_random_uuid(),
  user_id uuid references profiles,
  date date not null,
  mood text,
  woke_up_on_time boolean default false,
  avoided_complaints boolean default false,
  helped_someone boolean default false,
  finished_tasks boolean default false,
  practiced_self_control boolean default false,
  reflection text,
  goal text,
  xp_earned integer default 50,
  created_at timestamp default now(),
  unique (user_id, date)
);

-- Posts do feed
create table posts (
  id uuid primary key default gen_random_uuid(),
  user_id uuid references profiles,
  content text not null,
  image text,
  seal text,
  likes_count integer default 0,
  created_at timestamp default now()
);

-- Likes em posts
create table post_likes (
  user_id uuid references profiles,
  post_id uuid references posts,
  primary key (user_id, post_id)
);

-- Comentários
create table comments (
  id uuid primary key default gen_random_uuid(),
  post_id uuid references posts,
  user_id uuid references profiles,
  content text not null,
  created_at timestamp default now()
);

-- Convites (Levante Um)
create table invites (
  id uuid primary key default gen_random_uuid(),
  inviter_id uuid references profiles,
  invite_code text unique not null,
  created_at timestamp default now()
);

-- Convites aceitos
create table invite_acceptances (
  invite_id uuid references invites,
  invited_id uuid references profiles,
  primary key (invite_id, invited_id)
);

-- IA Moderação (Edge Function)
-- Supabase Edge Function que usa OpenAI para moderar conteúdo

-- Row Level Security (RLS)
alter table profiles enable row level security;
alter table diary_entries enable row level security;
alter table posts enable row level security;

-- Políticas básicas
create policy "Users can view all profiles" on profiles for select using (true);
create policy "Users can update own profile" on profiles for update using (auth.uid() = id);
create policy "Users can insert own diary" on diary_entries for insert with check (auth.uid() = user_id);
create policy "Users can view own diary" on diary_entries for select using (auth.uid() = user_id);
create policy "Leaders can view team diary" on diary_entries for select using (
  exists (select 1 from profiles where id = auth.uid() and role in ('leader', 'admin', 'super_admin'))
);
```

---

## 🤖 IA - Moderação (Supabase Edge Function)

```typescript
// supabase/functions/moderate-content/index.ts

import { serve } from 'https://deno.land/std@0.168.0/http/server.ts'
import { createClient } from 'https://esm.sh/@supabase/supabase-js@2'

const OPENAI_API_KEY = Deno.env.get('OPENAI_API_KEY')!

serve(async (req) => {
  const { content, userId, type } = await req.json()
  
  // Chamada para OpenAI Moderation
  const response = await fetch('https://api.openai.com/v1/moderations', {
    method: 'POST',
    headers: {
      'Authorization': `Bearer ${OPENAI_API_KEY}`,
      'Content-Type': 'application/json',
    },
    body: JSON.stringify({ input: content }),
  })
  
  const moderation = await response.json()
  const flagged = moderation.results[0].flagged
  
  if (flagged) {
    // Registrar alerta
    // Ocultar conteúdo ou enviar warning
  }
  
  return new Response(JSON.stringify({ 
    approved: !flagged,
    categories: moderation.results[0].categories 
  }))
})
```

---

## 📱 PWA Setup

```json
// public/manifest.json
{
  "name": "Inconformados",
  "short_name": "Inconformados",
  "description": "Plataforma de evolução pessoal e transformação social",
  "start_url": "/",
  "display": "standalone",
  "background_color": "#0A0A0A",
  "theme_color": "#10B981",
  "icons": [
    { "src": "/icons/icon-192.png", "sizes": "192x192", "type": "image/png" },
    { "src": "/icons/icon-512.png", "sizes": "512x512", "type": "image/png" }
  ]
}
```

---

## 🔗 Recursos

- [open-design](https://github.com/nexu-io/open-design)
- [lucide-react](https://lucide.dev/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Supabase](https://supabase.com/)
- [Vite PWA](https://vite-pwa.latuvi.com/)
- [DiceBear Avatars](https://dicebear.com/) — Avatares mock