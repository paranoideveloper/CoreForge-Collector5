# CoreForge Collector 5

**HTTPS proxies** (HTTP proxy over TLS — the connection to the proxy itself is encrypted), verified to open YouTube **from inside Iran** 🇮🇷.

## Subscription

- **Clash / Mihomo / Clash Verge / FlClash (recommended):** `https://raw.githubusercontent.com/paranoideveloper/CoreForge-Collector5/main/clash.yaml`
- **Base64:** `https://raw.githubusercontent.com/paranoideveloper/CoreForge-Collector5/main/subscription_base64.txt`
- **Plain text:** `https://raw.githubusercontent.com/paranoideveloper/CoreForge-Collector5/main/subscription_raw.txt` (one `https://ip:port` per line)

Each proxy is named `<flag> CoreForge Collector 5 NNN`: the flag is the **real exit country** (measured through the proxy, not guessed from its address) and `NNN` is the speed rank (001 = fastest). These are HTTP-over-TLS proxies, so in apps that take a single proxy set type **HTTPS** (or HTTP + TLS) with the IP and port; the proxy certificates are self-signed, so certificate checking must be off.

## Latest run (2026-11-13)

| Stage | Count |
|---|---|
| HTTPS-proxy candidates scraped from public lists (GitHub + web) | 61,692 |
| Real HTTPS proxies (TLS to the proxy + CONNECT works) | 1,614 |
| Carried a speed test | 858 |
| Fastest kept for the in-country test | 500 |
| **Opened YouTube from inside Iran (2 of 2 rounds)** | **307** |

Exit countries: 🇩🇪 DE ×64, 🇺🇸 US ×50, 🇫🇷 FR ×29, 🇳🇱 NL ×27, 🇮🇳 IN ×17, 🇮🇹 IT ×13, 🇷🇴 RO ×8, 🇬🇷 GR ×8, 🇬🇧 GB ×7, 🇵🇱 PL ×7, 🇨🇿 CZ ×6, 🇭🇺 HU ×5, 🇪🇸 ES ×5, 🇭🇰 HK ×5, 🇸🇰 SK ×4, 🇦🇹 AT ×4, 🇨🇷 CR ×4, 🇮🇪 IE ×3, 🇵🇹 PT ×3, 🇨🇭 CH ×3, 🇿🇦 ZA ×3, 🇲🇾 MY ×3, 🇱🇹 LT ×2, 🇸🇦 SA ×2, 🇮🇱 IL ×2, 🇦🇲 AM ×2, 🇨🇦 CA ×2, 🇧🇼 BW ×2, 🇩🇰 DK ×1, 🇸🇪 SE ×1, 🇸🇮 SI ×1, 🇫🇮 FI ×1, 🇷🇺 RU ×1, 🇦🇱 AL ×1, 🇷🇸 RS ×1, 🇧🇬 BG ×1, 🇲🇪 ME ×1, 🇰🇿 KZ ×1, 🇹🇬 TG ×1, 🇸🇬 SG ×1, 🇿🇼 ZW ×1, 🇮🇩 ID ×1, 🇺🇬 UG ×1, 🇻🇳 VN ×1, 🇳🇦 NA ×1

## Method

1. Scrape HTTPS-proxy candidates from public GitHub lists and proxy websites.
2. Keep only **true** HTTPS proxies: a TLS handshake to the proxy, then a `CONNECT` inside that TLS session must succeed.
3. Speed-test each one (download through the proxy) and keep the fastest 500.
4. From an in-country vantage, load YouTube through each proxy twice, a minute apart; only proxies that pass both rounds are published, with their measured exit country.

These are third-party public proxies: they come and go, may log traffic, and should not be used for anything sensitive.
