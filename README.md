# ⚡ SlotEase — Local Service Booking Website

> A fully responsive, zero-dependency booking website that eliminates phone tag between customers and local service providers — built with pure HTML5, CSS3, and Vanilla JavaScript.

---

## 📌 Table of Contents

- [Problem Statement](#-problem-statement)
- [Solution](#-solution)
- [Live Demo](#-live-demo)
- [Screenshots](#-screenshots)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Design System](#-design-system)
- [Getting Started](#-getting-started)
- [Roadmap](#-roadmap)
- [Accessibility](#-accessibility)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🔍 Problem Statement

Local service providers — plumbers, electricians, tutors, salons — waste hours every day:

- Answering repetitive phone calls to check availability
- Managing paper diaries and whiteboards
- Dealing with double bookings and scheduling conflicts
- Chasing customers for no-show appointments

Customers face the same frustration: long hold times, missed calls, and zero transparency into when a professional is actually free.

---

## 💡 Solution

**SlotEase** is a real-time service booking platform where:

- Customers browse live availability and pick a time slot in under 60 seconds
- Providers never get double-booked — the calendar updates instantly on confirmation
- Both parties receive automated SMS and email reminders (24 hours + 1 hour before)
- No account required to browse; minimal friction to book

---

## 🚀 Live Demo

> Open `index.html` directly in any modern browser — no build step, no server required.

```bash
# Clone the repo
git clone https://github.com/your-username/slotease.git

# Open in browser
open index.html
# or on Windows:
start index.html
```

---

## 📸 Screenshots

| Section | Description |
|---|---|
| **Hero + Live Slot Grid** | Real-time slot selector with open / booked / selected states |
| **How It Works** | 4-step process cards (responsive grid) |
| **Services** | Category cards — Plumber, Electrician, Tutor, Salon |
| **Booking Modal** | Full form with validation + success confirmation |
| **Footer** | 4-column info grid with contact links |

---

## ✨ Features

### Core Functionality
- **Live slot grid** — Switch between service types (Plumber / Electrician / Tutor / Salon) to see real-time availability
- **Slot selection** — Click any open slot; it highlights and the confirm button activates
- **Instant confirmation** — Confirmed slots flip to "booked" immediately; slot count updates live
- **Booking modal** — Full form with name, phone, service, date, and time inputs
- **Form validation** — All fields required before submission; inline error toast
- **Success screen** — Post-booking confirmation with reminder notice inside the modal

### UX Details
- **Animated toast notifications** — Slide-up confirmation messages on key actions
- **Hamburger navigation** — Animated 3-bar → X toggle with ARIA state management
- **Smooth scroll** — All internal anchor links scroll smoothly
- **Sticky header** — Frosted-glass navbar stays visible on scroll
- **Min date enforcement** — Date picker prevents selecting past dates

### Responsive Design
- Mobile-first layout (single column, default)
- Tablet layout at `768px` — 2-column grids
- Desktop layout at `1024px` — 4-column grids for steps and services
- Fluid typography with `clamp()` — zero layout breakage at any viewport width

---

## 🛠 Tech Stack

| Layer | Technology | Details |
|---|---|---|
| **Structure** | HTML5 | Semantic landmark tags throughout |
| **Styling** | CSS3 | Grid, Flexbox, custom properties, `clamp()` |
| **Interactivity** | Vanilla JavaScript | Zero frameworks, zero dependencies |
| **Fonts** | Google Fonts | Montserrat + Open Sans |
| **Icons** | Unicode Emoji | No external icon library needed |

**Dependencies: none.** No npm, no bundler, no framework. One file, opens anywhere.

---

## 📁 Project Structure

```
slotease/
├── index.html        # Complete website (HTML + CSS + JS in one file)
└── README.md         # This file
```

All CSS is embedded in `<style>` tags and all JavaScript is in `<script>` tags at the bottom of `index.html`. This keeps the project truly zero-dependency and easy to inspect.

---

## 🎨 Design System

### Colour Palette

| Token | Hex | Usage |
|---|---|---|
| `--navy` | `#0F1B2D` | Page background (trust, depth) |
| `--navy-mid` | `#162236` | Card / header backgrounds |
| `--teal` | `#00C9A7` | Primary action, availability, accents |
| `--teal-dark` | `#00A88D` | Button hover state |
| `--coral` | `#FF6B6B` | Alerts, "few slots left" indicators |
| `--white` | `#F8FAFC` | Headings and primary text |
| `--slate` | `#64748B` | Secondary / meta text |
| `--slate-lt` | `#94A3B8` | Body copy, descriptions |

### Typography

| Role | Family | Weights Used |
|---|---|---|
| Headlines | Montserrat | 800 (hero), 700 (sections), 600 (cards) |
| Body | Open Sans | 600 (labels), 500 (nav), 400 (body copy) |

> Strictly 2 font families and 3 weights each — as per the brief.

### Spacing & Radius

```css
--radius-sm:  8px   /* Slots, inputs */
--radius-md:  16px  /* Cards */
--radius-lg:  24px  /* Booking demo, modal */
```

### Layout Breakpoints

```css
/* Mobile-first base  → single column */
@media (min-width: 768px)  { /* Tablet  → 2-column grids    */ }
@media (min-width: 1024px) { /* Desktop → 4-column grids    */ }
```

---

## 🏁 Getting Started

### Prerequisites

- Any modern browser (Chrome, Firefox, Safari, Edge)
- No Node.js, no build tools, no package manager

### Run Locally

```bash
# 1. Clone
git clone https://github.com/your-username/slotease.git
cd slotease

# 2. Open
open index.html
```

### Deploy to GitHub Pages

```bash
# 1. Push to GitHub
git add .
git commit -m "Initial commit"
git push origin main

# 2. Go to repo Settings → Pages
# 3. Source: Deploy from branch → main → / (root)
# 4. Your site is live at:
#    https://your-username.github.io/slotease/
```

### Deploy to Netlify (drag & drop)

1. Go to [netlify.com](https://netlify.com) → "Deploy manually"
2. Drag the project folder onto the deploy zone
3. Done — live URL in seconds

---

## 🗺 Roadmap

The current build is a fully functional frontend with simulated state. Here's what a production version would add:

- [ ] **Backend API** — Node.js / Python endpoint for real booking persistence
- [ ] **Database** — PostgreSQL or Firebase for provider calendars and bookings
- [ ] **Auth** — Phone OTP login for customers; email login for providers
- [ ] **Real reminders** — Twilio SMS + SendGrid email integration
- [ ] **Provider dashboard** — Manage availability, view upcoming bookings, set working hours
- [ ] **Payment gateway** — Razorpay / Stripe integration for advance booking deposits
- [ ] **Search & filters** — Find providers by location, rating, and price range
- [ ] **Reviews system** — Post-service ratings tied to completed bookings
- [ ] **PWA** — Service worker + manifest for installable offline-capable app

---

## ♿ Accessibility

This project targets **WCAG 2.1 AA** compliance:

| Feature | Implementation |
|---|---|
| Skip link | Visible on keyboard focus — jumps to `#main-content` |
| Semantic HTML | `<header>`, `<nav>`, `<main>`, `<article>`, `<footer>`, `<section>` throughout |
| ARIA labels | All interactive elements have descriptive `aria-label` attributes |
| ARIA live regions | Slot count, confirmation area, and toast use `aria-live="polite"` |
| ARIA states | `aria-expanded`, `aria-selected`, `aria-disabled` kept in sync with JS state |
| Keyboard nav | Full keyboard operability — tabs, enter, escape on modal |
| Focus management | Modal traps focus; `book-name` receives focus on open |
| Reduced motion | `@media (prefers-reduced-motion: reduce)` disables all animations |
| Colour contrast | Teal `#00C9A7` on navy `#0F1B2D` passes AA at all text sizes |
| Disabled states | Booked slots use `disabled` + `aria-disabled="true"` |

---

## 🧩 HTML Landmarks Used

```html
<header>   → Logo, branding, and sticky navigation
<nav>      → Desktop nav links + mobile hamburger menu
<main>     → All primary page content
<section>  → Hero, How It Works, CTA banner
<article>  → Service cards, testimonial cards, step cards
<footer>   → Contact info, site links, copyright
```

---

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature-name`
3. Commit your changes: `git commit -m "Add: your feature description"`
4. Push to the branch: `git push origin feature/your-feature-name`
5. Open a Pull Request

Please keep PRs focused — one feature or fix per PR. Follow the existing code style (no frameworks, comment your CSS sections).

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

Built as a solution to the real-world problem of inefficient local service scheduling.

> *"Stop playing phone tag. Book your first slot free."*

---

<p align="center">Made with ❤️ for local communities</p>
