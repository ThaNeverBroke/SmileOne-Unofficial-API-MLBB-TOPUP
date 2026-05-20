⚡ SmileOne Unofficial API ⚡
=============================

[![License](https://img.shields.io/badge/License-GPL--3.0-blue)](https://img.shields.io/badge/License-GPL--3.0-blue)
[![Success Rate](https://img.shields.io/badge/Success_Rate-99%25-brightgreen)](https://img.shields.io/badge/Success_Rate-99%25-brightgreen)

**Unofficial API for SmileOne Top-up Store** powered by **CamRapidSecure**

Fast, reliable and easy-to-use API for topping up **Mobile Legends** and many other games.

-------------------------------------------------------------------------------

What Makes This API Special?
----------------------------

**No need to constantly request SmileOne!** Just create a SmileOne account once, 
login to get your cookie, and you're ready to use this API for **instant Mobile 
Legends recharges/top-ups**.

  [✓] One-time setup - Get cookie once, use it forever
  [✓] Instant processing - No waiting, no manual approval  
  [✓] Direct top-up - Bypass SmileOne interface completely
  [✓] 99% success rate - Reliable and tested

-------------------------------------------------------------------------------

Official Links
--------------

  Website         : https://camrapidsecure.com/
  Telegram Channel: https://t.me/Cion
  Telegram Contact: https://t.me/NightStrang6r

-------------------------------------------------------------------------------

How to Use (Very Simple)
------------------------

  1. Login to your SmileOne Account (https://www.smile.one/)
  2. Copy the PHPSEED cookie value from browser dev tools
  3. Use it in the API URL as PHPSEED=your_php_seed
  4. Ready! Just send a simple GET request.

-------------------------------------------------------------------------------

Main API Endpoint
-----------------

  GET https://api.camrapidsecure.com/api_partner/ML_SmileOne_Unofficial.php?userid=262856740&zoneid=3543&package=11MLBB&PHPSEED=YOUR_PHPSEED

Parameters:

  userid   : Mobile Legends Player ID (example: 262856740)
  zoneid   : Mobile Legends Zone ID (example: 3543)
  package  : Package code (11MLBB, 22MLBB, 50MLBB, etc.)
  PHPSEED  : Your SmileOne cookie value

-------------------------------------------------------------------------------

Code Examples
-------------

PYTHON:

  import requests

  PHPSEED = "YOUR_PHPSEED_HERE"

  url = "https://api.camrapidsecure.com/api_partner/ML_SmileOne_Unofficial.php"

  params = {
      "userid": "262856740",
      "zoneid": "3543",
      "package": "11MLBB",
      "PHPSEED": PHPSEED
  }

  response = requests.get(url, params=params)
  data = response.json()

  if data["status"] == "Success":
      print(f"Success! Package: {data['api_data']['product_name']}")
      print(f"Reference: {data['reference']}")
  else:
      print(f"Failed: {data['message']}")

PHP:

  <?php
  $PHPSEED = "YOUR_PHPSEED_HERE";

  $url = "https://api.camrapidsecure.com/api_partner/ML_SmileOne_Unofficial.php?" . http_build_query([
      "userid" => "262856740",
      "zoneid" => "3543",
      "package" => "11MLBB",
      "PHPSEED" => $PHPSEED
  ]);

  $ch = curl_init();
  curl_setopt($ch, CURLOPT_URL, $url);
  curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
  $response = curl_exec($ch);
  curl_close($ch);

  $data = json_decode($response, true);

  if ($data["status"] == "Success") {
      echo "Success! Package: " . $data["api_data"]["product_name"] . "\n";
      echo "Reference: " . $data["reference"] . "\n";
  } else {
      echo "Failed: " . $data["message"] . "\n";
  }
  ?>

CURL:

  curl "https://api.camrapidsecure.com/api_partner/ML_SmileOne_Unofficial.php?userid=262856740&zoneid=3543&package=11MLBB&PHPSEED=YOUR_PHPSEED"

-------------------------------------------------------------------------------

JSON Response Examples
----------------------

SUCCESS RESPONSE:

  {
    "status": "Success",
    "message": "Orders Successful",
    "api_message": "Success Orders",
    "reference": "TRAN17792979543497",
    "api_data": {
      "status": "SUCCESS",
      "message": "Success Orders",
      "reference_id": "",
      "player_id": "1130533383",
      "zone_id": "11329",
      "product_name": "250+250 BONUS",
      "region": "BR",
      "flowid": "OWZlOGtoK0",
      "execution_time_seconds": 3.53,
      "type_api": "SmileOne Unofficial API",
      "developed_by": "CamRapidSecure",
      "success_packages": [
        "250+250 BONUS"
      ],
      "failed_packages": []
    }
  }

ERROR RESPONSE (Invalid Cookie):

  {
    "status": "Error",
    "message": "Invalid PHPSEED. Please login to SmileOne and get valid cookie",
    "api_message": "Authentication Failed"
  }

ERROR RESPONSE (Insufficient Balance):

  {
    "status": "Error",
    "message": "Insufficient balance in SmileOne account",
    "api_message": "Balance check failed"
  }

ERROR RESPONSE (Wrong Player ID):

  {
    "status": "Error",
    "message": "Invalid player ID or zone ID",
    "api_message": "Player not found"
  }

-------------------------------------------------------------------------------

Available Mobile Legends Packages
---------------------------------

  Package Code     Diamonds     Bonus
  ------------     --------     -----
  5MLBB            5            -
  11MLBB           11           -
  22MLBB           22           -
  50MLBB           50           -
  100MLBB          100          -
  250MLBB          250          -
  500MLBB          500          -
  1000MLBB         1000         -

  Contact support for more package options

-------------------------------------------------------------------------------

How to Get PHPSEED Cookie
-------------------------

CHROME/EDGE/BRAVE:

  1. Login to smile.one
  2. Press F12 to open DevTools
  3. Go to Application -> Cookies -> https://www.smile.one
  4. Find PHPSEED and copy its value

FIREFOX:

  1. Login to smile.one
  2. Press F12 -> Storage -> Cookies
  3. Find PHPSEED and copy its value

-------------------------------------------------------------------------------

Response Fields Explanation
---------------------------

  status                     : Overall API status (Success/Error)
  message                    : Human-readable status message
  reference                  : Unique transaction reference ID
  api_data.player_id         : Mobile Legends Player ID
  api_data.zone_id           : Mobile Legends Zone ID
  api_data.product_name      : Purchased package name
  api_data.region            : Player's region (BR, ID, MY, etc.)
  api_data.flowid            : Unique flow identifier for tracking
  api_data.execution_time_seconds : API processing time
  api_data.success_packages  : Successfully topped up packages
  api_data.failed_packages   : Failed packages (if any)

-------------------------------------------------------------------------------

Error Codes & Solutions
-----------------------

  Error                      Solution
  -----                      --------
  Invalid PHPSEED            Re-login to SmileOne and get fresh cookie
  Insufficient balance       Top-up your SmileOne account balance
  Invalid player ID          Double-check player ID and zone ID
  Package not found          Use correct package code
  Rate limit exceeded        Wait a few seconds before next request

-------------------------------------------------------------------------------

Rate Limits
-----------

  Requests per minute    : 30 requests
  Requests per hour      : 500 requests
  Concurrent requests    : 5 simultaneous

-------------------------------------------------------------------------------

Security Notes
--------------

  [!] Keep your PHPSEED cookie private - never share it
  [*] Cookie expires after ~30 days, re-login to refresh
  [✓] All requests are sent over HTTPS
  [✓] We don't store your PHPSEED or transaction data

-------------------------------------------------------------------------------

FAQ
---

Q: Do I need to keep SmileOne tab open?
A: No. Once you get the PHPSEED cookie, you can close SmileOne.

Q: How long does the cookie last?
A: About 30 days. After that, just login again to get a new one.

Q: Can I top-up other games?
A: Yes! Contact Telegram support for other games (Free Fire, PUBG, COD, etc.)

Q: Is this official SmileOne API?
A: No, this is an unofficial API developed by CamRapidSecure.

Q: What happens if top-up fails?
A: Your SmileOne balance won't be deducted. Just try again.

-------------------------------------------------------------------------------

Support
-------

  Telegram Channel : @Cion (https://t.me/Cion)
  Telegram Support : @NightStrang6r (https://t.me/NightStrang6r)
  Website          : https://camrapidsecure.com/

-------------------------------------------------------------------------------

License
-------

  GPL-3.0 License - Free to use, modify, and distribute

-------------------------------------------------------------------------------

Show Your Support
-----------------

  If this API helps you, please give it a star on GitHub!

-------------------------------------------------------------------------------

  Built with speed by CamRapidSecure
