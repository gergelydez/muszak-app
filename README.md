# ⏱ MűszakApp

Személyre szabott 12 órás műszak beosztás kezelő – PWA (telepíthető mobilra).

## 📁 Fájlok

```
muszakapp/
├── index.html      ← A teljes alkalmazás
├── manifest.json   ← PWA manifest (ikonok, appnév, téma)
├── sw.js           ← Service Worker (offline működés)
├── icon-192.png    ← App ikon (192x192)
├── icon-512.png    ← App ikon (512x512)
├── vercel.json     ← Vercel konfig
└── README.md
```

---

## 🚀 Feltöltés GitHub-ra

### 1. GitHub repo létrehozása
1. Menj a [github.com](https://github.com) oldalra → **New repository**
2. Név: `muszakapp` → **Create repository**

### 2. Fájlok feltöltése (egyszerű módszer – drag & drop)
1. A repo oldalon kattints: **uploading an existing file**
2. Húzd be az összes fájlt egyszerre:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon-192.png`
   - `icon-512.png`
   - `vercel.json`
3. Commit message: `Initial commit`
4. Kattints: **Commit changes**

### 3. Alternatíva – Git parancssorral
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/FELHASZNÁLÓNEVED/muszakapp.git
git push -u origin main
```

---

## ▲ Vercel deploy

### 1. módszer – GitHub-on keresztül (ajánlott)
1. Menj: [vercel.com](https://vercel.com) → **Sign in with GitHub**
2. Kattints: **Add New Project**
3. Importáld a `muszakapp` repót
4. Framework Preset: **Other**
5. Kattints: **Deploy** ✅

Az app pár másodperc alatt él lesz, pl: `https://muszakapp.vercel.app`

### 2. módszer – Vercel CLI
```bash
npm i -g vercel
vercel login
vercel --prod
```

---

## 📱 Telepítés mobilra (PWA)

### iPhone / iPad
1. Nyisd meg a Vercel URL-t **Safariban**
2. Alul: **Megosztás** gomb (négyzet nyíllal)
3. → **Hozzáadás a kezdőképernyőhöz**
4. Az app ikonként jelenik meg ✅

### Android
1. Nyisd meg Chrome-ban
2. Jobb felül **3 pont** → **Hozzáadás a kezdőképernyőhöz**
3. Vagy a böngésző automatikusan felajánlja ✅

---

## 🔧 Műszak ciklus logika

| Nap | Típus |
|-----|-------|
| 0–3 | ☀️ Nappal (06:00–18:00) |
| 4–7 | ✨ Szabad |
| 8–11 | 🌙 Éjszaka (18:00–06:00) |
| 12–15 | ✨ Szabad |

Referencia dátum: **2026. április 27.** = ciklus 1. napja
