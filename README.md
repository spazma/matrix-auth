# 👾 matrix-authenticator
Simple, secure, single-file TOTP authenticator.

---

# 🇬🇧 Key Features & Advantages

* **Single-file Architecture:** All code (HTML, CSS, and JavaScript) is contained within a single standalone file.
* **Client-Side Execution:** No backend server required – runs entirely in your browser. (Requires an active internet connection to load external CDN scripts for TOTP calculation and online QR code scanning).
* **Multi-Format Adding:** Add accounts manually, paste `otpauth://` URIs, or scan/upload QR codes directly via image file or live camera feed.
* **Multilingual (6 Languages):** Built-in support for 6 languages (EN, PL, DE, CS, FR, ES) with automatic browser language detection.
* **Backup & Export Options:** 
  * Full support for importing and exporting encrypted `.enc` database files.
  * Direct "Send via Email" backup option for quick off-device saving (generates/downloads a formatted email backup file on desktop or opens your mail app on mobile).
* **Matrix Visual Style:** Styled Matrix-themed user interface with full mobile responsiveness.

### Cryptographic Security Mechanisms:

* **AES-GCM (256-bit) Encryption:** All TOTP secrets are encrypted locally using the robust AES-GCM algorithm provided by the native Web Crypto API.
* **Password Protection (PBKDF2):** The encryption key is derived from the Master Password using PBKDF2 with a random salt and 100,000 iterations (SHA-256), significantly mitigating brute-force attacks.
* **Secure Local Storage:** The encrypted database is stored locally in the browser's `localStorage`. No data is ever transmitted to external servers.
* **Automatic Memory Cleanup:** Locking the application (`lockVault`) immediately clears sensitive data from JS RAM and redirects back to the authentication screen.

> ⚠️ **DURESS / FAKE PASSWORD MECHANISM:** Entering an incorrect (or fake) password twice consecutively triggers a wipe-and-switch operation: the app overwrites and replaces the real database with an empty/fake state. Once activated, your original data is permanently erased locally, and recovery is only possible by restoring from a previously created backup file.

# 🚀 Demo & Offline Usage:

### Live Demo & Offline Mode
* **Live Demo / Online Version:** [https://spazma.github.io/matrix-auth/](https://spazma.github.io/matrix-auth/)
* **Offline Usage:** If you want to use the app entirely offline (excluding the camera QR code scanning feature), simply copy the index.html file, rename it to whatever you like (e.g., matrix-auth.html), and open it locally in your browser. Feel free to authenticate securely! Good luck and greets to Wymiot from Discord :)

---

# 📜 License & Support

This project is 100% Free to Use for both personal and commercial purposes under the **MIT License**.

If you find this tool helpful, consider supporting my work:

<a href="https://buymeacoffee.com/spazma" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 50px !important;width: 217px !important;"></a>

---

## 📷 Screenshot

![MATRIX-AUTH Screenshot](https://raw.githubusercontent.com/spazma/spazma.github.io/main/screens/matrix-auth.jpg)

---

# 🇵🇱 Najważniejsze zalety i funkcja

* **Jednoplikowa architektura (Single-file):** Cały kod (HTML, CSS i JavaScript) zawarty jest w jednym, osobnym pliku.
* **Działanie po stronie klienta:** Brak wymogu serwera backendowego – aplikacja działa w pełni w przeglądarce (wymaga połączenia z siecią do pobrania skryptów CDN odpowiedzialnych za wyliczanie TOTP oraz skanowanie kodów QR online).
* **Wygodne dodawanie kont:** Możliwość dodawania ręcznego, wklejania linków `otpauth://` oraz skanowania/wczytywania kodów QR ze zdjęcia lub bezpośrednio z kamery.
* **Wielojęzyczność (6 języków):** Wbudowane wsparcie dla 6 języków (EN, PL, DE, CS, FR, ES) z automatyczną detekcją języka przeglądarki.
* **Kopie zapasowe i eksport:**
  * Tworzenie oraz przywracanie szyfrowanych kopii zapasowych bazy danych z/do pliku `.enc`.
  * Opcja szybkiej wysyłki kopii na e-mail (na telefonie automatycznie otwiera aplikację pocztową, na komputerze generuje gotowy plik wiadomości).
* **Interfejs Matrix:** Dedykowany styl wizualny w klimacie Matrixa z pełną responsywnością dla urządzeń mobilnych.

### Bezpieczeństwo i mechanizmy kryptograficzne:

* **Szyfrowanie AES-GCM (256-bit):** Wszystkie sekrety TOTP są szyfrowane lokalnie przy użyciu silnego algorytmu AES-GCM udostępnianego przez natywne API przeglądarki (Web Crypto API).
* **Ochrona hasła (PBKDF2):** Klucz szyfrujący jest generowany z Hasła Głównego przy użyciu funkcji PBKDF2 z losowością (salt) i 100 000 iteracji (SHA-256), co drastycznie utrudnia ataki typu brute-force.
* **Bezpieczny magazyn:** Zaszyfrowana baza danych jest przechowywana lokalnie w `localStorage` przeglądarki. Dane nie są wysyłane na żaden zewnętrzny serwer.
* **Automatyczne czyszczenie pamięci:** Po zablokowaniu aplikacji (`lockVault`) dane w pamięci RAM JS są natychmiast czyszczone, a aplikacja wraca do ekranu logowania.

> ⚠️ **MECHANIZM FAŁSZYWEGO HASŁA (DURESS):** Dwukrotne wpisanie błędnego (lub fałszywego) hasła powoduje przełączenie na fałszywą bazę i trwałe wyczyszczenie dotychczasowych danych. Po uaktywnieniu tego mechanizmu oryginalna baza zostaje bezpowrotnie usunięta z przeglądarki, a jedyną drogą do odzyskania dostępu jest przywrócenie danych z wcześniej utworzonej kopii zapasowej.

# 🚀 Demo & Offline:

### Wersja Demo i Praca Offline
* **Wersja Online / Demo:** [https://spazma.github.io/matrix-auth/](https://spazma.github.io/matrix-auth/)
* **Praca Offline:** Jeśli chcesz pracować w pełni offline (z wyłączeniem opcji skanowania kodów QR kamerą), po prostu skopiuj plik `index.html`, nadaj mu dowolną nazwę np.`matrix-auth.html` i otwórz go lokalnie w przeglądarce. Korzystaj i autoryzuj się śmiało! Powodzenia i pozdro dla Wymiota z Discorda :)
  
---

# 📜 License & Support

Projekt jest w 100% darmowy (Free to Use) zarówno do celów prywatnych, jak i komercyjnych na licencji **MIT**.

Jeśli kod Ci się przydał i chcesz docenić moją pracę, możesz postawić mi kawę:

<a href="https://buymeacoffee.com/spazma" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 50px !important;width: 217px !important;"></a>

---

<p align="center">
<img width="402" height="216" alt="QUnxPiMCrb0" src="https://github.com/user-attachments/assets/8d1cfcb2-cf39-4aae-9c01-5fc04a02e87d" />
<img width="402" height="273" alt="im2" src="https://github.com/user-attachments/assets/ca1ecea7-2ff0-4395-8ac7-0b0863fc693f" />
<br />
<img width="402" height="328" alt="im3" src="https://github.com/user-attachments/assets/556a4a69-b347-481c-b613-e1c0603fefb8" />
</p>




