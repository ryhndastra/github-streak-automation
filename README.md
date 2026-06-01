# 🤖 github-streak-automation

![Active](https://img.shields.io/badge/status-active-brightgreen)
![GitHub Actions](https://img.shields.io/badge/GitHub-Actions-purple)
![Schedule](https://img.shields.io/badge/daily-08.00%20WIB-orange)
![Commits](https://img.shields.io/badge/commits-10--30%2Fday-blue)

Automated daily commits using GitHub Actions. Keeps the contribution graph green without manual effort.

---

## ⚙️ How it works

1. GitHub Actions triggers every day at 08.00 WIB via cron schedule
2. Workflow picks a **random commit count** between 10–30 for the day
3. Each commit appends a timestamped entry to `LAST_UPDATED` with a randomized message
4. A short random delay between commits makes the log timestamps look natural
5. Changes are pushed back to `main` automatically

## 📁 Structure

​```
.
├── .github/
│   └── workflows/
│       └── autocommit.yml   # workflow definition
└── LAST_UPDATED             # auto-updated log file
​```

## 🕐 Schedule

Cron: `0 1 * * *` — runs daily at 01:00 UTC (08:00 WIB)

To change the time, edit the cron value in `autocommit.yml`. Use [crontab.guru](https://crontab.guru) to generate the schedule.

## 🚀 Setup

1. Fork or clone this repo
2. Go to **Settings → Actions → General** → set Workflow permissions to **Read and write**
3. Trigger manually from the **Actions** tab to test, then let the cron handle the rest

---

*Built with GitHub Actions · No dependencies · No tokens required*
