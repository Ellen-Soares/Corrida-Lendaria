# 🏎️ Corrida Lendária — Hall da Fama da Fórmula 1

Projeto acadêmico desenvolvido como uma aplicação web interativa sobre o universo da Fórmula 1, voltada para pessoas leigas que querem aprender de forma envolvente sobre a história, os pilotos, as tecnologias e as regras da categoria.

> **Status:** projeto acadêmico / portfólio pessoal

---

## 📖 Sobre o projeto

**Corrida Lendária** é um site educativo e interativo sobre Fórmula 1, criado para aproximar o público geral do esporte através de conteúdo visual, histórias marcantes e um mini-game de corrida em 3D. O objetivo foi unir aprendizado e entretenimento, apresentando de forma acessível a trajetória de pilotos lendários, a evolução dos carros e os bastidores técnicos de um fim de semana de corrida.

### 🎯 Público-alvo

Pessoas sem conhecimento aprofundado sobre Fórmula 1, mas curiosas sobre a história e a cultura do esporte.

---

## ✨ Funcionalidades

| Seção | Descrição |
|---|---|
| 🏁 **Hall da Fama** | Histórias e conquistas de pilotos que marcaram a F1 (Ayrton Senna, Michael Schumacher, Fernando Alonso, Lewis Hamilton, Max Verstappen, Niki Lauda, entre outros) |
| 🚗 **Grid 2026** | Apresentação das equipes e carros da temporada, com visual dos modelos |
| 🔧 **Motores** | Linha do tempo dos motores/fabricantes que fizeram história na categoria (Ferrari, Honda, Mercedes, Renault, Cosworth, BMW...) |
| 📰 **News Ticker** | Faixa de notícias em tempo real com link direto para acompanhamento externo (ESPN F1) |
| 🏆 **Top 10 / Ultrapassagens** | Momentos e ultrapassagens icônicas da história da F1 |
| ⚙️ **Tecnologia** | Exploração interativa do volante de F1, simulação de túnel de vento e explicação sobre pneus |
| 📅 **Race Week** | Explicação didática da rotina de um fim de semana de corrida (treinos, classificação, corrida) |
| 🎮 **Jogo (Pole Position)** | Mini-game de corrida em canvas, com obstáculos, combustível, sistema de pontuação e pódio final |
| 🎵 **Áudio ambiente** | Trilha sonora ambiente para imersão na experiência |

---

## 🛠️ Tecnologias utilizadas

- **[React 18](https://react.dev/)** + **[TypeScript](https://www.typescriptlang.org/)**
- **[Vite](https://vitejs.dev/)** — build tool e dev server
- **[Tailwind CSS](https://tailwindcss.com/)** — estilização
- **[shadcn/ui](https://ui.shadcn.com/)** + **Radix UI** — componentes de interface acessíveis
- **[React Three Fiber](https://docs.pmnd.rs/react-three-fiber)** + **[Three.js](https://threejs.org/)** — renderização 3D (carros e volante)
- **[React Router DOM](https://reactrouter.com/)** — roteamento
- **[Supabase](https://supabase.com/)** — backend (armazenamento de recordes do jogo)
- **[TanStack Query](https://tanstack.com/query)** — gerenciamento de estado assíncrono
- **[Vitest](https://vitest.dev/)** + **Testing Library** — testes
- **ESLint** — padronização de código

> O projeto foi originalmente criado com o apoio da plataforma [Lovable](https://lovable.dev/) e evoluído manualmente a partir daí.

---

## 🚀 Como rodar o projeto localmente

### Pré-requisitos

- [Node.js](https://nodejs.org/) 18 ou superior
- npm (ou [bun](https://bun.sh/), já que o projeto também possui `bun.lockb`)

### Passo a passo

```bash
# 1. Clone o repositório
git clone https://github.com/seu-usuario/corrida-lendaria.git

# 2. Acesse a pasta do projeto
cd corrida-lendaria

# 3. Instale as dependências
npm install

# 4. Configure as variáveis de ambiente
cp .env.example .env
# Preencha o .env com as credenciais do seu projeto Supabase

# 5. Rode o projeto em modo desenvolvimento
npm run dev
```

O site estará disponível em `http://localhost:5173` (porta padrão do Vite).

### Outros scripts disponíveis

```bash
npm run build       # gera a build de produção
npm run preview     # pré-visualiza a build de produção
npm run lint        # roda o linter
npm run test        # executa os testes
npm run test:watch  # executa os testes em modo watch
```

---

## 🔐 Variáveis de ambiente

O projeto utiliza o Supabase apenas para persistir os recordes do mini-game. As variáveis necessárias estão listadas em [`.env.example`](./.env.example):

```
VITE_SUPABASE_PROJECT_ID=
VITE_SUPABASE_PUBLISHABLE_KEY=
VITE_SUPABASE_URL=
```

> ⚠️ Nunca versione seu arquivo `.env` real — ele já está incluído no `.gitignore`.

---

## 📁 Estrutura do projeto

```
src/
├── assets/            # imagens dos pilotos, carros e motores
├── components/
│   ├── ui/            # componentes de interface (shadcn/ui)
│   ├── Legends.tsx     # Hall da Fama dos pilotos
│   ├── Grid2026.tsx    # equipes e carros da temporada
│   ├── Engines.tsx     # linha do tempo de motores
│   ├── Overtakes.tsx   # ultrapassagens históricas
│   ├── Tech.tsx         # aba de tecnologia (volante, túnel de vento, pneus)
│   ├── SteeringWheel.tsx
│   ├── WindTunnel.tsx
│   ├── Tyres.tsx
│   ├── RaceWeek.tsx    # explicação do fim de semana de corrida
│   ├── Game.tsx         # mini-game de corrida
│   ├── Podium.tsx       # pódio final do jogo
│   ├── NewsTicker.tsx   # faixa de notícias
│   └── NavBar.tsx       # navegação entre seções
├── data/               # dados estáticos (lendas, motores, grid, notícias, pistas)
├── hooks/              # hooks customizados
├── integrations/
│   └── supabase/       # cliente e tipos do Supabase
├── pages/
│   ├── Index.tsx        # página principal (controla qual seção é exibida)
│   └── NotFound.tsx
└── lib/                # utilitários
```

Mais detalhes técnicos em [docs/ARQUITETURA.md](./docs/ARQUITETURA.md).

---

## 🎓 Contexto acadêmico

Este projeto foi desenvolvido como atividade acadêmica, com foco em:

- Aplicar conceitos de desenvolvimento front-end moderno (React + TypeScript)
- Explorar renderização 3D no navegador com Three.js
- Praticar organização de componentes e dados em uma aplicação React de médio porte
- Criar uma experiência educativa e interativa sobre um tema de interesse pessoal

---

## 🤝 Contribuindo

Contribuições são bem-vindas! Veja o guia em [CONTRIBUTING.md](./CONTRIBUTING.md).

## 📄 Licença

Este projeto está sob a licença MIT — veja o arquivo [LICENSE](./LICENSE) para mais detalhes.

## 👤 Autor

Desenvolvido como projeto acadêmico.
Sinta-se à vontade para abrir uma *issue* ou entrar em contato para sugestões.
