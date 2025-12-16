
## 📝 **COMPLETE MODIFICATION PLAN**

## Step 1: Made the Dummy_por module commented 
<img width="417" height="232" alt="image" src="https://github.com/user-attachments/assets/507fa0e4-e3dc-4f95-9017-78591453ccdd" />



### Step 2: In `rtl/vsdcaravel.v` (Top Module)

- Declare `resetn` as input

file:///home/student/Pictures/assign.png<img width="229" height="80" alt="image" src="https://github.com/user-attachments/assets/5c144f4a-7434-44cd-add8-eba003b32c34" />


```verilog
assign porb_h = resetn;
assign porb_l = resetn;
assign por_l = ~resetn;

```

### Step 3: In `rtl\caravel_core,v`

- Declare `porb_l` as output port
- its in the SoC interface

<img width="310" height="244" alt="image" src="https://github.com/user-attachments/assets/d313e45c-1968-4866-a73e-5cdbea535b85" />


- Comment out or remove the dummy_por
<img width="336" height="221" alt="image" src="https://github.com/user-attachments/assets/aa1f9669-1e8f-40cf-a6b4-bf286422185a" />

### Step 4: In `rtl\caravel_netlist.v`

- Complete Comment out ``include "dummy_por.v"`
<img width="923" height="872" alt="image" src="https://github.com/user-attachments/assets/3ec7e6c1-e7c6-428d-970b-acfb8d1b0bd4" />

### Step 5: In `dv/hkspi/hkspi_tb.v`

- Declare `resetn` as register
  <img width="609" height="372" alt="image" src="https://github.com/user-attachments/assets/a09f451f-e03b-44ce-8037-43e27bfcc644" />
  
 Make the `resetn` intialize to `0`
- Increase the delay to `#20000` and `#10000`
- Then After `#20000` delay make the `resetn` as `1`

  <img width="607" height="288" alt="image" src="https://github.com/user-attachments/assets/4913bdb3-fdbc-44b7-bbfa-53aca93b28e6" />

- Instantiate the `resetn` in `vsdcaravel`
- 
- <img width="739" height="585" alt="image" src="https://github.com/user-attachments/assets/ead9847d-da23-497d-94a3-09ab0669f67a" />
#### Note: Change the `hkspi_tb.v` in gls as above

### Step 5: Test
```bash
cd dv/hkspi
make clean && make
./simv
gtkwave hkspi.vcd
```

<img width="796" height="908" alt="RTL Passed" src="https://github.com/user-attachments/assets/cff4ad8e-8c31-411f-bc8d-a94ebee7b0c6" />




<img width="1708" height="900" alt="waveform" src="https://github.com/user-attachments/assets/c8074d69-1d5e-496a-a240-51c572716dd7" />

