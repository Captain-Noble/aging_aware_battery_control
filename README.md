This repository contains data and notebooks for the paper [`Aging-Aware Battery Control via Convex Optimization`](https://stanford.edu/~boyd/papers/aging_aware_battery_control.html).  
## Environment and Library Versions

To reproduce the results in this notebook, use the following versions:

| Library     | Version       |
|-------------|---------------|
| Python      | 3.12.2         |
| pandas      | 2.2.3          |
| numpy       | 1.26.4         |
| cvxpy       | 1.6.0          |
| matplotlib  | 3.10.0         |

**Note:**  
- `os`, `sys`, `time`, `calendar`, and `datetime` are built-in Python libraries and do not require separate installation.

### Instructions
To ensure reproducibility, create a virtual environment and install the specified versions.  
Example using `pip`:

```bash
python3 -m venv venv
source venv/bin/activate
pip install pandas==2.2.3 numpy==1.26.4 cvxpy==1.6.0 matplotlib==3.10.0

