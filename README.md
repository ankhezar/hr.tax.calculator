# 🇭🇷 Croatia Obrt Calculator 2026

A lightweight, single-page application (SPA) for calculating taxes and contributions for Croatian Sole Proprietorships (*Obrt*). Updated for the **2025/2026** tax regulations.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-2026.1-green.svg)
![Size](https://img.shields.io/badge/size-%3C15kb-orange.svg)

## 🌟 Features

*   **Dual Modes:**
    *   **Paušalni (Flat-rate):** Calculates fixed tax tiers based on the new **€60,000 limit**.
    *   **Dohodovni (Regular/Income-based):** Calculates tax based on actual profit, personal deductions, and specific city tax rates.
*   **Employment Status Toggle:** Calculations for "Main Job" (Glavno zanimanje) vs. "Side Job" (Uz rad).
*   **2026 Tax Rules:**
    *   Updated contribution bases projected for 2026.
    *   New City Tax logic (abolition of *Prirez*).
    *   Updated Personal Deduction (*Osobni odbitak*) logic (€7,200/year).
*   **City Selector:** Pre-configured tax rates for major Croatian cities (Zagreb, Split, Rijeka, Osijek, etc.) with a custom input option.
*   **UX/UI:**
    *   **Mobile-First Design:** Large touch targets and custom spinner inputs for accessibility.
    *   **Auto Dark Mode:** Detects and applies system color scheme preference automatically.
    *   **Multilingual:** Instant toggle between Croatian (HR), English (EN), and Slovenian (SL).
    *   **Contextual Help:** Tooltips and FAQs located directly next to relevant inputs.
*   **Zero Dependencies:** Pure HTML, CSS, and Vanilla JavaScript in a single file.

## 🚀 Live Demo

<!-- Replace the link below with your actual GitHub Pages link after deployment -->
[👉 Click here to view the Calculator](https://yourusername.github.io/your-repo-name)

## 🛠️ Installation & Usage

Since this is a client-side Single Page Application contained within one file, no build process or package manager is required.

### Local Development
1.  Clone the repository:
    ```bash
    git clone https://github.com/yourusername/croatia-obrt-calculator.git
    ```
2.  Open `index.html` in any modern web browser.

### Deployment (GitHub Pages)
1.  Go to your repository **Settings**.
2.  Click on **Pages** in the sidebar.
3.  Under **Build and deployment**, select **Source** -> `Deploy from a branch`.
4.  Select `main` (or `master`) and save.
5.  Your site will be live at `https://yourusername.github.io/repo-name/`.

## 📊 Logic & Tax Rules (2025/2026)

This calculator implements the following logic based on the latest Croatian tax amendments:

### 1. Paušalni Obrt (Flat-rate)
*   **Revenue Limit:** Increased to **€60,000**.
*   **Tax Tiers:** Based on annual revenue brackets (e.g., 0-5k, 5-8.5k... up to 60k).
*   **Tax Calculation:** `Tier Base` × `City Tax Rate` (calculated using the lower tax threshold of the selected city).
*   **Expenses:** Ignored for tax purposes.
*   **Contributions:** Fixed monthly amount (Main job) or annual percentage of tier base (Side job).

### 2. Dohodovni Obrt (Regular)
*   **Mandatory:** If revenue > €60,000.
*   **Contributions:** Calculated on the Minimum Monthly Base (projected ~€1,100 for 2026).
    *   MIO I (Pension I): 15%
    *   MIO II (Pension II): 5%
    *   Zdravstveno (Health): 16.5%
*   **Income Tax:** `(Revenue - Expenses - Contributions - Personal Deduction) × City Tax Rate`.
*   **Personal Deduction:** €7,200/year (€600/month) is automatically deducted from the tax base.

## 🤝 Contributing
Contributions are welcome!

## ⚠️ Disclaimer
This tool is for informational purposes only.
While every effort has been made to ensure the accuracy of the calculations based on the 2025/2026 projections, tax laws in Croatia change frequently. The values produced by this calculator should not be considered professional financial or tax advice. Always consult with a certified accountant (knjigovođa) before making business decisions.

## 📄 License
Distributed under the MIT License. See [License] for more information.
