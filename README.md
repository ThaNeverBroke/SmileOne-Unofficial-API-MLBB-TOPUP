# ⚡ SmileOne Unofficial API ⚡

![License](https://img.shields.io/badge/License-GPL--3.0-blue)
![Success Rate](https://img.shields.io/badge/Success_Rate-99%25-brightgreen)
![API Status](https://img.shields.io/badge/API-Online-success)
![Mobile Legends](https://img.shields.io/badge/Mobile_Legends-Supported-orange)

<h1 align="center">SmileOne Unofficial API</h1>

<p align="center"><strong>Unofficial API for SmileOne Top-up Store</strong> powered by <strong>CamRapidSecure</strong></p>

<p align="center">⚡ Fast • 🔒 Reliable • 📱 Easy-to-use API for topping up <strong>Mobile Legends</strong> and many other games</p>

---

## 💡 What Makes This API Special?

**No need to constantly request SmileOne!** Just create a SmileOne account once, login to get your cookie, and you're ready to use this API for **instant Mobile Legends recharges/top-ups**.

> ✅ **One-time setup** - Get cookie once, use it forever  
> ✅ **Instant processing** - No waiting, no manual approval  
> ✅ **Direct top-up** - Bypass SmileOne interface completely  
> ✅ **99% success rate** - Reliable and tested

---

## 🌐 Official Links

<table align="center">
  <tr>
    <td align="center">
      <a href="https://camrapidsecure.com/">
        <img src="https://img.icons8.com/color/48/000000/domain.png" width="32"><br>
        <b>Website</b>
      </a>
    </td>
    <td align="center">
      <a href="https://t.me/Cion">
        <img src="https://img.icons8.com/color/48/000000/telegram-app.png" width="32"><br>
        <b>Telegram Channel</b>
      </a>
    </td>
    <td align="center">
      <a href="https://t.me/NightStrang6r">
        <img src="https://img.icons8.com/color/48/000000/telegram-app--v1.png" width="32"><br>
        <b>Telegram Contact</b>
      </a>
    </td>
  </tr>
</table>

- 🌐 **Website**: [camrapidsecure.com](https://camrapidsecure.com/)
- 📢 **Telegram Channel**: [t.me/Cion](https://t.me/Cion)
- 👤 **Telegram Contact**: [t.me/NightStrang6r](https://t.me/NightStrang6r)

---

## 🔑 How to Use (Very Simple)

| Step | Action |
|------|--------|
| 1️⃣ | Login to your **[SmileOne Account](https://www.smile.one/)** |
| 2️⃣ | Copy the **`PHPSEED`** cookie value from browser dev tools |
| 3️⃣ | Use it in the API URL as `PHPSEED=your_php_seed` |
| 4️⃣ | **Ready!** Just send a simple GET request |

---

## 📡 Main API Endpoint

```http
GET https://api.camrapidsecure.com/api_partner/ML_SmileOne_Unofficial.php
  ?userid=262856740
  &zoneid=3543
  &package=11MLBB
  &PHPSEED=YOUR_PHPSEED
