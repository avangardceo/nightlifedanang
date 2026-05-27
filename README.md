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

## 📨 Attivare il form (ricevere le richieste via email)
Il form "Request Your Night" è già collegato a **Web3Forms** (gratuito).
Per ricevere i risultati nella tua casella email:

1. Vai su **https://web3forms.com**
2. Inserisci la tua email reale → ricevi una **Access Key** (gratis, 1 minuto)
3. In `index.html`, nel blocco `CONFIG`, sostituisci:
   `web3forms_key: "INSERISCI-LA-TUA-ACCESS-KEY-QUI",` con la chiave ricevuta.
4. Fatto! Ogni richiesta dal form ti arriverà via email con tutti i dettagli
   (nome, data, gruppo, tipo di serata, canale preferito, contatto, lingua).

> Piano gratuito: 250 invii/mese. Se in futuro vorrai una dashboard vera (tabella
> con stato e filtri), si potrà migrare senza rifare il sito.

---

## 🌍 Farsi trovare su Google, Naver, Yandex, Baidu, Bing

Il sito è già predisposto per tutti i principali motori (meta-tag robots, sitemap,
hreflang per le 6 lingue). Per indicizzarti attivamente, registra il sito su ciascuna
console (gratis) e inserisci il codice di verifica nei meta-tag dell'`<head>` di `index.html`:

- **Google** → https://search.google.com/search-console
- **Naver** (Corea) → https://searchadvisor.naver.com → codice in `naver-site-verification`
- **Yandex** (Russia) → https://webmaster.yandex.com → codice in `yandex-verification`
- **Baidu** (Cina) → https://ziyuan.baidu.com → codice in `baidu-site-verification`
- **Bing** → https://www.bing.com/webmasters → codice in `msvalidate.01`

In ogni console, dopo la verifica, invia il sitemap: `https://nightlifeindanang.com/sitemap.xml`

---

## Caratteristiche

- **6 lingue**: Inglese, Vietnamita, Coreano, Giapponese, Cinese, Russo
  (rilevamento automatico della lingua del browser, fallback su Inglese)
- **Video hero** a tutta altezza (muto, in loop)
- **6 canali di contatto**: WhatsApp, Telegram (QR), KakaoTalk (QR), LINE (QR), WeChat (QR), Email
- **Form di richiesta** collegato a Web3Forms (richieste via email)
- **Gallery** con foto reali dei locali partner
- **Recensioni** multilingua + trust badge
- Completamente **responsive** (desktop, tablet, mobile)
- **SEO** ottimizzato (meta tag, hreflang, JSON-LD Schema.org)

---

## Note tecniche

- Sito statico: nessun server richiesto, gira ovunque (GitHub Pages, Netlify, hosting classico).
- Nessuna dipendenza esterna se non i Google Fonts e Web3Forms (entrambi via CDN/API).
- Il form invia le richieste via Web3Forms; se l'utente sceglie WhatsApp come canale,
  apre anche la chat col riepilogo precompilato.

---

© Ai Partners Web — per Nightlife in Da Nang
