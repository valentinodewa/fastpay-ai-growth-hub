# Fastpay AI Growth Hub — GitHub Pages

Paket ini menggunakan URL bawaan GitHub Pages, tanpa custom domain dan tanpa file CNAME.

## File yang diunggah ke root repository
- index.html
- config.js
- .nojekyll

## Sebelum upload
Edit config.js dan isi URL Web App Google Apps Script yang berakhiran /exec:

```js
window.FASTPAY_CONFIG = Object.freeze({
  API_URL: 'https://script.google.com/macros/s/DEPLOYMENT_ID/exec'
});
```

Jangan menaruh password, SESSION_SECRET, Gemini API key, atau Telegram token di repository.

## Pilihan URL
### Project site
Nama repository bebas, contoh `fastpay-ai-growth-hub`.
URL:
`https://USERNAME.github.io/fastpay-ai-growth-hub/`

### User/organization site
Nama repository harus persis `USERNAME.github.io`.
URL:
`https://USERNAME.github.io/`

## Aktifkan GitHub Pages
Repository → Settings → Pages:
- Source: Deploy from a branch
- Branch: main
- Folder: /(root)
- Save

## Acceptance test
1. Buka URL GitHub Pages di jendela incognito.
2. Login memakai email aktif pada Sheet Members.
3. Buat satu worklog uji.
4. Pastikan data masuk ke Sheet CheckIn.
5. Logout dan login kembali.
6. Pastikan endpoint getAll tanpa token ditolak.
