# PineCrafter

**Custom TradingView indicators and strategies in Pine Script v6.**
Your trading idea, properly coded and honestly measured.

---

## What I do

I turn trading rules into working Pine Script. Non-repainting, with real risk management, with alerts that actually fire when they should, and with an honest measurement of how the idea behaved on historical data.

What I do **not** do is sell winning strategies. Nobody can. What I sell is the craft: your logic, built properly, and the truth about it.

If your idea works, you get a tool. If it doesn't, you saved yourself months of losing money. Both are worth the price.

---

## Portfolio

Three indicators built from scratch. Open source, Pine Script v6, non-repainting. Copy them, read them, judge the work.

### 1. MTF Confluence — [`PineCrafter_01_Confluencia_MTF_v1.1.pine`](./PineCrafter_01_Confluencia_MTF_v1.1.pine)

A three-floor traffic light. Tracks trend across three timeframes at once (1H / 4H / Daily by default) and prints a signal when all three align.

- Higher timeframes read strictly from their last **closed** bar — no repainting
- Timeframes below the chart's own are ignored and flagged, so the reading is never misleading
- Configurable signal colours, Spanish/English panel, ready-made alerts

**Shows:** multi-timeframe data handling without repainting, table panels, alert conditions.

### 2. Swing Cockpit — [`PineCrafter_02_Swing_Cockpit_v3.pine`](./PineCrafter_02_Swing_Cockpit_v3.pine)

Not a signal generator. A full trade cockpit. When a pullback setup triggers, it draws the entire plan:

- Entry, ATR-based stop, three targets measured in R multiples
- **Position size** calculated from your account size and risk per trade
- Risk and reward zones drawn on the chart
- JSON alert payload, ready to wire to a webhook/bot
- A signal quality score (1–4 stars) from volume, candle conviction, higher-timeframe alignment and ADX

And the part most indicators don't have: a panel that measures **every** signal in the chart's history and reports win rate and mathematical expectancy with the target set at TP1, TP2 and TP3. Positive expectancy means the plan makes money. Negative means it loses.

**Shows:** risk management, position sizing, drawing objects, webhook payloads, statistics engine.

### 3. Levels Map — [`PineCrafter_03_Mapa_de_Niveles.pine`](./PineCrafter_03_Mapa_de_Niveles.pine)

Solves an everyday problem: *where do I put my target?*

- Recent swing highs and lows, plus previous day / week / month high, low and close
- A ladder panel showing the nearest levels above and below, with distance in **percent and in ATR multiples**
- Today's range vs the 20-day average range — turns orange when the asset has already spent its typical daily move

That ATR column is the point: if the next ceiling is 0.8 ATR away, a 2 ATR target is sitting behind a wall.

**Shows:** pivot detection without repainting, multi-timeframe reference levels, dynamic sorted panels.

---

## An honest note about the Swing Cockpit

The Cockpit originally shipped with a quality filter that scored signals from one to four stars. I tested it across **11 assets and 1,831 trades**. Every quality level won between 47.7% and 48.2% of the time. The filter added nothing.

So I said so, and rebuilt the panel to measure targets instead of selling the filter.

That is the whole point of how I work. An indicator that lies to you is worse than no indicator. If you hire me and your idea doesn't hold up, I will tell you.

---

## Services

| | **Workshop** | **Forge** |
|---|---|---|
| **When** | Your code already exists | It has to be written from scratch |
| **Includes** | Fix compile errors · Migrate v4/v5 → v6 · Add or repair alerts · Merge two indicators into one · Rework inputs and styling | Your indicator or strategy from your written rules · Non-repainting · Organised inputs · Alerts ready · Optional: stop, targets and position sizing inside the script |
| **Scope limit** | One file, no new logic | Up to 5 rules or conditions |
| **Delivery** | 1 day | 3 days |
| **Revisions** | 1 | 2 |

**Add-ons:** strategy version with TradingView's Strategy Tester and your commissions applied · JSON alert for bots and webhooks · express delivery · extra revision · walkthrough video.

Something bigger or with more rules? Open an issue or message me and I'll quote it.

---

## How a job runs

1. You send your rules.
2. I turn them into a written spec: logic, edge cases, open questions. **You approve it before a single line is written.** This step removes almost every misunderstanding.
3. I code it and compile it.
4. You check it on your own charts.
5. You get the `.pine` file and a README explaining every setting.

---

## What I will never do

- Promise profitability, a win rate, or "guaranteed signals"
- Copy or reverse-engineer someone else's protected indicator
- Give financial advice or tell you what to trade
- Deliver something that repaints without telling you clearly

---

## Contact

Open an issue in this repository, or reach me through my Fiverr profile.

---

---

# PineCrafter · en español

**Indicadores y estrategias a medida para TradingView, en Pine Script v6.**
Tu idea de trading, bien programada y medida con honestidad.

## Qué hago

Convierto reglas de trading en Pine Script que funciona. Sin repintado, con gestión de riesgo real, con alertas que saltan cuando deben, y con una medición honesta de cómo se comportó la idea en el histórico.

Lo que **no** hago es vender estrategias ganadoras. Nadie puede. Lo que vendo es el oficio: tu lógica, bien construida, y la verdad sobre ella.

Si tu idea funciona, te llevas una herramienta. Si no funciona, te has ahorrado meses perdiendo dinero. Las dos cosas valen lo que cuestan.

## El portfolio

Tres indicadores construidos desde cero. Código abierto, Pine Script v6, sin repintado.

**1 · Confluencia Multi-Temporalidad** — Un semáforo de tres pisos. Vigila la tendencia en 1H, 4H y diario a la vez, y marca cuándo las tres se alinean. Cada temporalidad se lee siempre de su última vela cerrada, así que lo que ves en el histórico es lo que habrías visto en directo.

**2 · Swing Cockpit** — Un cuadro de mando completo. Al dispararse la señal dibuja el plan entero: entrada, stop por ATR, tres objetivos en múltiplos de riesgo, y **cuántas acciones comprar** según tu capital y tu riesgo por operación. Alerta en JSON lista para bot. Y un panel que mide todas las señales del histórico y dice el acierto y la esperanza matemática con el objetivo puesto en TP1, TP2 y TP3.

**3 · Mapa de Niveles** — Resuelve la duda de dónde poner el objetivo. Dibuja máximos y mínimos recientes y los niveles del día, la semana y el mes anteriores, y ordena en un panel los más cercanos con la distancia en porcentaje y en múltiplos de ATR. Si el siguiente techo está a 0,8 ATR, un objetivo a 2 ATR está detrás de un muro.

## Una nota honesta

El Cockpit llevaba un filtro de calidad que puntuaba las señales de una a cuatro estrellas. Lo probé en **11 activos y 1.831 operaciones**. Todos los niveles acertaban entre el 47,7% y el 48,2%: el filtro no aportaba nada.

Lo dije, y rehice el panel para que midiera objetivos en vez de vender el filtro. Un indicador que te miente es peor que no tener indicador. Si me contratas y tu idea no aguanta, te lo diré.

## Servicios

**Taller** — Tu código ya existe. Arreglar errores, migrar de v4/v5 a v6, añadir o corregir alertas, unir dos indicadores en uno, cambiar aspecto y ajustes. Un archivo, sin lógica nueva. Entrega en 1 día, 1 revisión.

**Forja** — Hay que escribirlo desde cero. Tu indicador o estrategia a partir de tus reglas, sin repintado, con ajustes organizados y alertas listas. Si lo pides: stop, objetivos y tamaño de posición dentro del script. Hasta 5 reglas. Entrega en 3 días, 2 revisiones.

**Extras:** versión estrategia con el probador de TradingView y tus comisiones · alerta JSON para bots · entrega exprés · revisión adicional · vídeo explicativo.

## Cómo funciona un encargo

Me mandas tus reglas. Las convierto en una especificación escrita con la lógica, los casos límite y las preguntas abiertas, **y tú la apruebas antes de que se escriba una sola línea**. Programo, compilas, lo validas en tus gráficos, y recibes el archivo `.pine` con un README que explica cada ajuste.

## Lo que nunca voy a hacer

Prometer rentabilidad o porcentajes de acierto. Copiar el indicador protegido de otra persona. Darte consejo financiero. Entregarte algo que repinta sin avisarte.

## Contacto

Abre un issue en este repositorio, o escríbeme por mi perfil de Fiverr.
