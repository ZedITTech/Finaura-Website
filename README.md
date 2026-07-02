# Finaura

Most budgeting apps want you to link your bank account, ship your transaction history off to their servers, and just trust that a company's business model won't eventually mean monetizing your spending data. I never liked that trade. So I built something different: a finance app that actually works the way I plan my money, without asking me to hand my financial life over to a third party.

Finaura is my answer to that problem. It's a fully offline-first budgeting and financial planning app. Everything lives in your browser's local storage, there's no backend database, and nothing leaves your device unless you explicitly turn sync on.

## Why I made this

It started small, as a tool to manage my own budget, and it grew into a full personal finance platform because every time I hit a wall with an existing app, either the feature didn't exist or it was locked behind a subscription, I just built it myself instead.

A few things I wanted that I couldn't find anywhere else:

**Real budgeting, not just categorization.** Most apps will show you a pie chart of where your money went last month and call it budgeting. I wanted a proper zero-based, give-every-dollar-a-job planning grid, along with debt payoff strategies, goal funding plans, and real forecasting.

**Privacy as the default, not a paid tier.** No accounts required, no ad trackers, no relationships with data brokers. If you want to sync across your phone and laptop, that's opt-in and end-to-end encrypted. The app never sees your data either way.

**Something that gets smarter about my actual situation.** Finaura's Smart Insights engine and Veda, an on-device assistant with no external API calls, surface things like "you're about to miss a bill" or "this debt is costing you more than your investments are earning." All of it computed locally, from your own data, on your own device.

## What Finaura actually does

Finaura is a privacy-first personal finance app that runs entirely in your browser. It's installable as a PWA on desktop or mobile, doesn't require an account, and sends nothing to a server by default.

Here's what's in it:

- Zero-based budget planning with a full 12-month grid, rollover support, and per-paycheck planning
- Transaction tracking with running balances, CSV import, receipt attachments, and automatic categorization
- Bills, subscriptions, and gift/holiday tracking with recurrence and reminders
- Debt payoff planning (avalanche and snowball methods) with live balance projections
- Goals with funding-plan recommendations tailored to your target date or income
- Investment holdings, portfolio allocation, and retirement (FIRE) planning
- Credit score estimation with an actionable improvement checklist
- A tax estimator with withholding and quarterly-payment guidance
- Cash-flow forecasting with stress-test scenarios, like "what if I lose a paycheck" or "what if rent goes up"
- Smart Insights, a rules engine that watches every module and proactively flags what needs attention
- Veda, an on-device chat assistant you can ask things like "how much did I spend on groceries this month" and get an answer computed entirely on your own device

Everything is stored in IndexedDB, locally on your device. If you want to use Finaura across multiple devices, optional Google Drive or peer-to-peer sync is available, fully end-to-end encrypted, with the encryption key derived from your own PIN. The server, Google Drive in this case, only ever sees encrypted bytes. It has no way to read your data even if it wanted to.

## Where things stand

Finaura is live and stable, not a prototype or a waitlist page. It's built with React, TypeScript, and Dexie.js, deployed as a static site with a full CI pipeline, and backed by nearly 1,700 automated tests. It's the app I use myself, every week, which is honestly the best quality bar I know how to hold it to.

## The short version

Finaura is a privacy-first personal finance app that runs entirely offline in the browser: no backend, no account, no data collection. It handles full zero-based budgeting, debt payoff planning, investments, taxes, credit tracking, and an on-device assistant, all backed by optional end-to-end encrypted sync. I built it because I wanted a finance tool that treats privacy as a default, not a premium feature.

## Where to find it

[financial-aura.com](https://financial-aura.com)
