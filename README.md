# ZoeiStore – Import Order & E-commerce Profit Tracker

A business app for the full import-to-sale cycle of an online store: buying from **Alibaba**, shipping through agents to **Kenya**, and selling on **Jumia**.

## Features

| Area | What it does |
|---|---|
| **Dashboard** | Total invested, expected profit, money per agent, sea vs air freight split, biggest orders |
| **Shipment pipeline** | Not shipped → Shipped → Arrived at agent → In transit to Kenya → Received |
| **Orders** | Photo cards with filters by status and agent, plus search |
| **Cost maths** | USD → KSh at a set exchange rate, agent fees, true cost per piece, colour variants |
| **Pricing** | Profit per piece, margin and break-even price after Jumia commission and fees |
| **Jumia** | Stock and sales recording, linked automatically to the import orders, one source of truth |
| **Needs attention** | Flags duplicate tracking numbers, shipped orders with no tracking, loss-making prices, missing agent fees |
| **Security** | 6-digit PIN (SHA-256 hashed) with auto-lock after 1–30 minutes of inactivity |

Also: product photo uploads, light and dark mode, responsive layout (sidebar on desktop, tab bar on phones).

## Tech

- HTML5, CSS, vanilla JavaScript
- Cloud document database and file storage
- Web Crypto API (SHA-256) for the PIN check
- Built with AI-assisted development (Claude)

## Running it

The app is one file, `index.html`. It saves its data through the Claude Artifacts runtime (`window.claude`), so it is meant to be opened as a Claude artifact. Opened as a plain web page it shows a message that it cannot load data.

The demo PIN in this repository is `123456`. To set your own, replace `PIN_HASH` in `index.html` with the SHA-256 hash of your PIN.
