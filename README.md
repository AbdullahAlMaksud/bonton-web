# Bonton — Expense Sharing & Settlement System

Bonton is a modern, local-first, privacy-friendly web application designed to simplify group expense sharing, optimize debt settlement, and manage shared financial balances.


<p align="left">
  <img src="https://img.shields.io/badge/pnpm-12.15.0-F69220?style=for-the-badge&logo=pnpm&logoColor=white" alt="pnpm" />
  <img src="https://img.shields.io/badge/Next.js-16.4.3-black?style=for-the-badge&logo=next.js&logoColor=white" alt="Next.js" />
  <img src="https://img.shields.io/badge/React-19.3.1-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-5-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-v4-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License" />
</p>

<p align="center">
  <img width="49%" alt="Photocard Studio screenshot 2" src="https://github.com/user-attachments/assets/7fb2772a-81c3-4ed1-8e48-80085db625fd" />
  <img width="49%" alt="Photocard Studio screenshot 1" src="https://github.com/user-attachments/assets/19ede9b5-7d45-4a7c-a404-daa69b46a1bb" />
</p>



## Table of Contents

- [About](#about)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## About

**Bonton (বন্টন)** is a local-first web application designed to make splitting shared expenses and settling debts simple and efficient. Whether you're traveling with friends, sharing expenses in a household, or organizing a group outing, Bonton helps calculate who paid what and who owes whom.

Its core focus is privacy. No server-side database or account registration is required. Group information, expenses, and settlement records are stored in the browser's local storage, keeping your financial data under your control.

## Features

- **Local-First Architecture:** No cloud server or login is required. All user data stays in browser storage, providing a private and convenient experience.
- **Smart Debt Simplification:** Uses a greedy settlement optimization algorithm to calculate settlements with the goal of minimizing the number of transactions required to settle everyone's balances.
- **Bilingual Interface:** Switch seamlessly between Bengali and English using i18next.
- **Dynamic Animations and Modern Design:** Features smooth vector logo animations powered by Motion, a glassmorphism-inspired interface, and responsive layouts.
- **Advanced Export Utilities:**
  - Generate and download high-quality, vector-based PDF balance sheets.
  - Copy or export formatted Markdown reports for immediate use.
  - Generate visually polished receipt images for individual settlement transactions.
- **Member Management and Rebalancing:** Add or remove group members and automatically recalculate balances accordingly.

### Splitting Models

Bonton supports multiple ways to divide expenses among group members.

1. **Equal Split:** Divide an expense equally among the selected members.
2. **Percentage Split:** Allocate expenses by assigning a specific percentage to each member.
3. **Custom Fixed Split:** Assign a specific monetary amount to each individual.
4. **Personal Expense Deduction:** Deduct personal expenses from an initial bill before splitting the remaining amount among the other members.
5. **Multiple Payers:** Allow multiple people to contribute payments toward a single expense.

### Themes

Bonton offers five modern themes designed to suit different preferences and lighting conditions.

| Theme | Description |
| --- | --- |
| **Light** | A bright, clean interface with a fresh and uncluttered appearance. |
| **Dark** | A modern dark theme designed for comfortable nighttime use. |
| **Sepia** | Warm paper tones with a classic reading-inspired aesthetic. |
| **Forest** | A soothing interface inspired by natural green shades. |
| **Ocean** | A contemporary visual style inspired by deep ocean blues. |

## Tech Stack

- **Package Manager:** [pnpm](https://pnpm.io/) v12 — Fast, disk-space-efficient package management.
- **Framework:** [Next.js 16](https://nextjs.org/) — App Router, Server and Client Components, and Turbopack.
- **Language:** [TypeScript 6.0](https://www.typescriptlang.org/) — A type-safe development experience.
- **Styling:** [Tailwind CSS v4](https://tailwindcss.com/) and CSS variables — Utility-first styling and a flexible theming system.
- **UI Components:** [Radix UI](https://www.radix-ui.com/) and [shadcn/ui](https://ui.shadcn.com/) — Accessible, reusable UI components.
- **Animations:** [Motion](https://motion.dev/) (`motion/react`) — Smooth vector-path animations and transitions.
- **State Management & Storage:** [Zustand](https://zustand.docs.pmnd.rs/) — State management with local storage persistence and hydration.
- **Testing:** [Jest](https://jestjs.io/) and `@jest/globals` — Unit testing for application logic and calculations.
- **Localization:** [i18next](https://www.i18next.com/) and [react-i18next](https://react.i18next.com/) — Dynamic Bengali and English translations.
- **PDF Generation:** [jsPDF](https://github.com/parallax/jsPDF) — Client-side PDF document generation.
- **Markdown Processing:** [Unified](https://unifiedjs.com/), [Remark](https://remark.js.org/), and MDAST — Structured Markdown processing and export.
- **Icons:** [Lucide React](https://lucide.dev/) — A clean, modern icon library.

## Getting Started

### Prerequisites

Ensure you have the following installed:

- [Node.js](https://nodejs.org/): Version `20.x` or later (`24.x` recommended)
- [pnpm](https://pnpm.io/installation): Version `10.x` or later (`12.x` recommended)

Install pnpm globally if needed:

```bash
npm install -g pnpm
```


### Installation

**1. Clone the repository**

```bash
git clone https://github.com/AbdullahAlMaksud/bonton-web.git
cd ghorial-web
```

**2. Install dependencies**

```bash
pnpm install
```

**3. Configure environment variables (If Needed)**

Create a `.env.local` file in the project root and configure the required variables using `.env.example` as your reference, if your local setup requires it.

See [Environment Variables](#environment-variables) for details.

**4. Start the development server**

```bash
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Environment Variables

Ghorial uses environment variables to configure application services and external integrations.

1. Create a `.env.local` file in the project root.
2. Review `.env.example` for available variables and their intended use.
3. Configure the required settings for MongoDB Atlas and GitHub API integration, as applicable.
4. Keep credentials and access tokens private.

Never commit your real `.env.local` file or expose private credentials in client-side code.


### Available Scripts

| Command | Description |
| --- | --- |
| `pnpm dev` | Start the local development server with Turbopack. |
| `pnpm build` | Create an optimized production build. |
| `pnpm start` | Start the production server. |
| `pnpm lint` | Check code quality and style using ESLint. |
| `pnpm test` | Run unit and calculation tests using Jest. |

### Project Structure

```text
bonton-web/
├── public/                     # Static assets and brand icons
├── src/
│   ├── app/                    # Next.js App Router pages and layouts
│   │   ├── globals.css         # Global styles and theme color variables
│   │   ├── layout.tsx          # Root layout and provider wrappers
│   │   ├── page.tsx            # Home and dashboard view
│   │   └── groups/             # Group, expense, export, and settlement routes
│   ├── components/
│   │   ├── common/             # Application shell and shared components
│   │   └── ui/                 # Reusable shadcn/ui and custom components
│   ├── features/
│   │   └── splitly/
│   │       └── components/     # Expense-splitting components
│   ├── shared/
│   │   ├── lib/                # Calculations, currency, i18n, and export utilities
│   │   └── types/              # Shared TypeScript type definitions
│   ├── store/                  # Zustand stores and local storage synchronization
│   └── __tests__/              # Jest unit tests for settlement, images, and Markdown
├── doc/                        # Project documentation and logic specifications
├── jest.config.mjs             # Jest test configuration
├── next.config.ts              # Next.js configuration
├── package.json                # Project metadata, dependencies, and scripts
└── tsconfig.json               # TypeScript configuration
```

### Deployment

Bonton can be deployed to [Vercel](https://vercel.com/) or another hosting platform that supports Next.js.

Before deploying, configure the environment variables required by your chosen storage integrations and ensure that the database and GitHub API settings are correct.

To build and run the production application:

```bash
pnpm build
pnpm start
```

For platform-specific instructions, consult the [Next.js deployment documentation](https://nextjs.org/docs/app/getting-started/deploying).


## Contributing

Contributions, bug reports, and feature suggestions are welcome.

1. Fork the repository.
2. Create a feature branch:

   ```bash
   git checkout -b feature/amazing-feature
   ```

3. Commit your changes:

   ```bash
   git commit -m "feat: add some amazing feature"
   ```

4. Push the branch:

   ```bash
   git push origin feature/amazing-feature
   ```

5. Open a pull request.

## License

Distributed under the **MIT License**. See [`LICENSE`](./LICENSE) for details.

## Contact

**Abdullah Al Maksud**

- **Email:** [maksud.workspace@gmail.com](mailto:maksud.workspace@gmail.com)
- **Website:** [abdullahalmaksud.com](https://abdullahalmaksud.com)
- **LinkedIn:** [@AbdullahAlMaksud](https://linkedin.com/in/AbdullahAlMaksud)
- **GitHub:** [@AbdullahAlMaksud](https://github.com/AbdullahAlMaksud)
