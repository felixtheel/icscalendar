# icscalendar

https://img.shields.io/github/last-commit/felixtheel/icscalendar.svg?style=flat

## Usage
```python
import icscalendar
from datetime import datetime

# Start and End datetime objects
start = datetime(2019, 12, 24, 0, 0, 0).strftime(icscalendar.dayteformat)
end = datetime(2019, 12, 27, 0, 0, 0).strftime(icscalendar.dayteformat)

# New ICSCALENDAR object
ics = icscalendar.icscalendar()

# Add an event
ics.add(summary='Christmas with the family',
        description='Christmas with my awesome family',
        start=start,
        end=end,
        location='My beautiful home\, Santa Claus Road 25\, North pole')

# Generate the VCalendar
ics.generate()

# Save
ics.save('christmas.ics')

print('Ready to add christmas to your calendar :)')
```
