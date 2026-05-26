# Nightlife in Da Nang — Sito Web

Sito vetrina multilingua per servizi di nightlife a Da Nang (Vietnam): karaoke VIP,
bottle service, cene, eventi aziendali e transfer, per turisti e clienti business.

Realizzato da **Ai Partners Web**.

---

## Struttura del progetto

```
nightlife-danang/
├── index.html          ← il sito completo (HTML + CSS + JS in un unico file)
├── README.md           ← questo file
├── sitemap.xml         ← mappa del sito per i motori di ricerca
├── robots.txt          ← istruzioni per i crawler
├── .gitignore
└── media/
    ├── favicon.svg          ← icona del sito (scheda browser)
    ├── hero-vip.mp4         ← video hero (sala VIP, senza audio)
    ├── hero-vip.webm        ← video hero (formato alternativo)
    ├── hero-vip-poster.jpg  ← immagine di anteprima del video
    ├── kakao-qr.png         ← QR code KakaoTalk
    ├── gallery-sala-gold-1.jpg
    ├── gallery-sala-gold-2.jpg
    ├── gallery-corridoio.jpg
    ├── gallery-sala-neon.jpg
    └── gallery-skyline.jpg
```

> ⚠️ **Importante:** `index.html` e la cartella `media/` devono restare sempre
> insieme. Il sito carica video e immagini da `media/`.

---

## Come pubblicarlo su GitHub Pages (gratis)

1. Crea un nuovo repository su GitHub (es. `nightlife-danang`).
2. Carica **tutti** i file di questa cartella mantenendo la struttura
   (puoi trascinarli nella pagina del repo, oppure usare `git push`).
3. Vai su **Settings → Pages**.
4. In "Source" seleziona il branch `main` e la cartella `/ (root)`.
5. Salva. Dopo 1-2 minuti il sito sarà online all'indirizzo:
   `https://<tuo-username>.github.io/nightlife-danang/`

### Collegare il dominio NightlifeinDaNang.com
- In **Settings → Pages → Custom domain** inserisci `nightlifeindanang.com`.
- Dal pannello del tuo provider del dominio, imposta i record DNS verso GitHub Pages
  (GitHub fornisce le istruzioni esatte in quella schermata).

---

## ⚙️ Personalizzazione — DA FARE PRIMA DEL LANCIO

Apri `index.html` e cerca il blocco `CONFIG` (vicino alla fine, nello `<script>`).
Inserisci i dati reali:

```js
const CONFIG = {
  whatsapp: "84396677534",   // ✅ già impostato
  telegram: "84396677534",   // meglio uno username Telegram (es. "nightlifedanang")
  kakao:    "",              // gestito via QR (media/kakao-qr.png)
  line:     "",              // inserire ID/codice LINE per il link diretto
  wechat:   "84396677534",   // inserire ID WeChat per funzionare al 100%
  phone:    "84396677534",
  email:    "hello@nightlifeindanang.com",  // ← inserire email reale
};
```

Cerca poi i commenti `TODO` nel file per gli altri segnaposti:
- **Telefono** nel footer
- **Recensioni**: quelle attuali sono DIMOSTRATIVE → sostituire con recensioni reali
  dei clienti prima di pubblicare (cerca il commento `TODO: sostituire con recensioni reali`)

---

## Caratteristiche

- **5 lingue**: Inglese, Vietnamita, Coreano, Giapponese, Cinese
  (rilevamento automatico della lingua del browser, fallback su Inglese)
- **Video hero** a tutta altezza (muto, in loop)
- **6 canali di contatto**: WhatsApp, Telegram, KakaoTalk (QR), LINE, WeChat, Email
- **Form di richiesta** intelligente (predisposto per una futura dashboard)
- **Gallery** con foto reali dei locali partner
- **Recensioni** multilingua + trust badge
- Completamente **responsive** (desktop, tablet, mobile)
- **SEO** ottimizzato (meta tag, hreflang, JSON-LD Schema.org)

---

## Note tecniche

- Sito statico: nessun server richiesto, gira ovunque (GitHub Pages, Netlify, hosting classico).
- Nessuna dipendenza esterna se non i Google Fonts (caricati via CDN).
- Il form, allo stato attuale, mostra una conferma e (se l'utente sceglie WhatsApp)
  apre la chat con il riepilogo. Per raccogliere le richieste in una dashboard,
  collegare un backend nel punto segnato `TODO BACKEND` nel codice.

---

© Ai Partners Web — per Nightlife in Da Nang
