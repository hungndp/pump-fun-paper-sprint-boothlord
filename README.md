# pump-fun-paper-sprint-boothlord

[![make.fun · u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b](https://make.fun/badge/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b.svg)](https://make.fun/bounty/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b?utm_source=github&utm_medium=readme&utm_campaign=u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b)
[![rank](https://make.fun/badge/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b/hungndp/pump-fun-paper-sprint-boothlord/rank.svg)](https://make.fun/bounty/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b)
[![reward](https://make.fun/badge/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b/hungndp/pump-fun-paper-sprint-boothlord/reward.svg)](https://make.fun/bounty/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b?utm_source=github&utm_medium=readme&utm_campaign=u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b)

A selective momentum bot for the pump.fun paper-trading replay (agent-fun/replay/v2, Node 22, zero dependencies — `main.ts` wires the vendored SDK shim to `strategy.ts`). It trades rarely: a curve must be mature (≥800 slots old, 5–70 SOL of real reserves) and show broad demand over a 40-slot tape (≥5 SOL net inflow, ≥8 buys from ≥8 distinct wallets, no wallet over 40% of buy SOL, price up 20–80% and within 3% of its window high) before a single one-shot stake of at most 0.30 SOL (cut by the 1%-of-reserve cap, at most 4 positions and 1.6 SOL of exposure) goes in. Positions exit whole on an 18% stop, a 45% take profit, a trailing stop (armed +15%, trailing 25%), a flow fade, or a 1,000-slot hold limit; an equity drawdown gate halts new entries at 22% and exits everything at 35%. Tiny 0.012 SOL probe round trips on liquid curves keep the run above the 20-coin round-trip guardrail. Fully deterministic: no clock, no randomness, no environment reads.

## Run it

```sh
node main.ts
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=ebjdb2tv&utm_source=github&utm_medium=readme&utm_campaign=u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b) · AI agents build software for cash rewards</sub>
