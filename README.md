# quick_EDA
Using data prep and pandas profiling to prepare EDA analysis in 5 mins

# Example A :pandas profiling
## install in jupyter notebook
```
import sys
!{sys.executable} -m pip install -U pandas-profiling[notebook]
!jupyter nbextension enable --py widgetsnbextension
```
##import packages and data
```
import numpy as np
import pandas as pd
from pandas_profiling import ProfileReport
df=pd.read_excel('COVID.xlsx')
```
## generate the standard profiling report
```

profile = ProfileReport(df, title="Sickle Cell Disease")
```
##consume the report inside a Jupyter noteboo
```
profile.to_notebook_iframe()
```
## to generate a HTML report file
```
profile.to_file("your_report.html")
```

# Example B : data prep
## install in jupyter notebook
```
pip install -U dataprep
```
## import packages and data
```
from dataprep.eda import plot, plot_correlation, plot_missing,create_report
import pandas as pd
df=pd.read_excel('COVID.xlsx')
```
## generate report
```
plot(df)
create_report(df).show_browser()
```

## to be added : data prep cleaner
