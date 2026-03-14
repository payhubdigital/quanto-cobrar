# 💰 Quanto Cobrar?

### Calculadora inteligente de precificação para freelancers e autônomos brasileiros.

**Pare de chutar seus preços. Descubra quanto você realmente deveria cobrar.**
---

## 😰 O Problema

> **87% dos freelancers brasileiros cobram menos do que deveriam.**

Milhões de autônomos e freelancers enfrentam a mesma dor todos os dias:

- ❌ Não sabem quanto cobrar pelo seu trabalho
- ❌ Cobram barato demais e não pagam as contas
- ❌ Perdem clientes por não saber justificar o preço
- ❌ Usam o "achismo" em vez de dados reais
- ❌ Esquecem de calcular impostos, férias e custos invisíveis

O **Quanto Cobrar?** resolve isso em **2 minutos**.

---

## ✅ A Solução

Uma calculadora inteligente que considera **todos os fatores** que freelancers
esquecem na hora de precificar:
Custos fixos + Custos variáveis + Impostos + Férias + Horas improdutivas

Reserva de emergência + Meta de renda = SEU PREÇO IDEAL
text


Não é uma calculadora genérica. É um **consultor de precificação de bolso**
feito para a realidade brasileira.

---

## 🎯 Funcionalidades

### 🆓 Gratuito
- [x] Cálculo personalizado por profissão (+50 categorias)
- [x] 3 faixas de preço: Mínimo 🔴 | Saudável 🟡 | Ideal 🟢
- [x] Cálculo automático de impostos (MEI / Simples / Informal)
- [x] Ajuste por cidade e custo de vida regional
- [x] Quantos clientes você precisa por mês
- [x] Frase pronta para enviar ao cliente justificando o preço
- [x] Card compartilhável para redes sociais

### 💎 Premium
- [ ] Tabela de preços completa personalizada por serviço
- [ ] Simulador "E se?" (cenários de preço)
- [ ] Comparativo com a média da sua região
- [ ] Export em PDF profissional
- [ ] Scripts de negociação (quando pedem desconto)
- [ ] Alerta de reajuste anual (baseado no IPCA)
- [ ] Histórico de evolução dos seus preços

---

## 🖥️ Preview

| Landing Page | Formulário | Resultado |
|:---:|:---:|:---:|
| ![Landing](./docs/landing.png) | ![Form](./docs/form.png) | ![Result](./docs/result.png) |

---

## 🛠️ Tech Stack

| Camada | Tecnologia |
|---|---|
| **Frontend** | React / Next.js |
| **Estilização** | Tailwind CSS |
| **Ícones** | Lucide Icons |
| **Gráficos** | Recharts |
| **Backend** | Node.js / API Routes |
| **Banco de dados** | Supabase / PostgreSQL |
| **Autenticação** | Supabase Auth |
| **Pagamento** | Stripe |
| **Deploy** | Vercel |
| **Analytics** | Plausible |

---

## 🚀 Rodando Localmente

### Pré-requisitos

- Node.js 18+
- npm ou yarn
- Conta no Supabase (opcional para dev)

### Instalação

```bash
# Clone o repositório
git clone https://github.com/payhubdigital/quanto-cobrar.git

# Entre na pasta
cd quanto-cobrar

# Instale as dependências
npm install

# Configure as variáveis de ambiente
cp .env.example .env.local

# Rode o projeto
npm run dev
Acesse http://localhost:3000 🎉

Variáveis de Ambiente
env

# .env.local
NEXT_PUBLIC_SUPABASE_URL=sua_url_aqui
NEXT_PUBLIC_SUPABASE_ANON_KEY=sua_chave_aqui
STRIPE_SECRET_KEY=sua_chave_stripe
NEXT_PUBLIC_APP_URL=http://localhost:3000
📁 Estrutura do Projeto
text

quanto-cobrar/
├── public/
│   └── images/
├── src/
│   ├── app/
│   │   ├── page.tsx              # Landing page
│   │   ├── calculadora/
│   │   │   └── page.tsx          # Formulário wizard
│   │   ├── resultado/
│   │   │   └── page.tsx          # Dashboard de resultado
│   │   └── api/
│   │       ├── calcular/         # Lógica de cálculo
│   │       └── compartilhar/     # Geração de card
│   ├── components/
│   │   ├── ui/                   # Componentes base
│   │   ├── forms/                # Steps do formulário
│   │   ├── charts/               # Gráficos do resultado
│   │   └── layout/               # Header, Footer
│   ├── lib/
│   │   ├── calculos.ts           # Engine de precificação
│   │   ├── profissoes.ts         # Base de profissões
│   │   ├── impostos.ts           # Cálculo tributário
│   │   └── custoDeVida.ts        # Índices por cidade
│   ├── hooks/
│   └── types/
├── docs/
├── .env.example
├── tailwind.config.ts
├── package.json
└── README.md
🧮 Como Funciona o Cálculo
text

1. CUSTO HORA BASE
   custoHora = (custosFixos + reserva) / horasProdutivas

2. AJUSTE POR IMPOSTOS
   custoComImposto = custoHora / (1 - aliquotaImposto)

3. INCLUSÃO DE FÉRIAS + FERIADOS
   custoReal = custoComImposto × (52 / semanasTrabalháveis)

4. META DE RENDA
   precoIdeal = max(custoReal, metaRenda / horasProdutivas)

5. FAIXAS
   🔴 Mínimo  = custoReal (break-even)
   🟡 Saudável = precoIdeal × 1.2
   🟢 Ideal    = precoIdeal × 1.5 (com margem de crescimento)
🤝 Contribuindo
Contribuições são muito bem-vindas! Este é um projeto que pode ajudar
milhões de profissionais brasileiros.

Faça um fork do projeto
Crie sua branch (git checkout -b feature/minha-feature)
Commit suas mudanças (git commit -m 'feat: adiciona nova feature')
Push para a branch (git push origin feature/minha-feature)
Abra um Pull Request

📌 Formas de contribuir
🐛 Reportar bugs
💡 Sugerir novas funcionalidades
📊 Adicionar dados de novas profissões
🌎 Melhorar dados regionais de custo de vida
📝 Melhorar documentação
🎨 Melhorar UI/UX
📊 Profissões Suportadas

Categoria	Profissões
💻 Tecnologia	Dev Frontend, Dev Backend, Dev Fullstack, Dev Mobile, UI/UX Designer, QA
🎨 Design	Designer Gráfico, Ilustrador, Motion Designer, Editor de Vídeo
📸 Fotografia	Casamento, Produto, Ensaio, Eventos
📱 Marketing	Social Media, Copywriter, Gestor de Tráfego, SEO
📚 Educação	Professor Particular, Tradutor, Revisor de Textos
🍰 Gastronomia	Confeiteiro(a), Chef, Food Stylist
💪 Saúde & Bem-estar	Personal Trainer, Nutricionista, Psicólogo
💅 Beleza	Manicure, Cabeleireiro(a), Maquiador(a)
🔧 Serviços	Eletricista, Encanador, Pintor, Marceneiro
📐 Arquitetura	Arquiteto, Designer de Interiores
⚖️ Consultoria	Consultor Financeiro, Coach, Mentor

📈 Roadmap
 MVP — Calculadora básica
 Sistema de etapas (wizard)
 Cálculo por profissão
 Comparativo regional
 Sistema premium (Stripe)
 App mobile (React Native)
 API pública para integrações
 Plugin para plataformas (99Freelas, Workana)
 Versão para pequenas empresas

📄 Licença
Distribuído sob a licença MIT. Veja LICENSE para mais informações.

💚 Apoie o Projeto
Se o Quanto Cobrar? te ajudou, considere:

⭐ Dar uma star no repositório
📢 Compartilhar com outros freelancers
☕ Me pagar um café

Feito com 💚 para os freelancers do Brasil

Porque seu trabalho tem valor. Cobre certo.
