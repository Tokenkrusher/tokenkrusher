<div align="center">

# TokenKrusher

### Crush your Claude Code token spend.

**Keep every chat cheap, focused and on course.**

![Price](https://img.shields.io/badge/price-%C2%A32.50%20%2F%20month-3b9cff?style=for-the-badge)
![Platform](https://img.shields.io/badge/Claude%20Code-plugin-f5c518?style=for-the-badge)
![Private](https://img.shields.io/badge/runs-100%25%20local-7cc0ff?style=for-the-badge)

[**Subscribe for £2.50 / month →**](https://buy.stripe.com/3cIfZg4JveA28hr3dm6c000) · [**Download the Console →**](https://github.com/Tokenkrusher/tokenkrusher/releases/latest)

</div>

---

TokenKrusher watches your Claude Code chats, spots wasted tokens, and steers every session back to its goal. It reads Claude Code's own local logs, so **your code and chats never leave your machine**.

> 🪙 **Tokens in, a big blue fist comes down.** On startup the desktop console plays a short line-art animation of exactly that. Yes, really.

## ✨ What you get

| | Benefit | How it works |
|---|---|---|
| 💸 | **Lower usage on long chats** | Spots waste (an expensive model doing light work, a chat whose context has ballooned) and offers a one-click fix. |
| 🧭 | **Chats that stay on target** | The **plan keel** re-states each chat's goal on every reply, so long sessions don't drift. |
| 🔁 | **Painless handoffs** | When a chat gets heavy, it writes a handoff pack so you start fresh without re-explaining. |
| 🪤 | **Stuck-chat detection** | Notices chats going in circles and suggests a way out. |
| 📈 | **Pace awareness** | Knows how fast you are burning your weekly allowance and tells you when to ease off or spend freely. |
| 👀 | **Visibility** | See every open chat, whether it is working or waiting, and what it costs. |
| ↩️ | **Private and reversible** | Everything is local, and every action can be undone with one command. |

## 🧰 Every feature

### 🔍 Waste detection (the tips)

TokenKrusher scans your chats and raises a tip, each with a one-click fix:

| Tip | What it catches |
|---|---|
| **Open chat not routed** | A chat running without cheaper-model routing, where routing would cut cost. |
| **Heavy chat, hand off?** | Context is large enough that a fresh chat with a handoff pack is cheaper. |
| **Context is huge** | Very large context being re-read on every turn. |
| **Cache is breaking** | Prompt caching is not holding, so you pay full price repeatedly. |
| **Cache expired, then re-written** | A long idle gap made the cache expire and be rebuilt. |
| **Resumed cold** | You came back to an old chat and it re-read tens of thousands of tokens. |
| **Resume check** | An advisory check before you resume a stale chat. |
| **Opus/Fable used for big look-ups** | A top-tier model doing plain reading and searching a cheaper one can do. |
| **Opus/Fable share is high** | Over the week, too much of your usage went to the most expensive tier. |
| **Same file read repeatedly** | The same unchanged file read over and over. |
| **Huge tool outputs** | Giant command or file outputs flooding the context. |
| **Chat may be going in circles** | A session that is looping and not getting anywhere. |
| **Long session, no plan file** | A long chat with no written plan to keep it honest. |

### 🛠️ One-click actions

- **Create plan file**: drafts a `PLAN-<task>.md` from the chat so work stays on goal.
- **Write task brief**: turns a rambling chat into a clear goal, constraints and acceptance criteria.
- **Add guard rules**: adds a managed block to your project's `CLAUDE.md` that stops the wasteful habit in new chats.
- **Hand off**: writes a handoff pack and moves the work into a fresh chat.
- **Undo**: every action is reversible, with `tokenkrusher undo`.

### 🧭 The plan keel

Attach a plan to a chat and TokenKrusher keeps it in view on every prompt. It checks whether the chat is drifting from the goal, and when a prompt points somewhere new it asks "this changes the plan, sure?" before treating it as a new direction.

### 📊 Usage and pace

- Live **weekly** and **5-hour** usage meters, with a projection to your reset time.
- **Pace advice** that adapts: when budget is tight it recommends cheaper routing and shorter chats; when you have headroom it tells you to use the strongest model freely.
- A **daily usage chart** showing what you used against what you would have used without TokenKrusher.
- A running estimate of **tokens and money saved**, plus runway gained and CO₂ avoided.

*Savings are shown as usage value at API list prices: an estimate, not a bill.*

### 🖥️ Desktop console (Windows)

[**Download TokenKrusher Console →**](https://github.com/Tokenkrusher/tokenkrusher/releases/latest) · same £2.50/month subscription as the plugin: the app asks for the email you paid with on first launch. It starts with Windows by default and stays running in the tray until you choose **Quit** there. Windows may show a SmartScreen warning because the app isn't code-signed yet: choose *More info → Run anyway*.

- A tray icon that changes colour with your usage and chat health.
- A compact window with live meters, your open chats, tips and the daily chart.
- A **locator bubble** that points at the chat a tip is about, even among many tabs.
- Toast popups for important tips, a weekly report, adjustable handoff threshold, and **Start with Windows**.
- A startup animation that is entirely unnecessary and we love it.

### ⌨️ In Claude Code

| Command | What it does |
|---|---|
| `/tokenkrusher-status` | ON/OFF, open chats, tip count. |
| `/tokenkrusher-tips` | Show tips for this chat with their one-click actions. |
| `/tokenkrusher-act <tip-id>` | Run a tip's action. |
| `/tokenkrusher-keel` | Plan-keel status for this chat. |
| `/tokenkrusher-console` | Subscribe and desktop console download links (same as this page). |
| `/tokenkrusher-activate <email>` | Unlock after subscribing. |

## 🎯 When it pays off most

TokenKrusher shines on **maintenance work**: bug fixes, small changes and long-running chats in an existing codebase, where context grows and routing, handoffs and the keel save real usage. For huge one-off build-outs, switch it off and back on when you return to everyday work.

## 💷 Pricing

**£2.50 per month.** Cancel any time. Billed immediately when you subscribe; no free trial.

1. [Subscribe here](https://buy.stripe.com/3cIfZg4JveA28hr3dm6c000).
2. In Claude Code, run `/tokenkrusher-activate <the email you paid with>`.

## 📦 Install (Claude Code 2.1.275 or later)

Run these in a normal terminal (not inside the chat panel):

```
claude plugin marketplace add Tokenkrusher/tokenkrusher
claude plugin install tokenkrusher@tokenkrusher
```

Windows is supported today.

## 🔒 Privacy

TokenKrusher runs on your own computer. It reads Claude Code's local usage files to give advice, and does **not** upload your code, chats or prompts anywhere. The only network request it makes is a licence check that sends the email you paid with to confirm your subscription is active. A few features run your own `claude` command in the background, which uses your own Claude plan.

## ❓ FAQ

**Will it change my files?** Only when you click an action, only inside the chat's own project, and every action can be undone.

**Does it block me from using any model?** No. It only advises. You stay in control.

**What if I'm offline?** A paid licence keeps working for up to 7 days offline.

**How do I cancel?** Use the link in your payment receipt. You keep access until the end of the period you paid for.

**Refunds?** If something is not right, email within 14 days of a payment and it will be refunded.

## 💬 Support

Questions, bugs and billing: **purecycle.contact@gmail.com**

---

<sub>Copyright TokenKrusher. All rights reserved. Provided as a compiled binary for use with Claude Code; no copying, modification, reverse engineering or resale. See `LICENSE.txt`.</sub>
