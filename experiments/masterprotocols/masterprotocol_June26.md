---

author: Yatharth Bhasin
description: Master protocol for cell trapping.

---



# Master Protocol for cell trapping

+ Master protocol to process and trap cells for longterm imaging.
+ An experiment is started on each microscope. A common `metaexperiment` is used to log common processes.
+ Additional Information lists the use of flags to indicate microscope state.

## Requirements

1. **UV treated** microfluidics devices (x8) + a few reserves
2. Tubing kit (autoclaved) + syringes + stop walves (x16)
3. BSA + 15mL of water

## Steps

### Process and trap Cells

1. **Start UV treatment of microfluidics, clean bench, and transfer BSA solution to water bath:** Microfluidics are already placed in a UV chamber, start UV treatment for a set durtation: **UV-A 15W lamp for 30mins**. Clean every surface, all keyboards, all mice, and personal phone with Ethanol. Transfer BSA solution from the fridge to a water bath. Transfer to a small bottle if required.
2. **Check cultures,centrifugation-light separation; acclimation for 20mins:** Take samples of a few cultures and check motility, size, and contamination state under the microscope. Chose the best and isolate $20\mu L$ for cell counting. Transfer the culture to a clear centrifuge tube under asceptic conditions, and cover the tube with parafilm before caping. Centrifuge at **200g** for **10mins**. After centrifuging, light separate the cultures for **60 minutes** under bechtop light on a raised platform (30cm form the bench — 80-100 $\mu mol/m^2s$ of PAR light). Isolate about $V_r \approx1.0-2.0mL$ from the top carefully and dilute to $20mL$ using fresh media. Count dilluted cultures.
3. **Start BSA treatment**: Mix solid BSA with 15mL of $ddH_20$. Fill it in a 20mL syringe and purge the microfluidic devices with BSA under pressure via a $0.22\mu m$ syringe filter. Treat the devices for atleast 30 minutes before flusing with $1.5mL$ of fresh media. 
4. **Microscope alignment and mounting**: Mount purged microfluidic devices on the microscopes and center the device. Trap cells gently and bring the microscope to focus. Use `start_alignment()` to confirm sample focus and alignment. Then trap cells and use `trapped_one()`/`trapped_many()` to count cells and get speed estimates. If the cells are suitable, leave the microscopes for checkpoint clearance and move to the next one. Else, call `open_trap()` and retrap cell(s).
5. Update metadata on each microscope.

### Cleanup

1. **Cleanup:** Recycle the paper and plastic. Clean the bench with ethanol, and dispose the cultures with bleach if necessary.
2. **Count cell culture** and update the metaexperiment.
3. Update metadata if not already done. Record room temepraure and number of broken devices. And update metaexperiment.

## Additional Information

1. **Blue flag**: Meta-data has been updated.
2. **Yellow flag X1**: Cell(s) is/are trapped. Automatic checkpointing is scheduled.
3. **Green flag: ** Cells acclimated for 20mins. The scope is ready to acquire.
4. **Red flag:** Air bubbles, the trap is being purged.
5. **Pink flag X1:** Cell not spotted after trapping. Wait 10 more minutes.
6. **Pink flag X2**: Cell not spotted after trapping. Wait another 10 minutes, before changing to a red flag.
7. **White flag:** Microfluidic device broken without replacement. The scope has been surrendered.
