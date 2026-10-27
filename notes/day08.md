# Day 8: Data Analysis in Excel + Carbohydrates

Date: 26/10/2026

## Part 1: Data analysis in Excel

Basic calculations and charts in Excel. I'll use these later to check and summarize biological data (for example gene expression values, colony counts, or lab measurements).

### Calculations

**Fill (fill handle)**
- Type a value or formula in a cell, then drag the small square at the bottom-right corner of the cell down or across.
- Excel copies the content into the other cells. For formulas, the cell references adjust automatically.
- It also continues patterns such as 1, 2, 3 or dates.

**Sum**
- `=SUM(B2:B10)` adds all values from B2 to B10.
- `=B2+C2` adds two specific cells.

**Subtraction**
- There is no SUBTRACT function. Use the minus sign: `=B2-C2`.

**Average (mean)**
- In Excel the mean is calculated with AVERAGE.
- `=AVERAGE(B2:B10)` gives the mean of B2 to B10.

**Min and Max**
- `=MIN(B2:B10)` gives the smallest value in the range.
- `=MAX(B2:B10)` gives the largest value in the range.

**Division**
- Use the slash sign: `=B2/C2`.

**COUNT**
- Counts how many cells in a range contain numbers (empty cells and text are ignored).
- `=COUNT(B2:B20)` returns the number of numeric values from B2 to B20.

**COUNTIF**
- Counts the cells that meet a condition.
- `=COUNTIF(B2:B20,">50")` counts how many values are greater than 50.
- `=COUNTIF(A2:A20,"Bacteria")` counts how many cells contain the word Bacteria.

### Quick reference

| Operation | Formula example |
|-----------|-----------------|
| Sum | `=SUM(B2:B10)` |
| Subtract | `=B2-C2` |
| Average (mean) | `=AVERAGE(B2:B10)` |
| Minimum | `=MIN(B2:B10)` |
| Maximum | `=MAX(B2:B10)` |
| Divide | `=B2/C2` |
| Count numbers | `=COUNT(B2:B20)` |
| Count with a condition | `=COUNTIF(B2:B20,">50")` |
| Fill | drag the corner handle |

### Charts
To make a chart: select the data, then go to Insert > Charts and pick the type.

| Chart | Best used for | Example |
|-------|---------------|---------|
| Scatter plot | Relationship between two numeric variables | Concentration vs absorbance |
| Bar graph | Comparing categories | Colony count for different samples |
| Pie chart | Parts of a whole (percentages), only a few categories | Share of different bacteria in a sample |
| Line graph | Change over time | Bacterial growth over hours |

Every chart should have a title, labelled axes, and units.

### Key points
- Every formula starts with `=`.
- Use the fill handle to apply one formula to a whole column instead of typing it again.
- Cell ranges use a colon, for example `B2:B10`.
- Choose the chart type based on the question: relationship (scatter), comparison (bar), proportion (pie), trend (line).

### Why this matters for bioinformatics
Before analysing data in Python or R, I can use Excel to quickly check totals, averages, counts, and trends in a small dataset, and to draw a first plot.

## Part 2: Biochemistry class, carbohydrates

### Carbohydrates
- Organic molecules made of carbon, hydrogen and oxygen, often with the general formula Cn(H2O)n.
- They are a main source of energy and also have structural roles.

### Monosaccharides
- The simplest sugars. They cannot be broken down into smaller sugars by hydrolysis.
- Examples: glucose, fructose, galactose (6 carbons), ribose and deoxyribose (5 carbons, found in RNA and DNA).
- Aldose: has an aldehyde group (for example glucose). Ketose: has a ketone group (for example fructose).

### Chirality
- A carbon bonded to four different groups is a chiral carbon (chiral centre).
- A chiral molecule and its mirror image cannot be superimposed. The two forms are called enantiomers.
- Sugars are labelled D or L. The sugars found in nature are mostly the D form (for example D-glucose).

### Why this matters
Enantiomers can behave very differently in the body, so chirality is important in drug discovery.
