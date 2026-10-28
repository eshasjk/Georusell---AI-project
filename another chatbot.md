from datetime import datetime
from zoneinfo import ZoneInfo

drivers = {
    "russell": {"no": 63, "country": "British", "role": "Primary"},
    "antonelli": {"no": 12, "country": "Italian", "role": "Primary"}
}

while True:
    user = input("\nAsk about drivers or a specific name: ").lower()

    if "exit" in user:
        break
    elif "drivers" in user:
        print("Mercedes Drivers: George Russell, Kimi Antonelli")
    elif "russell" in user or "antonelli" in user:
        name = "russell" if "russell" in user else "Kimi"
        info = drivers[name]
        print(f"#{info['no']} | {info['country']} | {info['role']} Driver")
    else:
        print("Unknown command.")