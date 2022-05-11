# Petroleum-Geology-Analyses
This series of Python Scripts Interogates, analyzes and charts data sets commonly used by petroleum Geologist.
There are eight jobs (exercises) that primarily analyzes data using the Pandas library:
0. **Ex 0 Production Data analysis** - Looks at oil and gas productions data from Natrona County, Wyoming, USA for the year 2000.
- _Examines a pandas dataframe_
- _Summarize data using pivot tables_
- _Plot histograms, stacked histograms, pie chart, line and scatter plots using matplotlib and plotly_
- _Plot a map of data points with topography using plotly_
1. **Ex1 Well Header Ex** - Examines well headers for Teapot Dome Field wells
- Looks at the number of wells
- Makes sure that the Wellbore IDs are all the same lenght and the number of sidetrack wells
- Drilling history, by decadea an makes bar chart
- Tricontour map of elevations with colorbar_
2. **Ex2 Tops** - Examine well formation top depths
- Read CSV and Excel XLSX worksheets from Github
- Examine data and make sure wellbore id numbers are strings of the same lenght
- Merge dataframes
- .count() functions
- scatter plot with color ramp and tricontours
3. **Ex3 Directions Survey_Interpolations** - Linear interpolation of measured depths to true vertical depths for formation tops
- Read Excel XLSX worksheets from Github
- Examine data
- Merge dataframes
- Sort dataframes
- .shift() function to capture values from rows above and below (same as SAS's lag function)
- .notna() - remove null (NaN) values
- Scatter plot with annotated labels
4. **Ex4 LogAnalysis 48-28x** - Reads and analyzes wireline (.las) file, core data and tops
- Reads wireline .las file from Github using Lasio library
- Reads Excel worksheets from Github
- Defines and calculatets pay, bed ID and net sand
  - Uses .sum, .cumsum, .drop functions
  - Uses groupby and merge_asof
  - Uses pivot_table, .columns, .drop, .to_sting
