import os
import time
import requests
from random import randint

BOT_TOKEN = os.getenv(BOT_TOKEN)
CHAT_ID = os.getenv(CHAT_ID)
CHECK_INTERVAL = int(os.getenv(CHECK_INTERVAL, 60))

CITIES = [Edirne, İzmir, Antalya]

def send_telegram(msg)
    url = fhttpsapi.telegram.orgbot{BOT_TOKEN}sendMessage
    data = {chat_id CHAT_ID, text msg}
    resp = requests.post(url, data=data)
    return resp.ok

def check_city(city_name)
    # Simülasyon %30 şansla müsaitlik bildiriliyor
    available = randint(1, 10)  7
    if available
        msg = f🔔 {city_name} şubesi için Bulgaristan vize randevusu bulundu!
        send_telegram(msg)

if __name__ == __main__
    while True
        for city in CITIES
            check_city(city)
        time.sleep(CHECK_INTERVAL)
