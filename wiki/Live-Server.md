# 🛠️ Step 1: Install Browser-Sync

```bash
npm install -D browser-sync

```

---

## ⚙️ Step 2: Update Your `package.json` Scripts

### FILE: `./package.json`

```json
  "scripts": {
    "start": "node ./src/server.js",
    "dev": "browser-sync start --proxy 'localhost:3000' --files 'public/**/*' & node --watch ./src/server.js"
  }

```

### What this script does

- **`--proxy 'localhost:3000'`**: Tells browser-sync to wrap around your Express server.
- **`--files 'public//*'`**: Tells it to watch every single file inside your `public` folder (HTML, CSS, JS).
- **`& node --watch ...`**: Runs both the proxy watcher and your backend server simultaneously in the background.

---

## 🚀 Step 3: Run the Development Server

Now, run your dev command like normal:

```bash
npm run dev

```

### 🎈 Look what happens

1. Your terminal will start your Express server on port `3000`.
2. Browser-sync will initialize and automatically open a new browser tab at **`http://localhost:3001`**.

> ⚠️ **Important:** Always use **port 3001** in your browser while developing. Port 3001 is the special browser-sync link that injects the live-reloading script.

---

## 🧪 Let's Test It

Keep your browser open on `http://localhost:3001` side-by-side with Neovim.

Open `public/index.html` and look for the outer card `<div>`. Add the utility class **`text-center`** right into the class list:

```html
<div
  class="w-80 bg-slate-950 p-6 rounded-2xl border border-slate-800 shadow-xl text-center"
></div>
```

Hit save (`:w` in Neovim). Look at your browser—the whole card's text will immediately jump to the center without you ever touching `F5` or hitting a reload button!

Once this live-reload wrapper is working perfectly on your screen, let me know, and we will jump straight into **Lesson 2: Spacing & The Boxing Layout Core**!
