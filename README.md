# SUSTech Academic Calendar Data

南方科技大学校历数据

## Files

| File | Description |
|------|-------------|
| `2026-general.json` | Holiday dates (same for all programs) |
| `2026-undergraduate.json` | Undergraduate-specific schedule |
| `2026-graduate.json` | Graduate-specific schedule |

## Usage

```bash
# Raw URL
curl https://raw.githubusercontent.com/dumixthestpd/sustech-calendar/main/2026-general.json

# Or Python
import requests
holidays = requests.get("https://raw.githubusercontent.com/dumixthestpd/sustech-calendar/main/2026-general.json").json()
```

## Format

### 2026-general.json
```json
{
  "holidays": [
    {"name": "春节", "date": "2026-02-17", "end": "2026-02-23"},
    ...
  ]
}
```

### 2026-underscore.json / 2026-graduate.json
```json
{
  "semester": {
    "week_1_monday": "2026-02-23",
    "first_teaching_day": "2026-02-25",
    "total_teaching_weeks": 17,
    "semester_end": "2026-07-05"
  },
  "week_pattern": {
    "odd_weeks": [1, 3, 5, 7, 9, 11, 13, 15, 17],
    "even_weeks": [2, 4, 6, 8, 10, 12, 14, 16],
    "class_days": {
      "1": ["Mon", "Wed", "Fri"],
      "0": ["Tue", "Thu"]
    }
  },
  "exam_weeks": [...],
  "special_days": [...]
}
```

## Data Source

SUSTech official academic calendar:
https://www.sustech.edu.cn/zh/academic-calendar.html