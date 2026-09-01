# Standard Deviation Calculator Online

A fast, lightweight, and responsive client-side **Standard Deviation Calculator** built using HTML, CSS, and Vanilla JavaScript.

## 🚀 Live Demo & Web Tool
You can use the fully deployed web application here:
👉 **[Standard Deviation Calculator - Global Tools Box](https://www.globaltoolsbox.online/2026/08/standard-deviation-calculator.html)**

---

## ⚡ Features
* **Instant Calculations:** Computes sample standard deviation, population standard deviation, mean, and variance in real-time.
* **100% Client-Side:** No server-side processing or API calls, ensuring high execution speed.
* **Complete Privacy:** User input numbers are processed directly in the browser and never stored or transmitted.
* **Zero Dependencies:** Pure Vanilla JavaScript without heavy external math frameworks.

---

## 🛠️ How It Works (JavaScript Logic)

```javascript
function calculateSD(numbers) {
  const n = numbers.length;
  if (n < 2) return null;

  // Step 1: Compute Mean
  const mean = numbers.reduce((sum, val) => sum + val, 0) / n;

  // Step 2: Compute Variance
  const varianceSample = numbers.reduce((sum, val) => sum + Math.pow(val - mean, 2), 0) / (n - 1);
  const variancePop = numbers.reduce((sum, val) => sum + Math.pow(val - mean, 2), 0) / n;

  return {
    mean: mean.toFixed(4),
    sampleSD: Math.sqrt(varianceSample).toFixed(4),
    populationSD: Math.sqrt(variancePop).toFixed(4)
  };
}
