# Georusell---AI-project
My newest AI project ever
from datetime import datetime
from zoneinfo import ZoneInfo

while True:
    user = input("Hi! My name is George. How can I help you? ")

    if "weather" in user:
        print("The weather today is sunny!")
    elif "time" in user:
        malaysia_tz = ZoneInfo("Asia/Kuala_Lumpur")
        current_time = datetime.now(malaysia_tz).strftime("%d-%m-%Y %I:%M %p")
        print(f"It's {current_time} sweetheart.")
    else:
        print("Sorry, I don't understand.")
