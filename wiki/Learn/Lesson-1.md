# 📚 Lesson 1 Concept: The Box Model & Typography

```html
<body
  class="bg-slate-900 text-slate-100 flex items-center justify-center min-h-screen"
></body>
```

---

how Tailwind handles dimensions and spacing.

### 1. Spacing (Padding & Margin)

Tailwind uses a numeric scale where `1 unit = 4px` (or `0.25rem`).

- **`p-4`**: Adds padding on **all sides** ($4 \times 4\text{px} = 16\text{px}$).
- **`px-6`**: Adds horizontal padding (**left and right** only, $24\text{px}$).
- **`py-2`**: Adds vertical padding (**top and bottom** only, $8\text{px}$).
- **`mt-4`**: Adds a top margin ($16\text{px}$) to push adjacent element containers away.

### 2. Sizing (Width & Height)

- **`w-80`**: Fixes the width to $320\text{px}$ ($80 \times 4\text{px}$).
- **`w-full`**: Makes the element stretch to match 100% of its parent wrapper width.

### 3. Typography basics

- **`text-sm` / `text-lg` / `text-2xl**`: Controls font size cleanly.
- **`font-normal` / `font-semibold` / `font-bold**`: Adjusts the font weight maps.

---

## 🛠️ Your Lesson 1 Coding Sandbox Challenge

```html
<div
  class="w-80 bg-slate-950 p-6 rounded-2xl border border-slate-800 shadow-xl"
>
  <h2 class="text-xl font-bold text-blue-400">Nabil Backend Dev</h2>

  <p class="text-xs font-mono text-slate-500 mt-1">
    Stack: Node.js & Arch Linux
  </p>

  <p class="text-sm text-slate-300 mt-4">
    Building high-performance social networking APIs and learning responsive
    frontend styling utilities.
  </p>

  <button
    class="mt-6 w-full bg-blue-600 hover:bg-blue-500 text-white font-semibold text-xs py-2.5 px-4 rounded-xl transition"
  >
    Connect Profile
  </button>
</div>
```

---
