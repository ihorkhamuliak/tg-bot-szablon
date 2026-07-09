**English** | [Українська](README_UA.md)

# Telegram bot for small business (n8n) — template

A ready-made building block: a Telegram bot that **answers customers, books appointments, and sends reminders** — configurable for a new business in one evening, with no logic rewriting.

> 📦 Included: the ready-to-import workflow [n8n_workflow.json](n8n_workflow.json) + a step-by-step setup guide [SETUP.md](SETUP.md) (UA). Import into n8n, fill in the CONFIG node — done.

## What it does

- 💬 **Answers questions (FAQ)** with conversation memory — the customer never repeats themselves.
- 📝 **Books appointments:** collects name → service/class → date & time → phone, and saves to a sheet.
- ⏰ **Reminders** 24h and 2h before the visit — automatically.
- 🔔 **Notifies the owner** about every new booking.
- 🙋 **Escalation:** on a complaint or unusual request the bot replies politely and hands off to the owner.
- 🛡️ **Validation:** checks the phone number, no duplicate bookings per customer.

## Who it's for

Studios, workshops, salons, any appointment-based small business where customers write on Telegram and need to be booked.

## Tech stack

- **n8n** (Cloud or self-hosted) — orchestration
- **Claude API** — dialogue and customer understanding
- **Google Sheets** — bookings and conversation history
- **Telegram Bot API** — communication channel

## How it works

```
Customer on Telegram
      │
      ▼
   n8n workflow ── Claude (dialogue) ── Google Sheets (booking + memory)
      │
      ├─ confirmation to the customer
      ├─ notification to the owner
      └─ reminders 24h / 2h
```

## Configuring for a client

A single `CONFIG` node is the heart of the template. You only change: business name, city, list of services, prices, FAQ (address, hours, parking). The rest of the logic stays untouched. Full guide: [SETUP.md](SETUP.md).

## Get it implemented

Setup for a new business, training, support — get in touch:
**Telegram:** [@Ihor_0O](https://t.me/Ihor_0O) · **Email:** hamulakigor7@gmail.com

---

© 2026 Ihor Khamuliak.
