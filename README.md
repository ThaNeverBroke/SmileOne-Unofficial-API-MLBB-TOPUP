# ⚡ SmileOne Unofficial API ⚡

![License](https://img.shields.io/badge/License-GPL--3.0-blue)
![Success Rate](https://img.shields.io/badge/Success_Rate-99%25-brightgreen)
![Status](https://img.shields.io/badge/Status-Active-success)

**Unofficial API for SmileOne Top-up Store** powered by **CamRapidSecure**

Fast, reliable, stable and easy-to-use API for topping up Mobile Legends and many other games via SmileOne. This API allows you to send top-up orders quickly using only a GET request with query parameters. No complicated authentication or headers needed — just your SmileOne PHPSEED cookie.

---

## 🌐 Official Links

| | Link |
|---|---|
| 🌍 **Website** | [camrapidsecure.com](https://camrapidsecure.com/) |
| 📢 **Telegram Channel** | [t.me/That_my_Bio](https://t.me/That_my_Bio) |
| 💬 **Telegram Contact** | [t.me/THANEVERBROKK](https://t.me/THANEVERBROKK) |

---

## ℹ️ About This API

This unofficial API serves as a bridge between your application and SmileOne's top-up system. It eliminates the need to constantly interact with SmileOne's web interface. Simply create a SmileOne account, retrieve your PHPSEED cookie once, and you can instantly process top-up orders for **Mobile Legends: Bang Bang** and other supported games.

**Supported Regions:** SmileOne supports all countries including:
- 🇧🇷 **Brazil (BR)** - Full support for Brazilian servers
- 🇵🇭 **Philippines (PH)** - Full support for Philippine servers  
- 🇮🇩 **Indonesia (ID)**
- 🇲🇾 **Malaysia (MY)**
- 🇸🇬 **Singapore (SG)**
- 🇹🇭 **Thailand (TH)**
- 🇹🇼 **Taiwan (TW)**
- 🌎 **And many more countries worldwide**

Whether your MLBB account is in Brazil, Philippines, or any other region, this API will detect the correct region and process your top-up accordingly.

---

## 🔑 How to Use (Very Simple)

| Step | Action |
|------|--------|
| 1️⃣ | Login to your **[SmileOne Account](https://www.smile.one/)** |
| 2️⃣ | Copy the **`PHPSEED`** cookie value from your browser |
| 3️⃣ | Use it in the API URL as `PHPSEED=your_php_seed` |
| 4️⃣ | **Ready!** Just send a simple GET request. |

---

## 📡 Main API Endpoint

```http
GET https://api.camrapidsecure.com/api_partner/ML_SmileOne_Unofficial.php?userid=262856740&zoneid=3543&package=11MLBB&PHPSEED=YOUR_PHPSEED
