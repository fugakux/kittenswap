# Kittenswap: ve(3,3) — How It Works (Full Guide)

A complete, **consumer-friendly** yet accurate guide to **ve(3,3)** on **Kittenswap** — a DEX with weekly epochs, a vote‑escrowed NFT called **VeKitten**, and a **decreasing emission** of the **$KITTEN** token.

> **Kittenswap Key Params**
>
> - **Epoch length:** 1 week  
> - **veNFT name:** **VeKitten**  
> - **Token:** **$KITTEN** (18 decimals)  
> - **Initial weekly emission:** **19.8M $KITTEN / epoch**  
> - **Decay:** **–1% per epoch** (compounded)  
> - **Formula:** `Eₙ = 19.8M × 0.99^(n−1)`

---

## TL;DR (One Screen)

- **Lock $KITTEN → get a VeKitten.** The **more you lock** and the **longer you lock**, the **more voting power** you get (it decays toward lock expiry).
- Every **week (epoch)**, Kittenswap mints that week’s **$KITTEN emissions** (starting at **19.8M** and dropping **1% weekly**).
- **VeKitten holders vote** to decide **which pools** (gauges) get **this week’s $KITTEN**.  
- **LPs** (who stake their LP tokens in a pool’s **Gauge**) earn the **$KITTEN** routed to that pool.  
- **Voters** earn **bribes** (bonus tokens posted to attract votes) **and a share of trading fees** from pools they voted for.  
- Optional “**(3,3)**” touch: a **small rebase** can go to VeKitten holders to **offset dilution**.
- The 1% decay gives a **soft landing** for inflation and encourages **early participation**.

---

## Weekly Rhythm (Epochs)

Each **epoch** is **1 week**. On epoch flip:

1. **Votes snapshot** (your votes at this moment decide the week’s routing).  
2. **Mint emissions** for the week (`Eₙ`).  
3. **Split emissions** across pools **pro‑rata by votes**.  
4. **Gauges stream rewards** to **staked LPs** over the week.  
5. **Voters** for those pools can **claim** their **bribes + fees** for that week.

> Your votes usually **persist** until you change them. You can **re‑vote** before the next snapshot to chase better opportunities.

---

## Emissions: The 19.8M → 1% Decay Schedule

- **Week 1:** `E₁ = 19.8M` $KITTEN  
- **Each week after:** multiply by **0.99** (–1%)  
- **Week n:** `Eₙ = 19.8M × (0.99)^(n−1)`  
- **Cumulative after N weeks:** `S_N = 19.8M × (1 − 0.99^N) / (1 − 0.99) = 1.98B × (1 − 0.99^N)`  
- **Maximum (very long‑run):** `S_∞ = 1.98B $KITTEN`

**First 12 weeks (rounded):**

| Week | Emission (M $KITTEN) |
|---:|---:|
| 1 | 19.80 |
| 2 | 19.60 |
| 3 | 19.41 |
| 4 | 19.21 |
| 5 | 19.02 |
| 6 | 18.83 |
| 7 | 18.64 |
| 8 | 18.45 |
| 9 | 18.27 |
| 10 | 18.09 |
| 11 | 17.91 |
| 12 | 17.73 |

> Numbers are approximate for readability; the app follows the exact geometric schedule.

---

## VeKitten: Locking, Voting Power, Decay

- **Lock $KITTEN → mint VeKitten:** Choose **how much** and **how long** to lock. Both increase your **voting power**.  
- **Time weighting:** Longer locks grant **more power** (commonly linear up to a **max lock**, e.g., 2 years).  
- **Decay:** Your voting power **slowly declines** and hits **0 at expiry**. You can **extend** or **add tokens** to refresh.  
- **NFT benefits:** Because VeKitten is an **NFT**, you can **transfer**, **merge**, or **split** positions.

**Use your VeKitten to vote** on pools each week and earn **voter rewards** (bribes + fees; and possibly rebase).

---

## Voting & Gauges: How Rewards Get Routed

- Every pool has a **Gauge**.  
- **VeKitten holders** spread their voting power across gauges (e.g., 70% to `KITTEN/HYPE`, 30% to `FeUSD/USDT`).  
- On the weekly snapshot, Kittenswap **adds up weights** and routes that week’s emissions **pro‑rata**.  
- **LPs must stake** LP tokens in the **Gauge** to receive the streamed **$KITTEN**.

---

## Bribes & Fees: Why Voters Care

- **Bribes:** Anyone can post extra tokens to a pool’s **Bribe** to **attract votes**. If you **voted** for that pool, you can **claim** your **share**.  
- **Fees:** A portion of a pool’s **trading fees** is shared with that week’s **voters of that pool**.  
- Together, bribes + fees mean **voting wisely** can be **profitable** (especially where trading is active or bribes are generous).

---

## LP Rewards: Why Liquidity Providers Care

- LPs earn the **$KITTEN emissions** that voters **route** to their pool.  
- To participate, **stake your LP tokens** in the pool’s **Gauge**.  
- Rewards **stream during the week** and can be **claimed** in‑app.

---

## Rebase / Anti‑Dilution (the “3,3” Bit)

- A small **optional** slice of each week’s emissions can be distributed to **VeKitten holders** (by current voting power).  
- This **offsets dilution** for lockers and **rewards long‑term alignment**.  
- If enabled, it will be shown clearly in the app and docs.

---

## FAQ 

**Q1: What is ve(3,3) in one sentence?**  
**A:** **Lockers vote** where rewards go, **LPs earn** the routed rewards, and **voters earn** bribes/fees for steering liquidity — a cooperative loop.

**Q2: Do I need to lock to use Kittenswap?**  
**A:** No. You can **trade** or **LP** without locking. Locking is for those who want to **vote** and earn **voter rewards**.

**Q3: What exactly do LPs earn?**  
**A:** **$KITTEN** streamed weekly to the pool, sized by **votes**. Stake LP tokens in the **Gauge** to receive it.

**Q4: What do voters earn?**  
**A:** A share of **bribes** and **trading fees** from the pools they voted for (and possibly a **rebase**).

**Q5: Can I both LP and vote the same pool?**  
**A:** Yes. Many users **lock + vote + LP** the same pool.

**Q6: What are bribes?**  
**A:** They’re just **bonus rewards** posted to attract votes. If you vote that pool, you can claim a **share**. It’s transparent and on‑chain.

**Q7: Why do emissions fall 1% weekly?**  
**A:** To **taper inflation** and create a **soft cap**. Over time, total minted approaches **1.98B $KITTEN**.

**Q8: Do I have to re‑vote every week?**  
**A:** Not required but you can vote every week to earn from the bribes..

**Q9: My LP rewards were small. Why?**  
**A:** Your pool may have received **few votes**, or you didn’t **stake** LPs in the Gauge.

**Q10: I voted but earned little. Why?**  
**A:** There may have been **few trades** (low fees) or **no bribes** in that pool for the week. Try **re‑allocating** next epoch.

**Q11: What’s a Gauge in simple words?**  
**A:** The place you **stake LP tokens** to receive that pool’s weekly **$KITTEN**.

**Q12: What happens when my lock expires?**  
**A:** Your voting power becomes **0** and you can **withdraw** your $KITTEN. You can **extend** anytime before expiry.

**Q13: Can a whale control everything?**  
**A:** Influence requires **fresh locks**. Voting power **decays**, so long‑term control needs maintenance.

**Q14: Is there a minimum to participate?**  
**A:** Trading has no minimum. LPing and locking may have practical minimums due to gas/fees.

**Q15: Stable vs. volatile pools — what’s the difference?**  
**A:** **Stable** pools (e.g., `FeUSD/USDT`) are optimized for low slippage around 1:1; **volatile** pools (e.g., `KITTEN/HYPE`) suit non‑pegged assets.

**Q16: What is a rebase here?**  
**A:** A small, weekly payout to **VeKitten holders** to offset dilution and reward locking.

**Q17: When and where do I claim rewards?**  
**A:** In the **VeKitten Dashboard** section after each epoch.

**Q18: Can anyone post bribes?**  
**A:** Yes — projects, treasuries, or individual users.


---

