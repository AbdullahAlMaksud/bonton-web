# Bonton (বন্টন) — Expense Sharing & Settlement System

**Short Description:** Bonton (বন্টন) একটি আধুনিক, লোকাল-ফার্স্ট এবং গোপনীয়তাবান্ধব ওয়েব অ্যাপ্লিকেশন যা গ্রুপভিত্তিক খরচ ভাগাভাগি, স্মার্ট ঋণ সরলীকরণ এবং সেটেলমেন্ট হিসাবের সমাধান করে।

**Technology Badges:**
[![pnpm](https://img.shields.io/badge/pnpm-12-F69220?style=flat-square&logo=pnpm&logoColor=white)](https://pnpm.io/)
[![Next.js](https://img.shields.io/badge/Next.js-16-black?style=flat-square&logo=next.js&logoColor=white)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19-61DAFB?style=flat-square&logo=react&logoColor=black)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-6.0-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-v4-06B6D4?style=flat-square&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Jest](https://img.shields.io/badge/Jest-30-C21325?style=flat-square&logo=jest&logoColor=white)](https://jestjs.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

---

## Table of Contents

- [About](#about)
- [Features](#features)
  - [Splitting Models](#splitting-models)
  - [Theme Palette](#theme-palette)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Available Scripts](#available-scripts)
  - [Project Structure](#project-structure)
  - [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## About

**Bonton (বন্টন)** হলো যৌথ খরচের জটিল হিসাব-নিকাশ অত্যন্ত সহজ ও কার্যকরভাবে সমাধানের জন্য তৈরি একটি লোকাল-ফার্স্ট ওয়েব অ্যাপ্লিকেশন। ভ্রমণ, মেস কিংবা বন্ধুদের যেকোনো আড্ডায় কে কত টাকা পরিশোধ করলো এবং কার কাছে কার কত পাওনা—তা নির্ভুলভাবে বের করতে অ্যাপ্লিকেশনটি বিশেষ অ্যালগরিদম ব্যবহার করে। 

অ্যাপ্লিকেশনটির প্রধান দিক হলো সর্বোচ্চ গোপনীয়তা—এখানে কোনো সার্ভার ডেটাবেস বা অ্যাকাউন্ট রেজিস্ট্রেশনের প্রয়োজন নেই; সমস্ত গ্রুপের তথ্য ও খরচের হিসাব ব্রাউজারের লোকাল স্টোরেজে নিরাপদে সংরক্ষিত থাকে।

---

## Features

- **লোকাল-ফার্স্ট আর্কিটেকচার (Local-First Architecture)**: কোনো ক্লাউড সার্ভার বা লগইনের প্রয়োজন নেই; ব্যবহারকারীর সমস্ত ডেটা ব্রাউজারের স্টোরেজে সম্পূর্ণ প্রাইভেট ও সুরক্ষিত থাকে।
- **স্মার্ট ঋণ সরলীকরণ (Smart Debt Simplification)**: গ্রিডি সেটেলমেন্ট অপটিমাইজেশন অ্যালগরিদমের মাধ্যমে সর্বনিম্ন সংখ্যক ট্রানজ্যাকশনে সবার লেনদেন নিষ্পত্তির হিসাব বের করে।
- **বহুভাষিক সুবিধা (Bilingual Interface)**: বাংলা ও ইংরেজি উভয় ভাষায় খুব সহজেই ভাষা পরিবর্তন করে ব্যবহারের সুবিধা (i18next)।
- **ডায়নামিক অ্যানিমেশন ও প্রিমিয়াম ডিজাইন (Dynamic Motion)**: মসৃণ ভেক্টর লোগো অ্যানিমেশন (Framer Motion), গ্লাস মরফিজম ইন্টারফেস এবং রেসপনসিভ লেআউট।
- **অ্যাডভান্সড এক্সপোর্ট টুলস (Advanced Export Utilities)**:
  - উচ্চমানের ভেক্টর PDF ব্যালেন্স শিট তৈরি ও ডাউনলোড।
  - তাৎক্ষণিক ব্যবহারের জন্য ফরম্যাটেড Markdown রিপোর্ট কপি ও এক্সপোর্ট।
  - প্রতিটি সেটেলমেন্ট লেনদেনের জন্য সুন্দর ভিজ্যুয়াল রসিদ/ইমেজ জেনারেশন।
- **মেম্বার ম্যানেজমেন্ট ও রি-ব্যালেন্সিং**: প্রয়োজনমতো গ্রুপের সদস্য যোগ বা অপসারণ করলে স্বয়ংক্রিয়ভাবে ব্যালেন্স পুনঃহিসাব।

### Splitting Models

1. **Equal Split (সমান ভাগ)**: নির্বাচিত সদস্যদের মাঝে খরচ সমান ভাগে ভাগ করা।
2. **Percentage Split (শতাংশ অনুযায়ী ভাগ)**: প্রতিটি সদস্যের জন্য নির্দিষ্ট শতকরা হার নির্ধারণ করে খরচ ভাগ।
3. **Custom Fixed Split (নির্দিষ্ট পরিমাণ অনুযায়ী ভাগ)**: ব্যক্তিভেদে নির্দিষ্ট টাকার অঙ্ক সরাসরি নির্ধারণের সুবিধা।
4. **Initial Bills Pre-deduction (প্রাথমিক বিল বাদ দিয়ে ভাগ)**: বিলের অংশবিশেষ কারো ব্যক্তিগত খরচের হলে তা আগে বাদ দিয়ে অবশিষ্ট অঙ্ক অন্যদের মধ্যে ভাগ করা।
5. **Multiple Payers (একাধিক পেয়ার)**: এক খরচে একাধিক ব্যক্তি অংশ নিয়ে টাকা প্রদান করার সম্পূর্ণ সমর্থন।

### Theme Palette

অ্যাপ্লিকেশনটিতে চোখের স্বাচ্ছন্দ্য অনুযায়ী ৫টি আধুনিক থিম সংযুক্ত রয়েছে:
1. **লাইট (Light)**: উজ্জ্বল এবং পরিচ্ছন্ন ইন্টারফেস।
2. **ডার্ক (Dark)**: আধুনিক রাতের থিম ও চোখের জন্য আরামদায়ক।
3. **সেপিয়া (Sepia)**: উষ্ণ কাগজের টোন ও ক্লাসিক রিডিং ফিল।
4. **ফরেস্ট (Forest)**: স্নিগ্ধ সবুজ প্রকৃতির আভা।
5. **ওশান (Ocean)**: গভীর নীল সমুদ্রের আধুনিক ভাব।

---

## Tech Stack

| ক্যাটাগরি | টেকনোলজি / টুল | বিবরণ |
| :--- | :--- | :--- |
| **Package Manager** | [pnpm](https://pnpm.io/) | v12 ফাস্ট, ডিস্ক-স্পেস সাশ্রয়ী প্যাকেজ ম্যানেজার |
| **Framework** | [Next.js 16](https://nextjs.org/) | App Router, Server/Client Components, Turbopack |
| **Language** | [TypeScript](https://www.typescriptlang.org/) | টাইপ-সেফ কোডবেস (v6.0 স্টাবল) |
| **Styling** | [Tailwind CSS v4](https://tailwindcss.com/) & CSS Variables | আধুনিক ইউটিলিটি-ফার্স্ট ও থিমিং সিস্টেম |
| **UI Components** | [Radix UI](https://www.radix-ui.com/) & [shadcn/ui](https://ui.shadcn.com/) | এক্সেসিবল হেডলেস ইউআই কম্পোনেন্টস |
| **Animations** | [Motion](https://motion.dev/) (`motion/react`) | স্মুথ ভেক্টর পাথ অ্যানিমেশন ও ট্রানজিশন |
| **State & Storage** | [Zustand](https://zustand.docs.pmnd.rs/) | লোকালস্টোরেজ হাইহাইড্রেশন পারসিস্টেন্স স্টোর |
| **Testing** | [Jest](https://jestjs.io/) & `@jest/globals` | অফিসিয়াল Next.js টেস্ট রানার (ESM মোড) |
| **Localization** | [i18next](https://www.i18next.com/) & [react-i18next](https://react.i18next.com/) | বাংলা ও ইংরেজি ডায়নামিক অনুবাদ |
| **PDF Generation** | [jsPDF](https://github.com/parallax/jsPDF) | ক্লায়েন্ট-সাইড ভেক্টর PDF ডকুমেন্টস |
| **Markdown Engine** | [Unified](https://unifiedjs.com/), [Remark](https://remark.js.org/), MDAST | স্ট্রাকচার্ড মার্কডাউন প্রসেসিং ও এক্সপোর্ট |
| **Icons** | [Lucide React](https://lucide.dev/) | আধুনিক এবং পরিষ্কার আইকন লাইব্রেরি |

---

## Getting Started

### Prerequisites

প্রজেক্টটি চালানোর জন্য আপনার কম্পিউটারে নিচের সফটওয়্যারগুলো ইনস্টল থাকতে হবে:
- **Node.js**: `v20.x` বা তার পরবর্তী ভার্সন (`v24.x` সাজেস্টেড)
- **pnpm**: `v10.x` বা তার পরবর্তী ভার্সন (`v12.x` সাজেস্টেড)

### Installation

১. রিপোজিটরিটি ক্লোন করুন:
```bash
git clone https://github.com/AbdullahAlMaksud/bonton-web.git
```

২. প্রজেক্ট ফোল্ডারে প্রবেশ করুন:
```bash
cd bonton-web
```

৩. ডিপেন্ডেন্সিগুলো ইনস্টল করুন:
```bash
pnpm install
```

৪. ডেভেলপমেন্ট সার্ভার চালু করুন:
```bash
pnpm dev
```

ব্রাউজারে [http://localhost:3000](http://localhost:3000) লিংকে ভিজিট করে অ্যাপ্লিকেশনটি ব্যবহার করুন।

---

## Available Scripts

| কমান্ড | বিবরণ |
| :--- | :--- |
| `pnpm dev` | Turbopack সহ লোকাল ডেভেলপমেন্ট সার্ভার চালু করে |
| `pnpm build` | প্রোডাকশনের জন্য অপটিমাইজড বিল্ড তৈরি করে |
| `pnpm start` | প্রোডাকশন বিল্ড সার্ভার চালু করে |
| `pnpm lint` | ESLint দিয়ে কোডের কোয়ালিটি ও সিনট্যাক্স যাচাই করে |
| `pnpm test` | Jest দিয়ে সমস্ত ইউনিট এবং ক্যালকুলেশন টেস্ট রান করে |

---

## Project Structure

প্রজেক্টটি আধুনিক **src-first** ডিরেক্টরি স্ট্রাকচার অনুসরণ করে তৈরি:

```text
bonton-web/
├── public/                     # স্ট্যাটিক অ্যাসেটস ও ব্র্যান্ড আইকন
├── src/
│   ├── app/                    # Next.js App Router পেজ ও গ্লোবাল লেআউট
│   │   ├── globals.css         # গ্লোবাল স্টাইলিং ও থিম কালার ভেরিয়েবল
│   │   ├── layout.tsx          # রুট লেআউট (প্রোভাইডার ও শেল র‍্যাপার)
│   │   ├── page.tsx            # হোম / ড্যাশবোর্ড ভিউ
│   │   └── groups/             # গ্রুপ ক্রিয়েশন, ভিউ, এক্সপোর্ট ও সেটেলমেন্ট রুট
│   ├── components/
│   │   ├── common/             # অ্যাপ শেল, থিম প্রোভাইডার ইত্যাদি
│   │   └── ui/                 # পুনঃব্যবহারযোগ্য shadcn ও কাস্টম UI কম্পোনেন্ট
│   ├── features/
│   │   └── splitly/components/ # স্প্লিট ও হিসাব সংক্রান্ত নির্দিষ্ট কম্পোনেন্টস
│   ├── shared/
│   │   ├── lib/                # ক্যালকুলেশন, কারেন্সি, i18n ও এক্সপোর্ট ইউটিলিটি
│   │   └── types/              # ইউনিফাইড টাইপস্ক্রিপ্ট টাইপ ডেফিনিশন
│   ├── store/                  # Zustand স্টেট স্টোর (লোকাল স্টোরেজ সিঙ্ক)
│   └── __tests__/              # Jest ইউনিট টেস্ট স্যুট (সেটেলমেন্ট, ইমেজ ও মার্কডাউন)
├── doc/                        # প্রজেক্ট ডকুমেন্টেশন ও লজিক স্পেসিফিকেশন
├── jest.config.mjs             # Next.js Jest টেস্ট কনফিগারেশন
├── next.config.ts              # Next.js কনফিগারেশন
├── package.json                # প্রজেক্ট মেটাডেটা, ডিপেন্ডেন্সি ও স্ক্রিপ্টস
└── tsconfig.json               # TypeScript কনফিগারেশন
```

---

## Deployment

প্রজেক্টটি স্ট্যাটিক কিংবা সার্ভারলেস হিসেবে সহজেই Vercel, Netlify অথবা যেকোনো Node.js হোস্টিংয়ে ডেপ্লয় করা যায়:

১. প্রোডাকশন বিল্ড তৈরি করুন:
```bash
pnpm build
```

২. প্রোডাকশন রান করুন:
```bash
pnpm start
```

---

## Contributing

যেকোনো ধরনের বাগ রিপোর্ট, ফিচার আইডিয়া কিংবা কোড কন্ট্রিবিউশন আন্তরিকভাবে স্বাগত জানানো হয়! 

১. রিপোজিটরিটি Fork করুন  
২. আপনার ফিচারের জন্য নতুন Branch তৈরি করুন (`git checkout -b feature/amazing-feature`)  
৩. পরিবর্তনগুলো Commit করুন (`git commit -m 'feat: add some amazing feature'`)  
৪. আপনার Branch-এ Push করুন (`git push origin feature/amazing-feature`)  
৫. একটি Pull Request ওপেন করুন  

---

## License

এই প্রজেক্টটি **MIT License** এর অধীনে প্রকাশিত। বিস্তারিত জানতে [LICENSE](LICENSE) ফাইলটি দেখুন।

---

## Contact

**Abdullah Al Maksud**

- **Email**: [maksud.workspace@gmail.com](mailto:maksud.workspace@gmail.com)
- **Website**: [abdullahalmaksud.com](https://abdullahalmaksud.com)
- **LinkedIn**: [@AbdullahAlMaksud](https://linkedin.com/in/AbdullahAlMaksud)
- **GitHub**: [@AbdullahAlMaksud](https://github.com/AbdullahAlMaksud)
