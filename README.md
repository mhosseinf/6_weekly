# 6_weekly

import pandas as pd
from pathlib import Path
excel_file_path = Path('resource/data.xlsx')
pivot_tab = 'Data'
data_tab = '6 Weekly'
clean_data='finalData'
table_df = pd.read_excel(excel_file_path, sheet_name=data_tab)
p_table = pd.pivot_table(table_df, index = ['Work order', 'Project Title', 'Task -List'],values=['Project Hours Total'],filter=['Main Field Team
/
Team
'])
