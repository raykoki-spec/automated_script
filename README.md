# File: README.md

# Data Processing Script 
An API script with a fetch function, a process function, and an output function.
Applied on simulated readings of a dairy farm cooperative, it makes requests, transforms data, and presents formated report.

## What It Does

- Process simulated readings from farm collection
- Flags farms with daily produce that are below the set target (10 L)
- Returns a summary report clearly indicating number of  farms  collected and total litres collected
- Exports the report to JSON
- Creates and saves a JSON file 


## Setup

```bash
pip install -r requirements.txt
```

## Usage

```python
def process_readings(readings, min_litres):
    total = sum(r["litres"] for r in readings)
    top = max(readings, key=lambda r: r["litres"])

    
    print(f"  Total litres:      {summary['total_litres']:.1f} L")
    print(f"  Top farm:          {summary['top_farm']} ({summary['top_litres']} L)")
```

## Sample Output

```

==================================================
  DAILY REPORT: UPLANDS DAIRY COOPERATIVE
==================================================
  Farms collected:   6
  Total litres:      142.0 L
  Average per farm:  23.7 L
  Top farm:          Kirwa's farm (33 L)
  All farms met target today.
==================================================

```

## Stack

Python

Built-in Modules: `json`
