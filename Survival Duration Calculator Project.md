```python
import sys

def calculate_duration(age, unit):
    if unit.lower() == 'months' or unit.lower() == 'm':
        return age * 12
    elif unit.lower() == 'weeks' or unit.lower() == 'w':
        return age * 52
    elif unit.lower() == 'days' or unit.lower() == 'd':
        return age * 365
    elif unit.lower() == 'hours' or unit.lower() == 'h':
        return age * 365 * 24
    elif unit.lower() == 'minutes' or unit.lower() == 'min':
        return age * 365 * 24 * 60
    elif unit.lower() == 'seconds' or unit.lower() == 's':
        return age * 365 * 24 * 60 * 60
    else:
        return "Invalid unit"

def main():
    print("Survival Duration Calculator Project\n")
    try:
        age = int(input("What's your age? "))
        unit = input("Please choose time unit: Months, Weeks, Days, Hours, Minutes, Seconds. \nNote: You can write the first letter or the full name of the time unit. ").strip()

        duration = calculate_duration(age, unit)

        if isinstance(duration, int):
            print(f"You lived for {duration} {unit.capitalize()}")
        else:
            print(duration)
    except ValueError:
        print("Please enter a valid age as a number.")
        sys.exit(1)

if __name__ == "__main__":
    main()

```

    Survival Duration Calculator Project
    
    What's your age? 32
    Please choose time unit: Months, Weeks, Days, Hours, Minutes, Seconds. 
    Note: You can write the first letter or the full name of the time unit. hours
    You lived for 280320 Hours
    


```python

```
