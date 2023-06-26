# slogger-python
A python porting of the existing Slogger repository, found at github.com/NicoNex/slogger

compared to the original implementation, the calls are not stacked.

Example (can be checked by runnning slogger.py as a script):
```python
title = "title"
results = {"result": "positive", "n_cycles": 300}
final_score = "saved 300 kWh"

logbox = SLogger(title=title)
print(logbox.width)
logbox.addFields(results)
print(logbox.width)
logbox.addLine(final_score)
print(logbox.width)
logbox.print()
```

Result
```
┌──────────────────────────────┐
| 26-42-23 12:06:48 - title    |
├──────────────────────────────┤
| result: positive             |
| n_cycles: 300                |
| saved 300 kWh                |
└──────────────────────────────┘
```
In case of more complex methods, the same considerations apply to the original case.
