# VIRTUS — Organizador Pessoal Estoico

> *Disciplina gera liberdade.*

Aplicativo minimalista de organização pessoal com filosofia estoica. Sistema de metas, rotinas, agenda semanal, controle financeiro e gamificação por emblemas e streaks.

---

## 🚀 Como usar

**Não precisa de instalação.** Basta abrir o arquivo `index.html` no navegador.

```
Abrir index.html no Chrome, Firefox ou Safari
```

Para a melhor experiência, use um servidor local:

```bash
# Python (já vem instalado no Mac/Linux)
python3 -m http.server 8080
# Depois acesse: http://localhost:8080

# Node.js
npx serve .
```

---

## 📱 Instalar como App (PWA)

No Chrome/Edge:
1. Abra com servidor local
2. Clique nos 3 pontinhos → "Instalar Virtus"
3. O app aparece na área de trabalho e funciona offline

No iPhone/Safari:
1. Abra com servidor local
2. Compartilhar → "Adicionar à Tela de Início"

---

## 🗂 Estrutura

```
virtus/
├── index.html     ← app completo (HTML + CSS + JS em um arquivo)
├── sw.js          ← service worker (funciona offline)
├── manifest.json  ← configuração PWA
├── icon.svg       ← ícone do app
└── README.md      ← este arquivo
```

---

## ✨ Funcionalidades

### 📊 Visão Geral
- Dashboard com métricas do dia
- Tarefas do dia (rotinas + subtarefas de metas)
- Histórico visual de streak (últimos 14 dias)
- Citação estoica diária

### 🎯 Metas
- Criar metas com período (diária/semanal/mensal/trimestral/anual)
- Subtarefas com checkboxes
- Barra de progresso automática
- Status automático: Ativa / Atrasada / Concluída / Cancelada
- Cancelamento com penalidade de XP

### 🔄 Rotinas
- Hábitos recorrentes com frequência configurável
- Check-in diário (contribui para o streak global)
- Histórico visual de consistência dos últimos 7 dias
- Taxa de consistência percentual

### 📅 Agenda
- Visualização semanal (seg a dom)
- Rotinas aparecem automaticamente por dia
- Adicionar/remover compromissos
- Navegação entre semanas

### 💰 Finanças
- Registro de entradas e saídas com categoria
- Cards de saldo (entradas / saídas / resultado)
- Filtro por semana, mês ou trimestre
- Cada lançamento concede +5 XP

### 🏆 Conquistas
- 8 emblemas: Semente → Discípulo → Praticante → Guardião → Filósofo → Sábio → Mestre → Virtuoso
- Progresso por XP + streak mínimo
- Fogo 🔥 com intensidade visual por dias consecutivos

---

## 🔥 Sistema de XP e Emblemas

| Ação | XP |
|---|---|
| Check-in de rotina | +15 XP |
| Subtarefa concluída | +10 XP |
| Meta concluída | +50 XP (bônus) |
| Meta concluída com atraso | +25 XP |
| Lançamento financeiro | +5 XP |
| Streak 7 dias | +100 XP |
| Streak 30 dias | +500 XP |
| Cancelar meta | −30 XP |
| Cancelar rotina | −20 XP |

### Emblemas

| Emblema | XP Mínimo | Streak Mínimo |
|---|---|---|
| 🌱 Semente | 0 | — |
| 📖 Discípulo | 150 | 3 dias |
| ⚔️ Praticante | 400 | 7 dias |
| 🛡️ Guardião | 900 | 14 dias |
| 🏛️ Filósofo | 1.800 | 21 dias |
| 🌙 Sábio | 3.200 | 30 dias |
| ⚡ Mestre | 5.500 | 45 dias |
| 👑 Virtuoso | 9.000 | 60 dias |

---

## 💾 Dados

Todos os dados são salvos automaticamente no `localStorage` do navegador.

**Backup:**  
Adicione este botão na URL do navegador para exportar:
```javascript
javascript:void(exportData())
```
Ou abra o console (F12) e execute: `exportData()`

---

## 🛠 Tecnologias

- HTML5 + CSS3 + JavaScript vanilla
- `localStorage` para persistência
- Service Worker para funcionamento offline
- PWA-ready (instalável)
- Zero dependências externas (funciona sem internet após primeiro carregamento)
- Fontes: Cormorant Garamond + DM Mono (Google Fonts)

---

*Virtus v1.0 — Abril 2026*
