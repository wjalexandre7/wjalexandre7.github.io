# 📋 Painel de Tarefas — App Web, iOS e Android (PWA)

Aplicativo de tarefas sincronizado com o Google Drive, construído como **PWA
(Progressive Web App)**. É **um único código** que roda:

- 🌐 **Web** — em qualquer navegador, hospedado no GitHub Pages.
- 🍎 **iOS/iPadOS** — instalável pela tela inicial via Safari.
- 🤖 **Android** — instalável pela tela inicial via Chrome (com banner de instalação).

Publicado em: **https://wjalexandre7.github.io/**

## Recursos

- Adicionar, editar, concluir e remover tarefas.
- Filtros (Todas / Hoje / Pendentes / Concluídas) e busca.
- Estatísticas (total, concluídas, pendentes, recorrentes).
- Gerador de relatórios (copiar/baixar).
- **Funciona offline**: as tarefas ficam salvas no dispositivo (localStorage) e o
  app carrega mesmo sem internet (Service Worker).
- **Instalável** como app nativo, com ícone próprio e tela cheia (sem barra do
  navegador).
- Sincronização com o Google Drive via Google Apps Script.

## Como instalar

### Android (Chrome)
1. Acesse **https://wjalexandre7.github.io/**.
2. Toque em **Instalar** no banner que aparece — ou no menu ⋮ → *Instalar app*.

### iPhone / iPad (Safari)
1. Acesse **https://wjalexandre7.github.io/** no Safari.
2. Toque em **Compartilhar** (□↑) → **Adicionar à Tela de Início**.

### Computador (Chrome/Edge)
1. Acesse o site.
2. Clique no ícone de instalar na barra de endereço (ou menu → *Instalar*).

## Estrutura

| Arquivo | Função |
|---|---|
| `index.html` | O app (interface + lógica). |
| `manifest.webmanifest` | Metadados do PWA (nome, ícones, cores, atalhos). |
| `sw.js` | Service Worker (cache do app e suporte offline). |
| `icons/` | Ícones do app (192, 512, maskable, Apple touch, favicon). |
| `painel-sincronizado.html` | Versão original (mantida por referência). |

## Configuração do backend

A URL do Google Apps Script fica no topo do `<script>` em `index.html`
(`APPS_SCRIPT_URL`). Para trocar o backend, basta editar essa constante.

## Desenvolvimento local

Por causa do Service Worker, use um servidor local (não abra o arquivo direto):

```bash
python3 -m http.server 8000
# acesse http://localhost:8000
```
