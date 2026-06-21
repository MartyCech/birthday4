# 🦕 Pozvánka — 4. narozeniny Kikouše Čecha

Jednoduchá statická stránka (pozvánka + registrační formulář) pro GitHub Pages.
Registrace chodí přes **Formspree**, kde je uvidíš online po přihlášení.

## Soubory
- `index.html` — pozvánka a formulář
- `styles.css` — dinosauří styl
- `kikous.png` — fotka

---

## 1) Nastavení formuláře (Formspree)

GitHub Pages umí jen statické stránky, proto sběr odpovědí zajišťuje Formspree (zdarma).

1. Jdi na **https://formspree.io** a zaregistruj se (stačí e-mail / GitHub).
2. Vytvoř nový formulář („New form"), pojmenuj ho např. `Narozeniny Kikouš`.
3. Formspree ti dá adresu ve tvaru `https://formspree.io/f/abcdwxyz`.
   Část za `/f/` (např. `abcdwxyz`) je tvoje **Form ID**.
4. V souboru `index.html` najdi řádek:
   ```html
   action="https://formspree.io/f/YOUR_FORM_ID"
   ```
   a nahraď `YOUR_FORM_ID` svým ID. Výsledek např.:
   ```html
   action="https://formspree.io/f/abcdwxyz"
   ```
5. Hotovo. Po prvním odeslání formuláře přijde na tvůj e-mail potvrzení Formspree — klikni na ověřovací odkaz.

### Kde uvidíš registrace
Přihlas se na **https://formspree.io** → otevři svůj formulář → **Submissions**.
Tam je seznam všech odpovědí (účast ANO/NE + jméno dítěte). Lze i exportovat do CSV.

---

## 2) Nasazení na GitHub Pages

1. Vytvoř na GitHubu nový **veřejný** repozitář, např. `narozeniny-kikous`.
2. Nahraj do něj soubory `index.html`, `styles.css`, `kikous.png` (a `README.md`).

   Přes terminál:
   ```bash
   cd /Users/mcech1/Documents/Projects/birthday4
   git init
   git add .
   git commit -m "Pozvánka na narozeniny"
   git branch -M main
   git remote add origin https://github.com/TVOJE_JMENO/narozeniny-kikous.git
   git push -u origin main
   ```
3. V repozitáři jdi na **Settings → Pages**.
4. U „Build and deployment" vyber **Source: Deploy from a branch**,
   branch **main** a složku **/ (root)**. Ulož.
5. Za chvíli bude web na adrese:
   ```
   https://TVOJE_JMENO.github.io/narozeniny-kikous/
   ```

---

## 3) QR kód

Z výsledné adresy (bod 2.5) vygeneruj QR kód, např. na
**https://www.qr-code-generator.com** nebo `https://www.qrcode-monkey.com`.
QR vytiskni na pozvánky — po naskenování se otevře tato stránka.

---

## Co stránka obsahuje
- Nadpis **4. narozeniny Kikouše Čecha** + fotka
- Text: *Moc se na vás těším. Dejte mi vědět, jestli dorazíte.*
- Formulář: **Oslavy se zúčastním: ANO / NE** + **Jméno dítěte**
- Poznámka o vstupném (Dinolive, 200 Kč pro dospělé)
- Odkaz na **https://dinolive.cz/** a tlačítko do mapy (GPS 50.097267, 14.333780)
