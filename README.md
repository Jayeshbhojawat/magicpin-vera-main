# 🌟 Vera — The WhatsApp Bot That Actually Gets It

**by Jayesh Bhojawat** · [jayeshbhojawat@gmail.com](mailto:jayeshbhojawat@gmail.com) · magicpin AI Challenge

---

> *"What if your AI assistant didn't just send messages — but sent the right message, at the right moment, in the right language, with the right vibe?"*
> 
> That's Vera. And this is her story. 💌

---

## ✨ What's living inside here?

Vera isn't just a bot. She's a thoughtful little composer who:

- 🎯 **Knows 24 different moods** — from "a dentist needs a clinical nudge" to "a salon needs festival energy" — each trigger gets its own personality
- 🏗️ **Runs a full HTTP server** — all 5 judge endpoints, clean and ready (`/context`, `/tick`, `/reply`, `/healthz`, `/metadata`)
- 💬 **Handles real conversations** — detects auto-replies, understands YES vs STOP, switches Hindi/English mid-chat like a desi friend
- 🛡️ **Validates herself** — checks her own output, retries if something's off. accountability era ✅
- 📦 **Ships with 25 pre-generated messages** — anchored on real numbers, real data, real feels

---

## 🚀 Run it yourself (seriously, 3 minutes)

```bash
# grab the goods
pip install flask requests

# get a free key → openrouter.ai
export OPENROUTER_API_KEY=your_key_here

# wake her up
python server.py

# test one message (CLI magic)
python bot.py trg_001_research_digest_dentists

# watch a full convo unfold
python conversation_handlers.py
```

---

## 🧠 How she thinks

```
you send a trigger
        ↓
Vera picks her strategy  (24 routing variants — no one-size-fits-all here)
        ↓
she reads the room       (category voice + merchant data + customer history)
        ↓
she writes the message   (Llama 3.3 70B, temp=0, calm and precise)
        ↓
she checks her work      (validates CTA, send_as, body — retries if needed)
        ↓
💌 one perfect WhatsApp message lands
```

---

## 💭 Honest tradeoffs (no cap)

**Why 24 routing variants and not one big prompt?**
One prompt = average everything. Routing = sharp, specific, *actually good*. A dentist message that says "38% fewer caries from a 2,100-patient JIDA trial" hits different than "great dental tips!" You feel me.

**Why Llama 3.3 70B free tier?**
Free tools, same score — challenge rules. Llama handles Hindi-English code-mix beautifully. Only gap: subtle Hindi idioms are slightly formal sometimes. Would upgrade to Claude Sonnet for pure poetry. 🫶

**Things I skipped (for now):**
- Semantic search over digest items *(routing gets 90% of the value anyway)*
- Full conversation cadence planner *(suppression logic covers it for now)*
- Real-time slot lookup *(payload slots work fine for seed data)*

---

## 💡 What would make Vera even better

1. **50+ turn conversation history per merchant** — she'd know your favorite topics, your reply speed, everything
2. **Locality-level peer data** — "Lajpat Nagar dentists" hits harder than "Delhi dentists"
3. **WhatsApp template approval status** — knowing what's pre-approved changes the whole opening strategy

---

## 📁 What's in the box

| file | what it does |
|---|---|
| `bot.py` | the heart — `compose(category, merchant, trigger, customer?)` |
| `server.py` | the face — all 5 Flask endpoints, judge-ready |
| `conversation_handlers.py` | the brain — multi-turn, auto-reply, intent, language |
| `submission.jsonl` | 25 pre-loved outputs, hand-tuned |
| `dataset/` | the world Vera lives in |
| `requirements.txt` | just flask + requests, lightweight baby |

---

## 🌐 She's live right now

```
https://web-production-97d4b.up.railway.app
```

Say hi at `/v1/healthz` — she'll tell you she's okay 🩵

---

*Built with way too much love and just enough caffeine. — Jayesh* ☕
