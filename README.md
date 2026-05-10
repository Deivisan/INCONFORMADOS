# 🔥 INCONFORMADOS

> Ecossistema digital de transformação social e formação humana para jovens.

## 📱 Sobre

Plataforma gamificada de evolução pessoal, desenvolvimento e engajamento comunitário voltada para jovens de 12-18 anos em Salvador.

O aplicativo funciona como:
- 🔥 Plataforma de evolução pessoal
- 🔥 Rede social positiva
- 🔥 Sistema de gamificação (XP, níveis, streak, medalhas)
- 🔥 Ferramenta de acompanhamento comportamental
- 🔥 Ambiente educacional e comunitário
- 🔥 Diário de evolução com 4 blocos metodológicos
- 🔥 IA inteligente de acompanhamento e moderação

## 🎯 Funcionalidades

| Módulo | Features |
|--------|----------|
| **Área do Usuário** | Home com gamificação, perfil completo, dashboard de evolução, linha do tempo |
| **Sistema de Gamificação** | XP, 6 níveis (Despertar → Voz da Geração), streak, desafios, medalhas |
| **Sistema Social** | Feed comunitário, comunidades, chat monitorado por IA |
| **Sistema "Levante Um"** | Convite de amigos, XP passivo, perfil de impacto |
| **Diário do Inconformado** | 4 blocos: Consciência, Confronto, Ajuste, Meta |
| **Missões** | Diárias e mensais, com recompensas de XP |
| **IA Inteligente** | Moderação de conteúdo, acompanhamento comportamental, mensagens motivacionais |
| **Painel Admin** | 4 perfis (Super Admin, Líder, Escola, Coordenador), dashboard, relatórios |
| **Relatórios** | Individual e coletivo, tendências, alertas |
| **Segurança** | LGPD, consentimento, proteção de menores |

## 🏗️ Stack Técnica

- **Frontend**: React + Vite + TypeScript + Tailwind CSS
- **Backend**: Supabase (PostgreSQL, Auth, Realtime, Edge Functions)
- **IA**: OpenAI API (moderação + análise comportamental)
- **Hospedagem**: Vercel (frontend) + Supabase Cloud
- **Formato**: PWA (Progressive Web App) - mobile-first

## 📁 Estrutura do Repo

```
INCONFORMADOS/
├── opendesigner.md    # 🎨 Prompt master para open-design (design system + componentes)
├── guia.md            # 📖 Guia completo de vibe coding (setup, build, mock data, schema)
├── proposta.md        # 📝 Proposta técnica e comercial
└── README.md          # 📄 Este arquivo
```

## 🚀 Começando

1. Leia o `opendesigner.md` e cole o prompt no [open-design](https://github.com/nexu-io/open-design)
2. Iterate o design até满意
3. Siga o `guia.md` para criar o projeto

```bash
# Setup inicial
bun create vite inconformados --template react-ts
cd inconformados
bun add tailwindcss @tailwindcss/vite lucide-react
```

## 📅 Roadmap

| Fase | Descrição | Status |
|------|-----------|--------|
| **MVP** | Cadastro, Gamificação, Diário, Feed, Admin básico, IA básica | 🚧 Em progresso |
| **v2** | Chat, Comunidades, Modo Escola, Relatórios avançados, IA emocional | 📋 Planejado |

## 💰 Investimento

- **Desenvolvimento**: R$ 2.800,00 (3 meses)
- **Manutenção mensal**: R$ 300,00 (hospedagem + suporte + IA)

## 🔗 Links Úteis

- [open-design](https://github.com/nexu-io/open-design)
- [Supabase](https://supabase.com/)
- [Tailwind CSS](https://tailwindcss.com/)
- [lucide-react](https://lucide.dev/)
- [Vite PWA](https://vite-pwa.latuvi.com/)