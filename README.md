# Petroleum-Geology-Analyses
This series of Python Scripts Interogates, analyzes and charts data sets commonly used by petroleum Geologist. Data for the analyses come from Natrona County, Wyoming and Teapot Dome / Salt Creek Field complex. There are six exercises (Jupyter Notebooks) that primarily analyzes data using the Pandas library. The Jupyter Notebooks are summarized and enumerate the the basic Python skill that were used:

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
  - Uses groupby and merge_asof (an approximate merge)
  - Uses pivot_table, .columns, .drop, .to_sting
- Plot wireline logs with tops annotated and core plug data and pay
- Generate a probability distribution for core porosity
- Report descriptive statistics 
5. Ex5 **Time-Depth** - Creates a time-depth polynomial using check-shot survey
- Read Excel workbook from Github with Check Shot survey, sonic wireline log (DT) and formation tops
- Examines the imported data
- Fit a polynomial trend to the time ~ depth and examine residuals
- Executive summary charts - Three charts side by side
  - Time ~ Depth Polynomial
  - Check Shot Depth ~ Avg Velocity, RMS Velocity, Invteral Velocity
  - Sonic Log overlain with Interval Velocity
6. **Core Analysis** - Examine core data with respect to wireline log data, porosity ~ permeability realtionship and calculate Kh (perm - height)
- Import Excel workbook from Github: Core Gamma Ray (gr), core porosity and permeability (kphi), wireline density porosity (dphi) & FM tops
- Examine imported data and chart core gamma raw with tops of cores
- Chart wireline density porosity with core porosity
- Examine distribution / statitical measures of core porosity and permeability
  - Descriptive Statistics
  - Box and Wisker Charts
  - Histograms
- Chart core permeability with wireline data
- Scatter plot core porosity ~ permeability on linear-linear, log-linear and log-log scales (which scale is best for regressions model)
- Create and compare Statsmodels 2nd order polynomial for the semi-log and the linear model for the log-log scale
  - Determine which is the better model
- Use regression model to calculate permeability from wireline density porosity
  - Overlay modeled permeability form wireline density porosity with core permeabilty on depth chart
- Calculate permeability-height (Kh) which is a measure of potential well productivity. 
