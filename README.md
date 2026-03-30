<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:0f2744,100:1a3a5c&height=200&section=header&text=Luís%20Otávio%20Guero&fontSize=48&fontColor=e2e8f0&fontAlignY=42&desc=Web%20Developer%20·%20Python%20·%20TypeScript%20·%20C%2B%2B%20·%20SQL&descAlignY=62&descSize=15&descColor=94a3b8&animation=fadeIn" width="100%"/>

<br/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=16&duration=3000&pause=1000&color=38BDF8&center=true&vCenter=true&width=720&height=40&lines=React+%7C+Node.js+%7C+TypeScript+%7C+JavaScript;Meta+Ads+Tracking+%7C+Playwright+E2E+Tests;FastAPI+%7C+OpenAI+%7C+WhatsApp+Automation;PostgreSQL+%7C+MySQL+%7C+MongoDB+%7C+Firebird" />

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-luisotavioguero-0f2744?style=for-the-badge&logo=linkedin&logoColor=38bdf8)](https://linkedin.com/in/luisotavioguero)
[![GitHub](https://img.shields.io/badge/GitHub-zyzerkk-0d1117?style=for-the-badge&logo=github&logoColor=38bdf8)](https://github.com/zyzerkk)
[![Email](https://img.shields.io/badge/Email-contatoguero%40gmail.com-0f2744?style=for-the-badge&logo=gmail&logoColor=38bdf8)](mailto:contatoguero@gmail.com)
[![Views](https://komarev.com/ghpvc/?username=zyzerkk&style=for-the-badge&color=0f2744&label=PROFILE+VIEWS&labelColor=0d1117)](https://github.com/zyzerkk)

</div>

---

```typescript
const dev = {
  name:      "Luís Otávio Guero",
  age:       22,
  location:  "Santa Maria, RS — Brasil",
  education: [
    "Engenharia Aeroespacial · UFSM (2023–presente)",
    "Engenharia de Software · UNICESUMAR (2022–2023)",
    "Técnico em TI + Eletrotécnica · SESI SENAI (2019–2021)",
  ],
  stack:     ["React", "Node.js", "TypeScript", "Python", "C++", "SQL"],
  currently: "Desenvolvendo habilidades em Web Dev + automação de testes E2E",
}
```

---

## Desenvolvimento Web

### Stack atual

<div align="center">

| Camada | Tecnologias |
|:---:|:---|
| **Frontend** | ![React](https://img.shields.io/badge/React-0d1117?style=flat-square&logo=react&logoColor=38bdf8) ![TypeScript](https://img.shields.io/badge/TypeScript-0d1117?style=flat-square&logo=typescript&logoColor=38bdf8) ![JavaScript](https://img.shields.io/badge/JavaScript-0d1117?style=flat-square&logo=javascript&logoColor=38bdf8) ![Tailwind](https://img.shields.io/badge/Tailwind-0d1117?style=flat-square&logo=tailwindcss&logoColor=38bdf8) ![Vite](https://img.shields.io/badge/Vite-0d1117?style=flat-square&logo=vite&logoColor=38bdf8) |
| **Backend** | ![Node.js](https://img.shields.io/badge/Node.js-0d1117?style=flat-square&logo=nodedotjs&logoColor=38bdf8) ![FastAPI](https://img.shields.io/badge/FastAPI-0d1117?style=flat-square&logo=fastapi&logoColor=38bdf8) ![Python](https://img.shields.io/badge/Python-0d1117?style=flat-square&logo=python&logoColor=38bdf8) |
| **Testes** | ![Playwright](https://img.shields.io/badge/Playwright-0d1117?style=flat-square&logo=playwright&logoColor=38bdf8) ![Jest](https://img.shields.io/badge/Jest-0d1117?style=flat-square&logo=jest&logoColor=38bdf8) |
| **Banco de Dados** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-0d1117?style=flat-square&logo=postgresql&logoColor=38bdf8) ![MySQL](https://img.shields.io/badge/MySQL-0d1117?style=flat-square&logo=mysql&logoColor=38bdf8) ![MongoDB](https://img.shields.io/badge/MongoDB-0d1117?style=flat-square&logo=mongodb&logoColor=38bdf8) |
| **Infra** | ![Docker](https://img.shields.io/badge/Docker-0d1117?style=flat-square&logo=docker&logoColor=38bdf8) ![Git](https://img.shields.io/badge/Git-0d1117?style=flat-square&logo=git&logoColor=38bdf8) ![Render](https://img.shields.io/badge/Render-0d1117?style=flat-square&logo=render&logoColor=38bdf8) |
| **Marketing Tech** | ![Meta Pixel](https://img.shields.io/badge/Meta_Pixel-0d1117?style=flat-square&logo=meta&logoColor=38bdf8) ![Meta Ads](https://img.shields.io/badge/Meta_Ads_API-0d1117?style=flat-square&logo=meta&logoColor=38bdf8) |

</div>

---

## Projetos em Destaque

### 🌐 Landing Pages + Meta Ads Tracking
> Desenvolvimento de landing pages de alta conversão com rastreamento completo de eventos para o Meta Ads Manager.

**O que foi implementado:**

```typescript
// Eventos rastreados via Meta Pixel + Conversions API
const pixelEvents = {
  PageView:         "Dispara no carregamento da LP",
  InitiateCheckout: "Dispara ao clicar no CTA principal",
  Purchase:         "Dispara após confirmação de compra",
}
// Resultado: dados de conversão reais chegando ao Meta Ads Manager
// sem depender apenas dos cookies — server-side + client-side tracking
```

**Stack:** React · TypeScript · Node.js · Meta Pixel · Meta Conversions API

---

### 🧪 Testes E2E Automatizados — Meta Ads + Checkout

> Suite de testes com Playwright que simula a jornada real de um usuário desde o criativo do anúncio até o preenchimento do checkout, validando cada evento do Meta Pixel em tempo real.

```typescript
// O teste abre o link do criativo, scrolls a página,
// clica no CTA, preenche o checkout e valida cada evento do pixel
test('jornada completa do criativo ao checkout', async ({ page }) => {
  const eventos: string[] = []

  // Intercepta requisições ao Meta Pixel em tempo real
  page.on('request', (req) => {
    if (req.url().includes('facebook.com/tr/')) {
      const ev = new URLSearchParams(req.url().split('?')[1]).get('ev')
      if (ev) eventos.push(ev)
    }
  })

  await page.goto(AD_CREATIVE_URL, { waitUntil: 'networkidle' })
  expect(eventos).toContain('PageView')            // ✓

  await page.locator('[data-cta]').scrollIntoViewIfNeeded()
  await page.locator('[data-cta]').click()

  expect(eventos).toContain('InitiateCheckout')    // ✓

  await page.locator('input[type="email"]').fill('teste@email.com')
  // ... preenche nome, CPF, cartão de teste
})
```

**Cobertura dos testes:**

```
✓ PageView — pixel inicializado na landing page
✓ InitiateCheckout — evento ao clicar no CTA
✓ Scroll simulado — comportamento real do usuário
✓ Preenchimento de checkout — campos validados
✓ Smoke test — pixel carregado + sem erros de console
✓ Teste em desktop e mobile (iPhone 14)
```

**Stack:** Playwright · TypeScript · Node.js

---

### 🤖 Automação WhatsApp com IA
> Backend Python que conecta WhatsApp Business a GPT via webhook, com memória contextual por conversa e fluxos de atendimento automatizados.

```
Cliente → 360Dialog [~200ms] → FastAPI → OpenAI [~1.5s] → Resposta
                                              Latência total < 3s
```

**Entregáveis:** 6 semanas · Prompt mestre + memória contextual · Deploy Render · Documentação técnica  
**Stack:** Python · FastAPI · OpenAI API · 360Dialog WhatsApp API

---

### 🛰️ OBSAT — CubeSat Meteorológico
**🥇 1° Lugar Nacional — Olimpíada Brasileira de Satélites 2022/2023**

> Capitão e programador principal de um CubeSat para detecção antecipada de tornados em SC. Programação embarcada em C++ com telemetria via RF LoRa, GPS, sensores de temperatura/pressão e backup duplo em cartão SD. Lançamento sub-orbital no CLBI – Natal/RN.

```cpp
// Stack embarcada real do projeto
#include "PION_System.h"   // computador de bordo
#include <TinyGPS++.h>     // posicionamento GPS
#include <ArduinoJson.h>   // payload em JSON para telemetria
SoftwareSerial loraSerial(2, 3); // transmissor RF LoRa TX/RX
```

**Testes de qualificação:** criogênico (−33°C) · térmico (+50°C) · vácuo (6 mbar) · vibração · voo atmosférico ~40km

---

## Experiência Profissional

### Zucchetti Software e Sistemas — Suporte Técnico N1 → N3
`2021 – presente`

Iniciei no N1 e em 6 meses fui convidado a **criar e liderar a equipe N2**. Evoluí para **N3** pela alta capacidade de resolução de problemas avançados: correção de bugs, restauração de bancos corrompidos e reparos via IBExpert.

**Especialidade em migração de banco de dados:**

```sql
-- Conversões realizadas em ambiente de produção
FDB   → FDB      -- reestruturação de schema Firebird
PGSQL → FDB      -- migração PostgreSQL para Firebird  
CSV   → FDB      -- importação massiva de dados legados
MySQL → FDB      -- integração entre sistemas distintos
GDB   → FDB      -- atualização de versão de banco
```

---

## Premiações

```
🥇  Ouro  · OBSAT Regional e Nacional  2022 e 2023  (lançamento sub-orbital de CubeSat)
🥇  Ouro  · Mostra Brasileira de Foguetes (MOBFOG)   2020 e 2021
🥉  Bronze · Olimpíada de Foguetes Sólidos           2021
🥉  Bronze · Olimpíada Canguru de Matemática         2021
🥇  Ouro  · Copa Brasileira de Matemática Mangahigh  2020
🥉  Bronze · Copa Brasileira de Matemática Mangahigh 2019
```

---

## GitHub Stats

<div align="center">

<img height="175" src="https://github-readme-stats.vercel.app/api?username=zyzerkk&show_icons=true&hide_border=true&bg_color=0d1117&title_color=38bdf8&text_color=94a3b8&icon_color=38bdf8&count_private=true&include_all_commits=true&rank_icon=github" />
<img height="175" src="https://github-readme-stats.vercel.app/api/top-langs/?username=zyzerkk&layout=compact&hide_border=true&bg_color=0d1117&title_color=38bdf8&text_color=94a3b8&langs_count=6&card_width=320" />

</div>

<div align="center">

<img src="https://streak-stats.demolab.com?user=zyzerkk&hide_border=true&background=0d1117&ring=38bdf8&fire=38bdf8&currStreakLabel=38bdf8&sideLabels=94a3b8&dates=546e7a&currStreakNum=e2e8f0&sideNums=e2e8f0&mode=weekly" />

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a3a5c,100:0d1117&height=100&section=footer&fontSize=13&fontColor=38bdf8&animation=fadeIn" width="100%"/>

**contatoguero@gmail.com · Santa Maria, RS · Brasil**

</div>
