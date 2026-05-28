# Hi, I'm Michael Newman 👋

### Transportation & Atmospheric Science Professional | Data & GIS Analyst
I blend a decade of high-stakes operational experience with modern data science architectures to solve complex spatial, logical, and predictive data puzzles. 

* 🛠️ **Core Toolbelt:** Python, SQL, Snowflake, Power BI, PowerShell
* 🌍 **Domain Expertise:** Atmospheric Sciences, Fluid Dynamics, Logistics, Data Quality Control & Custodianship

---

## 📈 Featured Script: Automated Data Cleaning Pipeline

```python
import pandas as pd
import numpy as np

def clean_logistics_data(file_path):
    # Load messy data dataset
    df = pd.read_csv(file_path)
    
    # Drop rows missing critical transit identifiers
    df.dropna(subset=['transit_id'], inplace=True)
    
    # Standardize anomalies and timestamp strings todatetime objects
    df['timestamp'] = pd.to_datetime(df['timestamp'], errors='coerce')
    
    # Remove negative duration values (operational anomalies)
    df = df[df['duration_minutes'] >= 0]
    
    print(f"Pipeline successfully optimized. Matrix shape: {df.shape}")
    return df
