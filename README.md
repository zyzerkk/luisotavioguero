<div align="center">

<img src="https://capsule-render.vercel.app/api?type=venom&color=0:0a0a0a,100:1a3a5c&height=220&section=header&text=Luís%20Otávio%20Guero&fontSize=46&fontColor=4fc3f7&fontAlignY=45&desc=Engenharia%20Aeroespacial%20·%20Desenvolvimento%20de%20Software%20·%20IA%20Embarcada&descAlignY=65&descSize=14&descColor=78909c&stroke=1a3a5c&strokeWidth=2" width="100%"/>

<br/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=16&duration=3500&pause=1000&color=4FC3F7&center=true&vCenter=true&width=700&height=40&lines=Python+·+C%2B%2B+·+TypeScript+·+SQL;CubeSat+%7C+Embedded+Systems+%7C+RF+Communication;FastAPI+%7C+OpenAI+%7C+WhatsApp+Automation;Database+Migration+%7C+FDB+%7C+PostgreSQL+%7C+MySQL" />

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-luisotavioguero-1a3a5c?style=for-the-badge&logo=linkedin&logoColor=4fc3f7)](https://linkedin.com/in/luisotavioguero)
[![GitHub](https://img.shields.io/badge/GitHub-zyzerkk-0d1117?style=for-the-badge&logo=github&logoColor=4fc3f7)](https://github.com/zyzerkk)
[![Email](https://img.shields.io/badge/Email-contatoguero@gmail.com-1a3a5c?style=for-the-badge&logo=gmail&logoColor=4fc3f7)](mailto:contatoguero@gmail.com)
[![Views](https://komarev.com/ghpvc/?username=zyzerkk&style=for-the-badge&color=1a3a5c&label=PROFILE+VIEWS&labelColor=0d1117)](https://github.com/zyzerkk)

</div>

---

```python
#!/usr/bin/env python3
# luisotavioguero.py

class Dev:
    def __init__(self):
        self.name        = "Luís Otávio Guero"
        self.age         = 22
        self.location    = "Santa Maria, RS — Brasil"
        self.education   = [
            "Engenharia Aeroespacial · UFSM (2023–presente)",
            "Engenharia de Software · UNICESUMAR (2022–2023)",
            "Técnico em TI + Eletrotécnica · SESI SENAI (2019–2021)",
        ]
        self.languages   = ["Python", "C++", "TypeScript", "JavaScript", "SQL"]
        self.focus       = ["IA Embarcada", "Sistemas de Banco de Dados", "Automação", "Engenharia Espacial"]
        self.email       = "contatoguero@gmail.com"

    def __repr__(self):
        return f"Dev({self.name} | {self.location})"

me = Dev()
```

---

## Experiência

### Zucchetti Software e Sistemas — Suporte Técnico N1 → N3
`2021 – presente`

Iniciei no N1 e, em 6 meses, fui convidado a **criar e liderar a equipe de N2**. Evoluí para **N3** pela capacidade de resolver problemas avançados: correção de bugs, restauração de bancos corrompidos, reparos via IBExpert e migração de dados complexas.

**Conversão de banco de dados (6 meses dedicados):**

```sql
-- Conversões realizadas em produção:
FDB  → FDB      -- reestruturação de schema
PSQL → FDB      -- migração PostgreSQL para Firebird
CSV  → FDB      -- importação massiva de dados legados
MySQL→ FDB      -- integração entre sistemas
GDB  → FDB      -- atualização de versão
```

**Ferramentas:** IBExpert · DB Visualizer · SQL Server · MySQL · MongoDB · PostgreSQL

---

### UFSM – GEDRE (Grupo de Estudos de Reatores Eletrônicos)
`junho – dezembro de 2023`

Programador Python no projeto **Visible Light Communication – IA**: uso de inteligência artificial para manipular comunicação por luz visível.

**Stack:** Python · C++ · NVIDIA Modulus · Sistemas de IA

> Enfrentei e resolvi problemas de ambiente com o NVIDIA Modulus: migração de VSCode para Google Colab, resolução de dependências quebradas via fóruns especializados e downgrade de versão Python para compatibilidade com o framework de digital twins.

---

## Projetos em Destaque

### 🛰️ OBSAT — Equipe Halley `2021 – 2023`
**Olimpíada Brasileira de Satélites · 🥇 1° Lugar Regional e Nacional**

> Capitão, programador e desenvolvedor estrutural de um **CubeSat meteorológico** para detecção antecipada de tornados e ciclones tropicais em Santa Catarina. Lançamento sub-orbital no **CLBI – Natal/RN, dezembro de 2023**.

**Arquitetura do sistema:**

| Subsistema | Tecnologia | Função |
|---|---|---|
| Computador de bordo | PION (C++) | Orquestra todos os módulos |
| Comunicação RF | LoRa 433MHz – Helicoidal 30dBi | Telemetria terra–satélite |
| Posicionamento | GPS + TinyGPS++ | Lat, Long, Alt, Velocidade |
| Sensoriamento | C++/Arduino | Temp, Pressão, CO₂, Acelerômetro, Giroscópio |
| Armazenamento | Cartão SD (duplo backup) | CSV com todos os dados de missão |
| Estrutura | Alumínio Aeronáutico 7075 | 100×100mm · 420g |

**Dados transmitidos pela payload (amostra real):**
```
Equipe | Bateria | Temp(°C) | Pressão | CO₂(ppm) | Acelerômetro XYZ | Giroscópio XYZ | GPS Payload | Status
15     | 64      | 15.68    | 93635   | 2265     | X=-0.89 Y=0.06 Z=-9.55 | X=-0.24 Y=-0.11 Z=-0.00 | Altitude: 652.00... | Sucesso
```

**Programação C++ — bibliotecas utilizadas:**
```cpp
#include "PION_System.h"
#include <WiFi.h>
#include <ArduinoJson.h>
#include "FS.h"
#include <PION_Storage.h>
#include <TinyGPS++.h>
// RF LoRa TX/RX via SoftwareSerial
SoftwareSerial loraSerial(2, 3); // TX, RX
```

**Testes de qualificação realizados:**
- Criogênico: −33,33 °C (gelo seco) — nenhum dano
- Térmico: +50,65 °C (secador) — nenhum dano
- Vácuo: 946 → 6 mbar (máquina industrial BRF) — aprovado
- Vibração (shaker): 5 repetições por módulo — aprovado
- Voo atmosférico: balão a ~40 km de altitude, Santa Maria/RS

---

### 🤖 Automação WhatsApp com IA `2025`
**Consultoria · FastAPI + OpenAI + 360Dialog**

Backend Python que conecta WhatsApp Business a um modelo de linguagem via API oficial, com memória contextual e fluxos de atendimento automatizados.

**Fluxo de dados:**
```
Cliente (WhatsApp) → 360Dialog [100–300ms] → FastAPI Server → OpenAI [1–2s] → Resposta
                                                                         ↳ Latência total: < 3 segundos
```

**Entregas do projeto (6 semanas):**
1. Levantamento de requisitos + escolha de ferramentas
2. Backend Python (FastAPI) + webhook de recebimento
3. Prompt mestre + sistema de memória contextual
4. Fluxos: dúvidas, pedidos, reclamações, localização
5. Deploy (Render / Railway) + monitoramento
6. Documentação técnica + treinamento da equipe

**Stack:** Python · FastAPI · OpenAI API · 360Dialog · Ngrok · Render

---

## 🛠️ Stack Técnica

<div align="center">

| Categoria | Tecnologias |
|:---:|:---|
| **Linguagens** | ![Python](https://img.shields.io/badge/Python-0d1117?style=flat-square&logo=python&logoColor=4fc3f7) ![C++](https://img.shields.io/badge/C++-0d1117?style=flat-square&logo=cplusplus&logoColor=4fc3f7) ![TypeScript](https://img.shields.io/badge/TypeScript-0d1117?style=flat-square&logo=typescript&logoColor=4fc3f7) ![SQL](https://img.shields.io/badge/SQL-0d1117?style=flat-square&logo=postgresql&logoColor=4fc3f7) |
| **Banco de Dados** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-0d1117?style=flat-square&logo=postgresql&logoColor=4fc3f7) ![MySQL](https://img.shields.io/badge/MySQL-0d1117?style=flat-square&logo=mysql&logoColor=4fc3f7) ![MongoDB](https://img.shields.io/badge/MongoDB-0d1117?style=flat-square&logo=mongodb&logoColor=4fc3f7) ![SQLServer](https://img.shields.io/badge/SQL_Server-0d1117?style=flat-square&logo=microsoftsqlserver&logoColor=4fc3f7) |
| **Backend / IA** | ![FastAPI](https://img.shields.io/badge/FastAPI-0d1117?style=flat-square&logo=fastapi&logoColor=4fc3f7) ![OpenAI](https://img.shields.io/badge/OpenAI-0d1117?style=flat-square&logo=openai&logoColor=4fc3f7) ![NVIDIA](https://img.shields.io/badge/NVIDIA_Modulus-0d1117?style=flat-square&logo=nvidia&logoColor=4fc3f7) |
| **Embarcados** | ![Arduino](https://img.shields.io/badge/Arduino_IDE-0d1117?style=flat-square&logo=arduino&logoColor=4fc3f7) ![C++](https://img.shields.io/badge/C++_Embarcado-0d1117?style=flat-square&logo=cplusplus&logoColor=4fc3f7) |
| **Ferramentas** | ![Docker](https://img.shields.io/badge/Docker-0d1117?style=flat-square&logo=docker&logoColor=4fc3f7) ![Git](https://img.shields.io/badge/Git-0d1117?style=flat-square&logo=git&logoColor=4fc3f7) ![Node.js](https://img.shields.io/badge/Node.js-0d1117?style=flat-square&logo=nodedotjs&logoColor=4fc3f7) |
| **DB Tools** | ![IBExpert](https://img.shields.io/badge/IBExpert-0d1117?style=flat-square&logo=databricks&logoColor=4fc3f7) ![DBVisualizer](https://img.shields.io/badge/DB_Visualizer-0d1117?style=flat-square&logo=databricks&logoColor=4fc3f7) |

</div>

---

## 🏆 Premiações

```
┌─────────────────────────────────────────────────────────────────────┐
│  🥇  Medalha de Ouro  · OBSAT Regional e Nacional        2022 2023  │
│       Olimpíada Brasileira de Satélites — lançamento sub-orbital     │
│                                                                      │
│  🥇  Medalha de Ouro  · MOBFOG                           2020 2021  │
│       Mostra Brasileira de Foguetes                                  │
│                                                                      │
│  🥉  Medalha de Bronze · Olimpíada de Foguetes Sólidos       2021  │
│  🥉  Medalha de Bronze · Olimpíada Canguru de Matemática     2021  │
│  🥇  Medalha de Ouro  · Copa Brasileira de Matemática        2020  │
│       Mangahigh                                                      │
│  🥉  Medalha de Bronze · Copa Brasileira de Matemática       2019  │
└─────────────────────────────────────────────────────────────────────┘
```

---

## 📊 GitHub Stats

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=zyzerkk&show_icons=true&hide_border=true&bg_color=0d1117&title_color=4fc3f7&text_color=78909c&icon_color=4fc3f7&count_private=true&include_all_commits=true" />
<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=zyzerkk&layout=compact&hide_border=true&bg_color=0d1117&title_color=4fc3f7&text_color=78909c&langs_count=6" />

<br/>

<img src="https://streak-stats.demolab.com?user=zyzerkk&hide_border=true&background=0d1117&ring=4fc3f7&fire=4fc3f7&currStreakLabel=4fc3f7&sideLabels=78909c&dates=546e7a&currStreakNum=ffffff&sideNums=ffffff" />

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=venom&color=0:1a3a5c,100:0a0a0a&height=120&section=footer&text=contatoguero%40gmail.com&fontSize=16&fontColor=4fc3f7&fontAlignY=65&desc=Santa%20Maria%2C%20RS%20·%20Brasil&descAlignY=80&descSize=12&descColor=546e7a" width="100%"/>

</div>
