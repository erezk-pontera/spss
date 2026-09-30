# Secure Password Split

> **A Single-File, Offline-First Web Application for Threshold Secret Sharing (Shamir's Secret Sharing).**

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

**Secure Password Split** is a client-side utility that allows you to split sensitive secrets (passwords, seed phrases, private keys) into multiple shares using information-theoretically secure secret sharing. It operates entirely in the browser with **zero server-side transmission**.

It uses a single splitting mode:

* **K-of-N (Threshold):** Shamir's Secret Sharing over GF(256). The secret is split into **N** shares, and any **K** of them (2 ≤ K ≤ N ≤ 255) are sufficient to reconstruct it. Fewer than K shares reveal nothing about the secret's content.

> **Tip:** For an "all shares required" split, set **K = N**.

> ⚠️ **Legacy N-of-N (XOR) shares are no longer supported.** Earlier versions offered a separate XOR "Split" mode. That mode has been removed, and the Reconstruct tab now always uses threshold (Shamir) reconstruction. If you hold XOR shares created by an older version, keep a copy of that older version to reconstruct them.

---

## ✨ Features

### Cryptography
* **CSPRNG:** Uses `window.crypto.getRandomValues` for all random number generation (with rejection sampling to avoid modulo bias).
* **Parameter Enforcement:** Splitting is refused unless `2 ≤ K ≤ N ≤ 255`, preventing degenerate splits (e.g., K = 1, where every share would contain the secret in plain form).
* **Transport Agnostic:** Shares are encoded in Hexadecimal, making them safe to transport via any medium (paper, email, text) regardless of the secret's original character set (UTF-8 supported).
* **Sanitized Reconstruction:** Share inputs automatically strip non-hex characters (e.g., whitespace) and normalize case.
* **Reconstruction Checks:** Detects mismatched share lengths, duplicate shares, invalid share IDs, and results that are not valid text.

### Application Architecture
* **Single File Interface (SFI):** The entire app (HTML, CSS, JS, SVG assets, Web App Manifest) is contained in one `.html` file.
* **Recursive Quine Download:** The application can download its own source code. The copy is a snapshot taken at page load, so it **never includes secrets or shares** entered or generated during the session.
* **Installable (best-effort):** An embedded Web App Manifest and install guidance are provided for iOS, Android, and Desktop. Offline use is achieved by running the downloaded `SPSS.html` file directly; no offline cache is provided (see *Known Limitations*).

### UI/UX
* **Secure Inputs:** `autocomplete="off"` and anti-password-manager attributes (`data-lpignore`, `data-1p-ignore`) to discourage unauthorized caching.
* **Visual Hashing:** "Hold to Reveal" functionality with syntax highlighting (**Red** for digits, **Green** for symbols) to aid in manual transcription verification. Releasing the button, or moving the pointer away, hides the value again.
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
1.  On the **Threshold Split** tab, enter your secret (or generate one).
2.  Set **Total Shares (N)** and **Required Shares (K)** using the sliders or number inputs.
3.  Click **SPLIT**.
4.  Copy the resulting Hex strings. Each share is labelled with its K-of-N parameters. **Record K along with the shares**, as the shares themselves do not state how many are required.

### To Reconstruct
1.  Go to the **Reconstruct** tab.
2.  Paste **at least K** Hex shares (use **Add Share Row** for more than two). Order does not matter.
3.  Click **RECONSTRUCT SECRET**.

---

## 🧩 Share Format

Each share is a hex string: the first byte is the share ID (`01`–`FF`, the x-coordinate) and the remaining bytes are the share's y-values, one per byte of the UTF-8 encoded secret.

---

## ⚠️ Known Limitations

* **No integrity check:** Shares carry no checksum or authentication tag. Supplying fewer than K shares, or a mistyped share, usually produces an error, but may occasionally produce incorrect text without warning. Verify the recovered secret before relying on it.
* **Length is visible:** Share length reveals the byte length of the secret. Pad short secrets if their length is sensitive.
* **No offline cache:** The app does not use a Service Worker, so the hosted version is not cached for offline use. Use the downloaded file for offline operation.
* **Clipboard:** Copied shares and secrets remain on the system clipboard (and in any clipboard history) until overwritten. Clear it after use.

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
