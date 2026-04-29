# CIVE202---Project-5

# AutoBMD
## Project Description 


##Repository Structure 
-[AutoBMD Code]: Jupyter Notebook containing all four modulues - Gradation, Volumetrics, IDEAL-CT and HWTT analysis. 
-[AutoBMD Data]: Source Excel file containing all raw input data across tabs(Gradation, Volumetrics, IDEAL-CT, HWTT).

All exported plots are listed below:
-[Gradation Curve]
-[Volumetrics Summary Table]
-[IDEAL-CT Load vs. Displacement]
-[Hamburge Rut Depth Plot]

##User Guide 
1. Program Overview
   AutoBMD creates four core asphalt mixture design analyses. It processes the raw data with no maunal calculations needed, producing visulaizations, calculated properties, and Pass/Fail determinations aligned with NDOT specifications.
   
2. Execution Sequence
- Data Loading:Ensures the [AutoBMD Data] is the same directory as [AutoBMD Code]. The notebook reads all imput data directly from the Excel tabs. 
- Modula A - Gradation: Tun the gradation cells to generate the Sieve Size vs. Percent Passing curve with NDOT Control Point overlayds.  
- Module B - Volumetrics: Run the volumetrics cells to calculate mix properties automatically flag samples outside the valid Air Voids range (6.5%-7.5%).
- Module C - IDEAL-CT: Run the IDEAL-CT cells to process Load vs. Displacement data, computer the CT Index, and export the plot. 
- Module D - HWTT: Run the HWTT cells to detect the Stripping Inflection Point (SIP), determine failure at 12.5 mm rut depth, and output a Pass/Fail result.

  
3. Methods
- All coding is done is a Jupyter Notebook using Python functions.
- Visualizations use Matpltlib andor Seaborn with labeled legends, custom formatting, and specification to meet the report standards.
- The CT Index is calculated by finding the area under the Load-Displacement curve, the post-peak slope at 75% of peak load, and displacement at that threshold.
- The SIP is detected through identifying the inflection point in the rut depth vs. cycles where the deformation slope abruptly increases. 
Module A: Aggregate Gradation Automator
Reads individual sieve percentages and blending rations from teh Gradation tab. Visualizes the combined gradation curve based on specified blend percentages and compares it to NDOT specs. Outputs a Sieve Size vs. % Pasing plot showing each aggregate type, the combined gradation, and specification band. 
Module B: Volumetric Properties Calculator
Reads measurements from the Volumetrics tab and applies the provided equations to calculate mix properties. Automatcially flas samples where Air Voids fall outside 6.5%-7.5% as "Invalid for Performance Testins." Outputs a summary table of all calculated volumetric properties and validity status. 
Module C: IDEAL-CT Cracking Index
Reads raw time-series Load vs. Displacement data from the IDEAL-CT tab. Automates the CT Index calculation by computing the area under the curve, the post-peak slope at 75% of peak load, and the displacement at that point. Outputs a clean Load vs. Displacement plot and the CT Index value for each sample. 
Module D: Rutting Analyzer (HWTT)
Reads cycle-count rut depth data from the HWTT tab. Detects the Stripping Inflecction Point (SIP) and identifies the exact cycle count where rut depth crosses the 12.5 mm failure threshold. Outputs a Rut Depth vs. Cycles plot with the SIP and failure point annotated, and a Pass/Fail determination based on survival to 20,000 cycles. 
##Project Goals 
The project goal is to transition the Nebraska Department of Transportation’s asphalt mixture process to a balanced mix design. Basically, automating their Excel process, making it so that the engineers don’t have to manually take data from their spreadsheets and have excel to the calculations, but take their data, input it into Python, and then have Python do their calculations.
- [Individual Gantt Chart]
- [Engineering Timesheet]

##Project Documentation 
Links: 
- [Scope of Work]
- [Annotated Code Document]
- [Written Report]
- [Flow Chart]





