# Secure Password Split

> **A Single-File, Offline-First Progressive Web Application (PWA) for Cryptographic Secret Sharing.**

---

## 🚨 Security Warning

**THIS TOOL IS DESIGNED TO BE RUN LOCALLY AND OFFLINE.**

While this application can be hosted on a static server (like GitHub Pages), for **maximum security**, it is highly recommended to:

1.  Download the `SPSS.html` file (`index.html` in the repo).
2.  **Disconnect your device from the internet.**
3.  Run the file locally in a trusted browser.
4.  Close the browser window before reconnecting to the network.

---

## 📖 Overview

**Secure Password Split** is a client-side utility that allows you to split sensitive secrets (passwords, seed phrases, private keys) into multiple shares using information-theory cryptographic security methods. It operates entirely in the browser with **zero server-side transmission**.

It supports two splitting modes:

* **N-of-N (XOR):** All generated shares are required to reconstruct the secret.
* **K-of-N (Threshold Cryptography):** Uses Shamir's Secret Sharing (over GF(256)). A subset (K) of the total shares (N) is required to reconstruct the secret.

---

## ✨ Features

### Cryptography
* **CSPRNG:** Uses `window.crypto.getRandomValues` for all random number generation.
* **Transport Agnostic:** Shares are encoded in Hexadecimal, making them safe to transport via any medium (paper, email, text) regardless of the secret's original character set.
* **Sanitized Reconstruction:** Automatically handles case sensitivity and whitespace cleaning during reconstruction.

### Application Architecture
* **Single File Interface (SFI):** The entire app (HTML, CSS, JS, SVG Assets, PWA Manifest, Service Worker) is contained in one `.html` file.
* **Recursive Quine Download:** The application can download its own source code directly from memory, ensuring the offline copy is an exact replica of the running instance.
* **PWA Support:** Fully installable on iOS, Android, and Desktop (Chrome/Edge). Includes an embedded Service Worker for offline caching.

### UI/UX
* **Secure Inputs:** `autocomplete="off"` and anti-password-manager attributes (`data-lpignore`) to prevent unauthorized caching.
* **Visual Hashing:** "Hold to Reveal" functionality with syntax highlighting (**Red** for digits, **Green** for symbols) to aid in manual transcription verification.
* **Dark/Light Mode:** Auto-detection with manual override.
* **Generator:** Built-in secure password generator with configurable complexity (Symbols, Case, Numbers).

---

## 🚀 Usage

### Online
1.  Visit the [hosted URL](https://kaerez.github.io/Secure-Password-Split/).

### Offline (Recommended)
1.  Click the **HERE** link in the top yellow banner to download the `SPSS.html`.
2.  Open the file in your preferred browser.

### To Split
1.  Enter your secret.
2.  Select **Split** or **Threshold Split**.
3.  Adjust the sliders/inputs for the number of shares (N) and threshold (K).
4.  Click **SPLIT**.
5.  Copy the resulting Hex strings.

### To Reconstruct
1.  Go to the **Reconstruct** tab.
2.  Paste your Hex shares.
3.  If using Shamir shares, toggle **"Use Threshold Mode"** to **ON**.
4.  Click **RECONSTRUCT**.

---

## ⚖️ Liability Disclaimer

> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
>
> IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
>
> **YOU USE THIS APPLICATION AT YOUR OWN RISK.** The author accepts no responsibility for lost data, lost passwords, or security breaches resulting from the use or misuse of this software. It is the user's responsibility to ensure the security of the environment in which this tool is executed.

---

## 📄 License

**Author:** Erez Kalman - KSEC

This project is licensed under a custom **Personal Non-Commercial Use License**:

* Free for personal, private, non-commercial use only.
* Code can be reused under these same terms, provided that:
    1.  The software remains open source and freely available.
    2.  Commercial ownership and rights are retained exclusively by the author (Erez Kalman - KSEC).
    3.  Any commercial use, redistribution for profit, or inclusion in proprietary commercial software is strictly prohibited without prior written consent from the author.

*Built with ❤️ and Paranoia.*
