# 11-12-2025. 
# Objective:
RISC V Tape Out Program Thanks for VSD Kunal Gosh, Sameer bhai and IIT Gandhinagar started 11 am with 

<img width="861" height="457" alt="image" src="https://github.com/user-attachments/assets/75a8d745-de36-42ef-bc51-797930635c62" />

<img width="1059" height="606" alt="image" src="https://github.com/user-attachments/assets/aa6c5c97-e6f8-41f7-b257-df03b6ab5dfb" />

# 12-12-2025. 
# Objective:
Got Credential of login start working on RISC V Tape Out Program on opensource tools jumped into commercial tools of synopsys

<img width="560" height="193" alt="image" src="https://github.com/user-attachments/assets/09d31916-74e6-415a-86ae-e0ae32ca3b26" />

# 13-12-2025. 
# Objective:
Challenge: 1 with Synthesis with blackbox modules RAM128, RAM256 and POR 
Challenge: 2 GLS

Results  got with normal synthesis but without topographical-based synthesis
# 14-12-2025. 
# Objective:
Identified with soultion with compile_ultra -incremental The incremental compile also supports adaptive retiming with the compile_ultra -incremental -retime command.

Running the compile_ultra -incremental command on a topographical netlist results in placement-based optimization only. This compile should not be thought of as an incremental mapping. 
Finally the soultion for GLS with adding all the rtl files in gl folder
# 15-12-2025. 
# Objective:
POR Power On Resent Module usage analysis; done brain stroming come across 3 approaches:
### 1. Approache :
1. approaches identify all the signals replaced  (9 files to modify,~30 changes required, MODULES WITH REAL DEPENDENCIES:
 housekeeping.v:           6 locations (Flash, SPI, state machines)
 caravel_clocking.v:       1 CRITICAL (master reset AND gate) )
### Results:
  Failed
### 2. Approache :
2. Approach Just replacing the signal of PoR (porb_h,porb_l,por) with resetb
### Results:
  passed
### 3. Approache :
3. Approach keep extrernal input reset pin to the Core
### Results:
   Passed
10:08 am started without break Time-up for the closing the lab it was 8:55pm
# 16-12-2025. 
# Objective:
Started with new challenge brainstroming with document verifing with design again with task!!!till 2:00 pm
Started working on Documnetation.
