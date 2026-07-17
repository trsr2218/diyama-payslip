# Diyama PaySlip

A single-file Zambian payroll and payslip calculator by Diyama Solutions. Intended for the subdomain **payroll.diyama.online**.

## What it does

- Enter employee name, employer name, pay period month, and monthly gross salary (K).
- Computes Zambian statutory deductions:
  - **PAYE** using progressive monthly bands (defaults: 0% up to K5,100; 20% K5,100 to K7,100; 30% K7,100 to K9,200; 37% above K9,200).
  - **NAPSA** at 5% of gross, capped at K1,342.40 per month.
  - **NHIMA** at 1% of gross (can be toggled off per payslip).
- Shows a full breakdown with an emphasized **NET PAY** figure.
- Generates a branded payslip and downloads it as a **PDF** (jsPDF).
- Saves employees/payslips to **localStorage** so you can reopen them later.
- All tax rates and bands are **editable** in the Tax settings panel and persist on the device.

## Usage

Just open `index.html` in any modern browser. No build step, no server, no install. Everything runs client-side and all data stays on the device.

## Notes

- Currency is shown as Zambian Kwacha, e.g. `K5,100.00`.
- Figures are estimates for guidance only. Zambian tax bands, NAPSA ceilings and NHIMA rates can change, and individual circumstances (allowances, benefits, exemptions) may affect the final amount. Confirm with the Zambia Revenue Authority or a qualified payroll professional before paying.

## Tech

- Single self-contained `index.html` (inline CSS + JS).
- Fonts: Playfair Display + DM Sans (Google Fonts).
- PDF export: jsPDF 2.5.1 (CDN).
- Follows the shared Diyama Solutions app design system (teal/gold palette, sticky wordmark header, footer).
