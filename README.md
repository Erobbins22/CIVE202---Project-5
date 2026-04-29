# CIVE202---Project-5

# AutoBMD
## Project Description 


## Repository Structure 
-[AutoBMD Code](CIVE202_Spring2026_GroupGeost-02-01_Project5_Final Code.ipynb): Jupyter Notebook containing all four modules - Gradation, Volumetrics, IDEAL-CT, and HWTT analysis. 

-[AutoBMD Data](AutoBMD.xlsx): Source Excel file containing all raw input data across tabs(Gradation, Volumetrics, IDEAL-CT, HWTT).

All exported plots are listed below:
-[Gradation Curve]
-[Volumetrics Summary Table]
-[IDEAL-CT Load vs. Displacement]
-[ Rut Depth Plot]

## User Guide 
### 1. Program Overview
   AutoBMD creates four core asphalt mixture design analyses. It processes the raw data with no manual calculations needed, producing visualizations, calculated properties, and Pass/Fail determinations aligned with NDOT specifications.
   
### 2. Execution Sequence
- Data Loading:Ensures the [AutoBMD Data](AutoBMD.xlsx) is the same directory as [AutoBMD Data](AutoBMD.xlsx). The notebook reads all input data directly from the Excel tabs. 
- Modula A - Gradation: Turn the gradation cells to generate the Sieve Size vs. Percent Passing curve with NDOT Control Point overlays.  
- Module B - Volumetrics: Run the volumetrics cells to calculate mix properties automatically, flag samples outside the valid Air Voids range (6.5%-7.5%).
- Module C - IDEAL-CT: Run the IDEAL-CT cells to process Load vs. Displacement data, compute the CT Index, and export the plot. 
- Module D - HWTT: Run the HWTT cells to detect the Stripping Inflection Point (SIP), determine failure at 12.5 mm rut depth, and output a Pass/Fail result.

  
### 3. Methods
- All coding is done in a Jupyter Notebook using Python functions.
- Visualizations use Matplotlib and/or Seaborn with labeled legends, custom formatting, and specifications to meet the report standards.
- The CT Index is calculated by finding the area under the Load-Displacement curve, the post-peak slope at 75% of peak load, and displacement at that threshold.
- The SIP is detected through identifying the inflection point in the rut depth vs. cycles, where the deformation slope abruptly increases. 
#### Module A: Aggregate Gradation Automator
Reads individual sieve percentages and blending ratios from the Gradation tab. Visualizes the combined gradation curve based on specified blend percentages and compares it to NDOT specs. Outputs a Sieve Size vs. % Passing plot showing each aggregate type, the combined gradation, and specification band. 
#### Module B: Volumetric Properties Calculator
Reads measurements from the Volumetrics tab and applies the provided equations to calculate mix properties. Automatically flash samples where Air Voids fall outside 6.5%-7.5% as "Invalid for Performance Testing." Outputs a summary table of all calculated volumetric properties and validity status. 
#### Module C: IDEAL-CT Cracking Index
Reads raw time-series Load vs. Displacement data from the IDEAL-CT tab. Automates the CT Index calculation by computing the area under the curve, the post-peak slope at 75% of peak load, and the displacement at that point. Outputs a clean Load vs. Displacement plot and the CT Index value for each sample. 
#### Module D: Rutting Analyzer (HWTT)
Reads cycle-count rut depth data from the HWTT tab. Detects the Stripping Inflection Point (SIP) and identifies the exact cycle count where rut depth crosses the 12.5 mm failure threshold. Outputs a Rut Depth vs. Cycles plot with the SIP and failure point annotated, and a Pass/Fail determination based on survival to 20,000 cycles. 


## Project Goals 
The project goal is to transition the Nebraska Department of Transportation’s asphalt mixture process to a balanced mix design. Basically, automating their Excel process, making it so that the engineers don’t have to manually take data from their spreadsheets and have Excel do the calculations, but take their data, input it into Python, and then have Python do their calculations.
- [Individual Gantt Chart](CIVE202_Spring2026_GroupGeost-02-01_Project5_Ganttchart.xlsx)
- [Engineering Timesheet]

## Project Documentation 
Links: 
- [Scope of Work](CIVE202_Spring2026_GroupGeost-02-01_Project5_SOW.docx)
- [Annotated Code Document](CIVE202_Spring2026_GroupGeost-02-01_Project5_ACD.docx)
- [Written Report]
- [Flow Chart](CIVE202_Spring2026_GroupGeost-02-01_Project5_Flowchart.pdf)





