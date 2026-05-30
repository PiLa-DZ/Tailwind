# 🧭 The Core Concept: The Flex Container & Axes

By default, HTML elements stack vertically on top of each other.
The moment you add the utility class `flex` to a parent container,
its direct children instantly align horizontally in a row.

Flexbox operates along two directions:

1. **Main Axis:** The primary direction items flow (default is left-to-right).
2. **Cross Axis:** The perpendicular direction (default is top-to-bottom).

---

## 📊 Your Essential Flexbox Utility Cheat Sheet

Here are the exact basic tools you will need to organize any UI layout.

### 1. The Direction Switcher (`flex-row` vs `flex-col`)

Controls the layout orientation of the items.

- **`flex-row`** _(Default)_: Places children horizontally side-by-side (e.g., navigation links, a row of profile badges).
- **`flex-col`**: Stacks children vertically (e.g., a form input list, a timeline layout).

### 2. Main Axis Alignment (`justify-`)

Aligns elements horizontally when using `flex-row`, or vertically when using `flex-col`.

- **`justify-start`**: Flushes everything to the beginning.
- **`justify-end`**: Pushes everything to the very end.
- **`justify-center`**: Bunches everything perfectly in the middle.
- **`justify-between`**: Separates elements evenly, pushing the first item to the left wall and the last item to the right wall (perfect for navigation bars).

### 3. Cross Axis Alignment (`items-`)

Aligns elements vertically when using `flex-row`, or horizontally when using `flex-col`.

- **`items-start`**: Aligns items to the top edge.
- **`items-end`**: Aligns items to the bottom edge.
- **`items-center`**: Centers items perfectly along the cross axis (crucial for aligning different-sized icons next to text).

### 4. Spacing Between Items (`gap-`)

Instead of adding margins to every individual child, you can tell the parent container to automatically inject spacing between all its children.

- **`gap-2`**: Adds $8\text{px}$ of space between every item.
- **`gap-4`**: Adds $16\text{px}$ of space between every item.

---

## 🛠️ Lesson 2 Coding Sandbox Challenge

Let's put this into practice using your `live-server` setup. Open `public/index.html` in Neovim, and replace your code inside the `<body>` with this practical navbar and layout card row:

```html
<div
  class="w-full max-w-4xl bg-slate-950 p-6 rounded-2xl border border-slate-800 shadow-2xl flex flex-col gap-6"
>
  <nav
    class="flex justify-between items-center bg-slate-900 p-4 rounded-xl border border-slate-800"
  >
    <h1 class="text-lg font-bold text-blue-400 font-mono">Facechat App</h1>

    <div class="flex gap-3">
      <button
        class="text-xs font-semibold text-slate-300 hover:text-white px-3 py-1.5 transition"
      >
        Feed
      </button>
      <button
        class="bg-blue-600 hover:bg-blue-500 text-white text-xs font-bold px-4 py-1.5 rounded-lg transition"
      >
        Logout
      </button>
    </div>
  </nav>

  <div class="flex flex-row gap-4">
    <div
      class="flex-1 bg-slate-900 p-4 rounded-xl border border-slate-800/60 flex flex-col gap-2"
    >
      <span
        class="text-[10px] uppercase font-mono text-emerald-400 bg-emerald-500/10 px-2 py-0.5 rounded w-max"
        >Online</span
      >
      <h3 class="font-bold text-slate-200">Nabil</h3>
      <p class="text-xs text-slate-400">
        Arch Linux Developer environment configured.
      </p>
    </div>

    <div
      class="flex-1 bg-slate-900 p-4 rounded-xl border border-slate-800/60 flex flex-col gap-2"
    >
      <span
        class="text-[10px] uppercase font-mono text-slate-500 bg-slate-800 px-2 py-0.5 rounded w-max"
        >Offline</span
      >
      <h3 class="font-bold text-slate-200">Amin</h3>
      <p class="text-xs text-slate-400">
        Waiting for graph request synchronization channels.
      </p>
    </div>
  </div>
</div>
```

---

## 🧪 Experiment Time

Save the file (`:w` in Neovim) and watch your browser update immediately.

To feel how the main/cross axes work, try editing the `<nav>` component class string:

1. Change **`justify-between`** to **`justify-center`**. What happens to the title and buttons?
2. Change it to **`justify-end`**. Where does the content drift?

Once you see how the elements adjust, let me know, and we'll unlock **Lesson 3: Sizing limits (`flex-1`, `w-full`) and Hover State Interactions**!
