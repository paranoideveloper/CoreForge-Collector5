# CoreForge Collector 5

**HTTPS proxies** (HTTP proxy over TLS — the connection to the proxy itself is encrypted), verified to open YouTube **from inside Iran** 🇮🇷.

## Subscription

- **Clash / Mihomo / Clash Verge / FlClash (recommended):** `https://raw.githubusercontent.com/paranoideveloper/CoreForge-Collector5/main/clash.yaml`
- **Base64:** `https://raw.githubusercontent.com/paranoideveloper/CoreForge-Collector5/main/subscription_base64.txt`
- **Plain text:** `https://raw.githubusercontent.com/paranoideveloper/CoreForge-Collector5/main/subscription_raw.txt` (one `https://ip:port?allowInsecure=1#name` per line)

Each proxy is named `<flag> CoreForge Collector 5 NNN`: the flag is the **real exit country** (measured through the proxy, not guessed from its address) and `NNN` is the speed rank (001 = fastest). These are HTTP-over-TLS proxies, so in apps that take a single proxy set type **HTTPS** (or HTTP + TLS) with the IP and port; the proxy certificates are self-signed, so certificate checking must be off.

## Latest run (2026-11-19)

| Stage | Count |
|---|---|
| HTTPS-proxy candidates scraped from public lists (GitHub + web) | 61,694 |
| Real HTTPS proxies (TLS to the proxy + CONNECT works) | 1,585 |
| Carried a speed test | 824 |
| Fastest kept for the in-country test | 500 |
| **Opened YouTube from inside Iran (2 of 2 rounds)** | **327** |

Exit countries: 🇺🇸 US ×55, 🇩🇪 DE ×43, 🇫🇷 FR ×36, 🇳🇱 NL ×30, 🇮🇳 IN ×20, 🇮🇹 IT ×16, 🇷🇴 RO ×12, 🇵🇱 PL ×10, 🇬🇧 GB ×8, 🇬🇷 GR ×8, 🇨🇿 CZ ×6, 🇭🇺 HU ×5, 🇪🇸 ES ×5, 🇭🇰 HK ×5, 🇸🇰 SK ×4, 🇦🇹 AT ×4, 🇨🇦 CA ×4, 🇨🇷 CR ×4, 🇿🇦 ZA ×4, 🇵🇹 PT ×3, 🇲🇾 MY ×3, 🇮🇩 ID ×3, 🇮🇪 IE ×2, 🇨🇭 CH ×2, 🇫🇮 FI ×2, 🇱🇹 LT ×2, 🇮🇱 IL ×2, 🇦🇲 AM ×2, 🇸🇬 SG ×2, 🇧🇼 BW ×2, 🇧🇷 BR ×2, 🇩🇰 DK ×1, 🇱🇺 LU ×1, 🇸🇪 SE ×1, 🇸🇮 SI ×1, 🇧🇬 BG ×1, 🇲🇪 ME ×1, 🇦🇱 AL ×1, 🇷🇺 RU ×1, 🇸🇦 SA ×1, 🏴 T1 ×1, 🇷🇸 RS ×1, 🇰🇿 KZ ×1, 🇹🇬 TG ×1, 🇿🇼 ZW ×1, 🇻🇳 VN ×1, 🇺🇬 UG ×1, 🇹🇹 TT ×1, 🇲🇽 MX ×1, 🇳🇦 NA ×1, 🇱🇻 LV ×1, 🇨🇱 CL ×1

## Method

1. Scrape HTTPS-proxy candidates from public GitHub lists and proxy websites.
2. Keep only **true** HTTPS proxies: a TLS handshake to the proxy, then a `CONNECT` inside that TLS session must succeed.
3. Speed-test each one (download through the proxy) and keep the fastest 500.
4. From an in-country vantage, load YouTube through each proxy twice, a minute apart; only proxies that pass both rounds are published, with their measured exit country.

These are third-party public proxies: they come and go, may log traffic, and should not be used for anything sensitive.
