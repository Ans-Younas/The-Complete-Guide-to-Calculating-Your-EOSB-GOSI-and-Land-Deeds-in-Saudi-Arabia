# LocalCalc: Saudi Labor Law & Real Estate Logic 🇸🇦

A lightweight, zero-dependency client-side utility for processing Saudi End of Service Benefits (EOSB), GOSI deductions, and traditional land unit conversions. 

**Live Demo:** [https://localcalc.site/](https://localcalc.site/)

## Why This Exists
Most existing calculators for Saudi labor laws rely on server-side processing, which means user salary data and contract dates leave the device. This project was built to handle complex labor math entirely on the client side using native JavaScript, ensuring 100% privacy and instant execution.

## Core Features Implemented
*   **EOSB Engine:** Calculates final settlement based on Articles 84, 85, and 87 of the Saudi Labor Law. Handles exact fractional year calculations and dynamically adjusts payouts for resignation vs. termination.
*   **GOSI Calculator:** Computes precise Social Insurance deductions.
*   **Land Unit Converter:** Translates regional real estate measurements (Sahm, Qirat, Feddan, Ottoman Donum) into standard square meters.
*   **Hijri / Gregorian Support:** Accurately calculates tenure across both calendar systems.

## Tech Stack
*   **Logic:** Native JavaScript (ES6) - No external math libraries required.
*   **UI (Live Site):** Responsive HTML/CSS with seamless English/Arabic (RTL) toggling.
*   **Architecture:** 100% Client-side execution. 

## Code Example: EOSB Calculation Concept
*(Include a small snippet of your actual JavaScript here so developers can see your coding style. Example below:)*

```javascript
// Simplified example of handling Article 85 (Resignation)
function calculateResignationPayout(baseAmount, yearsWorked) {
    if (yearsWorked < 2) return 0;
    if (yearsWorked >= 2 && yearsWorked < 5) return baseAmount / 3;
    if (yearsWorked >= 5 && yearsWorked < 10) return (baseAmount * 2) / 3;
    return baseAmount; // 10+ years gets full amount
}
