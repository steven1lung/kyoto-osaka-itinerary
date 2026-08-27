# Project: 7D6N Kyoto & Osaka Solo Runner's Gourmet & Specialty Coffee Itinerary Web App (Round 2)
# Scope: Day 4 Kifune Shrine (貴船神社) & Mount Kurama Eizan Scenic Railway Exploration Replacement

## Architecture
- **Single-Page Application (`index.html`)**: Self-contained web application using Vue 3 Global CDN for reactive DOM state, Tailwind CSS CDN with custom Kyoto Modern Wabi-sabi palette tokens, and inline/FontAwesome iconography. No build steps required.
- **Embedded Data Store (`ITINERARY_DATA`)**: Structured JSON inside `index.html` defining 11 top-level tabs (`overview`, `runStations`, `coffees`, `dining`, and `days` Day 1 through Day 7) and 63 time-slotted itinerary cards with category filter tags (`All 全部`, `🏃 晨跑與修復`, `☕ 精品咖啡`, `🍜 嚴選美饌`, `⛩️ 景點與文化`), verified opening hours, insider tips, and clickable Google Maps URLs.
- **Automated Verification Harness (`verify_itinerary.py`)**: Standalone Python 3 verification script utilizing `unittest`, `bs4` (BeautifulSoup4), and `/usr/bin/google-chrome --headless=new --dump-dom` asserting 100% data integrity, zero offal invariants, Day 4 Kifune Shrine schedule, and flawless DOM rendering (25/25 tests passing).
- **Source Plan Markdown (`kyoto_osaka_7d6n_itinerary_plan.md`)**: The master travel plan document located at `/usr/local/google/home/stevenlung/.gemini/jetski/brain/bd166d84-fabb-4cb7-914c-a915bbde528d/kyoto_osaka_7d6n_itinerary_plan.md`.

## Feature Inventory
| # | Feature | Description | Milestone | Source |
|---|---------|-------------|-----------|--------|
| 1 | `🌟 總覽 Overview Tab` | Trip highlights (dates, solo runner, zero-offal policy, daily iced americano), confirmed hotels (Super Hotel Shijo Kawaramachi & Onyado Nono Namba), and luggage forwarding (Ta-Q-Bin guide). | M2 | survey |
| 2 | `🏃 晨跑名所 & 跑步驛站 Tab` | 6 morning run routes (including Day 4 Nijo Castle Outer Moat ~5.7km 3 laps) + OSHMAN'S Kyoto & RUNNING BASE Osaka Castle "手ぶら" (empty-handed rental) guides (~¥1,200 pack). | M2 | survey |
| 3 | `☕ 07:30 冰美式精品地圖 Tab` | The 6 verified early-opening specialty roasters paired with each run (Weekenders, Kurasu Ebisugawa, here Kyoto, Walden Woods, Brooklyn Roasting Namba EKIKAN & Kitahama) with hours and tasting notes. | M2 | survey |
| 4 | `🍜 免預約排隊 & 零內臟美饌 Tab` | Zero-offal dining (strictly zero horumon, motsu, liver, tripe, tongue) including Day 4 Kifune Kawadoko dining (sansai soba / Wagyu beef set meal) and Gion Ushimitsu dinner. | M2 | survey |
| 5 | `📅 Day 4 Kifune Shrine Itinerary Cards` | Day 4 time slots: (1) 06:30-07:30 Nijo Castle Outer Moat Run (3 laps, ~5.7km), (2) 07:30-08:00 here Kyoto single-origin Iced Americano (08:00 opening), (3) 09:30-13:30 Kifune Shrine & Eizan Scenic Railway "Kirara", red lantern stone steps, mizu-uranai water divination, and Kawadoko sansai soba / Wagyu lunch (zero offal), (4) 15:30-17:15 Nanzen-ji & Suirokaku Aqueduct, (5) 18:30-20:30 Dinner at Gion Ushimitsu (low-temp Wagyu beef chazuke). | M2 | user_request |
| 6 | Kyoto Modern Wabi-Sabi Aesthetics | Warm off-white `#F9F8F6` background, `#1E2A38`/`#2B3A42` indigo headers/buttons, `#4A6B5B` matcha accents, slate grey, rounded cards (`rounded-2xl`), responsive mobile/desktop layout. | M2 | survey |
| 7 | Instant Tabbed Navigation & Category Filters | 11 top navigation tabs switching instantly without page reloads via Vue 3 reactive state. Category filter pills (`All 全部`, `🏃 晨跑與修復`, `☕ 精品咖啡`, `🍜 嚴選美饌`, `⛩️ 景點與文化`). | M2 | survey |
| 8 | Automated Verification Test Suite (`verify_itinerary.py`) | Python test harness checking 100% data model coverage, Day 4 Kifune Shrine invariants, zero offal guidelines, Google Maps links, and headless Chrome DOM rendering. | M1 | survey |
| 9 | Git Version Control & GitHub Remote Push | Git commit `ab2388f` and push to remote `origin master` (`git@github.com:steven1lung/kyoto-osaka-itinerary.git`). | M3 | user_request |

## Milestones
| # | Name | Scope | Dependencies | Status |
|---|------|-------|--------------|--------|
| 1 | M1: Exploration & Survey | 3 parallel Explorers to analyze plan markdown, index.html, verify_itinerary.py, and git remotes | none | DONE |
| 2 | M2: Implementation (Markdown, UI, Test Harness, Git Push) | Worker updates `kyoto_osaka_7d6n_itinerary_plan.md`, `index.html`, `verify_itinerary.py`, runs tests, commits and pushes to GitHub origin master | M1 | DONE |
| 3 | M3: Multi-Agent Verification & Integrity Audit | 2 Reviewers, 2 Challengers, 1 Forensic Auditor evaluate correctness, DOM rendering, test suite pass, and zero-offal adherence | M2 | DONE |

## Code Layout
- `/usr/local/google/home/stevenlung/.gemini/jetski/brain/bd166d84-fabb-4cb7-914c-a915bbde528d/kyoto_osaka_7d6n_itinerary_plan.md`: Master travel plan markdown.
- `/usr/local/google/home/stevenlung/teamwork_projects/kyoto_osaka_itinerary_website/index.html`: Vue 3 + Tailwind CSS interactive single-page app.
- `/usr/local/google/home/stevenlung/teamwork_projects/kyoto_osaka_itinerary_website/verify_itinerary.py`: Automated verification test harness.
