---
Author: Yatharth bhasin
date: 12-03-2024
---

# Master Protocol

The protocol for trapping cells.

## Requirements

1. Set of 8 traps.
2. (fresh) 16 3-way valves (stopcocks)
3. (autoclaved) syringe and tubing kit (16 each)

## Macro procedures

1. Creating of meta experiment and cluster bootup
2. Setting-up of individual experiments, traps, and trap-purge
3. Swimmer selection protocol
4. Cell trapping(s)
5. Start acquisition of cluster 1
6. Start acquisition of cluster 2
7. First clearance
8. Second clearance



## Procedure

1. **Creating of meta experiment and cluster bootup**

  ```python
  #ScriptEngine.run_now("/scripts/lab/metaexperiment.py", globals())
  ```
  a. Log temperature from the differnt terminals. And adjust thermostat. Clean the benches with ethanol.
  b. Create meta-experiment on current scope and reboot the whole cluster.
  c. Start trappyscopes on the whole cluster (with the experiment script)

2. **Setting-up of individual experiments, traps, and trap-purge**
  a. Check the Network server for the presence of all the different experiments.
  b. Add sterile (autoclaved) tubing, stopcock, and syringes to the devices.
  c. Updates the trap id on each of the microscope and mount the trap. Focus and adjust the trap using the `test_fov` function.
  d. Fill 8 syringes with fresh media and use them to purge from one side for all the microscopes.
  e. Leave the microscopes to purge.

3. **Swimmer selection protocol**

  1. Start the cell-selection protocol
  	0. Bring out the cells and start processing cultures.
  	0. Take cells in their log phase: $10^5$ cells per mL (which are passaged daily).
  	0. Remove a portion for doing daily dilutions: *about 10%*. (culture for the next day).
  	0. Take the rest of the culture and replace cap with parafilm and put in the incubator for separation.
  	0. Let cells sediment for 5 mins under illumination without any shaking.
  	0. Extract the supernatant: About 25-50% fraction.
  	0. Centrifuge the cells 'gently' for 3mins at 100g.
  	0. Remove the top 25% fraction of the culture and isolate in a sterile tube (cover the tube in black tape).
  	0. Count the isolated fraction and add media to set the density to $\approx 5 \times 10^5$ cells per mL (required volume = 16mL to 20mL)
  	0. Target density: Assuming a trap size (2.8mm diameter and $34\mu m$ hight which yields a volume of $0.209mm^3$ or $0.209 \cross 10^{-3}mL$). This giives a target density of $0.48 \cross 10^4$ cells per mL.
  2. Count cells and update them in the `cell_count` measurement stream.
  3. Load 8 syringes with 2mL/3mL  of cell cultures each and cover them with black paper.

4. **Cell trapping(s)**

	1. Add the syringes to the other stopcock without creating bubbles and open the valves, this should equalise the pressure.
	2. Let about 0.25mL of culture pass before trying to confine cells.  
	3. Confine a "low contrast, small, fast" cell.
	4. Mark the process with the following flags:
		**orange**: single cell trapped but not verified. 
		**green**: verified to be a single cell after atleast 10mins.
		**red**: air bubbles / re-purgeing. Set to purge and move to another microscope.
	5. Once the cell is trapped, leave the stopcocks in closed positions.

5. **Start acquisition of cluster A**

6. **Start acquisition of cluster B**

7. **First clearance**

8. **Second clearance**

---

12. Check cells again for stability (proving difficult with mjpeg) :: **not possible for now. Some script adjustments are required.**
13. Clean traps and prepare the next set of microfluidics:
	1. Remove the syringes and stopcocks, and clear the cultures inside them. Place them in seperate bins.
	2. Connect the pumps to the microfluidics using the Leur locks and put the other end in a measuring cyclinder.
	3. Set forward pump rates such that the outflux is about 1 drop per second.
	4. Purge the following:
		1. 3mL of MilliQ (10 mins)
		2. 3mL of 0.1% Tween 20  (10 mins)
		3. 3mL of MilliQ  (10 mins)
		4. 3mL of 20% Ethanol  (10 mins)
		5. 3mL of MilliQ (10mins)
		6. Airpurge by hand
14. Remove tubings and put them in their respective bins.
15. Place the devices on 95% hot plate for a few hours / overnight.
16. Repeat for the other set.
17. Add bleach to the collected culture and trash appropriately.
18. Prepare the next round of microfluidics:
	1. Set of 8
	2. 16 tubes with needles (autoclaved)
	3. 16 syringes
	4. 16 stopcocks
19. Go home!