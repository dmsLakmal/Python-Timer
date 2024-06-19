# Countdown Timer
This is a simple Python script that acts as a countdown timer. You can enter the time in seconds, and it will count down from that time, 
displaying the remaining months, days, hours, minutes, and seconds.

## Usage
01. Ensure you have Python installed on your system.
02. Copy the script into a file, e.g., countdown_timer.py.
03. Run the script using a Python interpreter.
```sh
python countdown_timer.py
```
5. Enter the desired countdown time in seconds when prompted.
## Code
Copy code
```sh
import time

my_time = int(input("Enter the time in seconds: "))

for x in range(my_time, 0, -1):
    seconds = x % 60
    minutes = int(x / 60) % 60
    hours = int(x / 3600) % 24
    days = int(x / 86400) % 30
    months = int(x / 2592000)
    print(f"{months:02}:{days:02}:{hours:02}:{minutes:02}:{seconds:02}")
    time.sleep(1)

print("TIME'S UP!")
```
## Explanation

- The script takes an input time in seconds from the user.
- It then counts down from that time, updating the display every second.
- The remaining time is displayed in the format `MM:DD:HH:MM:SS`:
  - `MM` - Months
  - `DD` - Days
  - `HH` - Hours
  - `MM` - Minutes
  - `SS` - Seconds
- The script pauses for one second between updates using `time.sleep(1)`.
- When the countdown reaches zero, the script prints "TIME'S UP!".

## Requirements
  - Python 3.x
