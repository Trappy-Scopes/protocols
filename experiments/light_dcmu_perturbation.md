---

author: Yatharth Bhasin
description: Light perturbation experiment testing the effect of continuous dim red light against dark, red + DCMU and white light conditions on C. reinhardtii motility.
references: masterprotocol_June26.md, selectswimmers.md, bsa_treatment.md, light_calibration.md

---

# Light and DCMU perturbation

1. **Aim:** Test the effect of continuous dim red light on cell motility against three other conditions: dark, red light with PSII blocked by DCMU, and white light.
2. **Conditions:** There are four conditions, each with 2 scopes per day. 2 scopes run DCMU-TAPP and 6 run vehicle-TAPP.
3. **Light during setup:** All setup (mounting, alignment, trapping) is done under the control red light on every scope.
4. **t₀:** t₀ is the end of the 20-min dark acclimation plus trapping. At t₀ each scope's condition light is applied; the dark scopes stay dark after the 0th split acquisition completes.
5. **DCMU timing:** DCMU cultures are diluted directly into DCMU-TAPP, so they are acclimated to DCMU before the dark acclimation.
6. Cell processing, BSA treatment and trapping follow the latest master protocol, with the changes stated below.

## Requirements

1. DCMU (diuron, MW 233.09 g/mol)
2. Absolute ethanol (one bottle, used for both the stock and the vehicle)
3. New 15 mL PP Falcon tube, 2 mL PP screw-cap microtubes (single use) and aluminium foil
4. Sterile TAPP, about 60 mL per day
5. Requirements of the master protocol: 8 BSA-treated devices, a tubing kit, syringes and stopcocks
6. Microscopes M1–M8 with calibrated red, green and blue LEDs

## Steps

### DCMU stock (10 mM in ethanol, 1000×, one batch split into aliquots)

1. Wear gloves. Weigh **~11.7 mg DCMU** into a new **15 mL PP Falcon tube** and record the exact mass.
2. Add **0.429 mL absolute ethanol per mg** of DCMU (11.7 mg → 5.0 mL) to make a 10 mM stock. Vortex until fully dissolved.
3. Split into **2 mL PP screw-cap microtubes at ~1.8 mL each**, so each tube is nearly full with minimal headspace. Discard the Falcon tube as DCMU waste.
4. Label each aliquot `["LP", DATE, "DCMU 10 mM EtOH", "TOXIC", aliquot n]`, weigh it and write the mass on the label. Wrap in foil and store at **−20 °C**.
5. Use **one aliquot per 3-day block**. Before opening an aliquot, weigh it again; if more than 2–3% of the liquid's mass has been lost, discard it.
6. After the last day of the block, discard the opened aliquot as chemical waste. Do not reuse the tube.

### Media (prepare fresh each day)

1. Bring the stock tube to room temperature.
2. Make **DCMU-TAPP**: **15 mL TAPP + 15 µL DCMU stock** (10 µM DCMU, 0.1% ethanol).
3. Make **vehicle-TAPP**: **45 mL TAPP + 45 µL absolute ethanol** (0.1% ethanol).
4. Pipette into the liquid, invert about 10× to mix and label both tubes. Wrap DCMU-TAPP in foil and keep both at room temperature.
5. Return the stock tube to −20 °C straight away.

### Sample preparation

1. Process **one culture** using swimmer selection (centrifugation and 60 min light separation), and isolate V_r ≈ 1.0–2.0 mL.
2. **Split V_r about 1:3:**
   1. Dilute **¼ V_r to 5 mL with DCMU-TAPP** (2 scopes).
   2. Dilute **¾ V_r to 15 mL with vehicle-TAPP** (6 scopes).
3. Cover both bottles with foil for dark acclimation. DCMU exposure starts at this step.
4. After the BSA treatment, flush each device with **≥3 mL of its matching medium**: DCMU-TAPP for the DCMU devices and vehicle-TAPP for all others.
5. Assign the conditions to the scopes (table below), with 2 scopes per condition. Rotate the assignment across days and label the DCMU scopes, devices and syringes.

### Light conditions

Acquisition light is **identical for all four conditions**: red (627 nm) at **0.5 V**. Only the long-term light between acquisitions is condition-specific.

| # | Condition | Medium | Long-term light (from t₀, between acquisitions) | Acquisition light |
|---|---|---|---|---|
| 1 | **Control** | vehicle-TAPP | Red (627 nm), continuous | Red 0.5 V |
| 2 | **Dark** | vehicle-TAPP | Off | Red 0.5 V |
| 3 | **Red + DCMU** | DCMU-TAPP | Red (627 nm), continuous | Red 0.5 V |
| 4 | **White** | vehicle-TAPP | Red, plus green and blue at max operational voltage, continuous | Red 0.5 V (green and blue off) |

1. **Red setting (all conditions):** Set the red LED from each scope's calibration curve to give **1.5–2 µmol m⁻² s⁻¹** at the sample plane. 
2. **Room light:** Keep room lights off and the scopes shielded for the whole run.
3. **Setup:** Mount, align and trap under the control red light on every scope, keeping the time roughly equal across scopes. 
4. **Trapping:** Apply control red light conditions during trapping.
5. **t₀:** Apply each scope's condition light and start acquisition. Dark scopes acquire the 0th split under red like all others, then switch to dark. For the white conditions, green and blue are switched off for every acquisition (red only, 0.5 V) and back on when it ends; at t₀ the first acquisition starts immediately after the light switch. The acquisition schedule is identical for all conditions. 
6. **Metadata:** For each scope, record the condition, medium, stock aliquot number, LED voltages (R/G/B) for both the long-term and the acquisition light, measured PPFD and t₀.

## Additional Information

1. **Vehicle control:** All non-DCMU conditions contain the same 0.1% ethanol. Use the same ethanol bottle for the stock and the vehicle.
2. **DCMU carry-over:** Carry-over from V_r dilutes the DCMU to about 9 µM. For exactly 10 µM, make DCMU-TAPP with 16.5 µL stock per 15 mL, and vehicle-TAPP with 49.5 µL ethanol per 45 mL.
3. **Why one batch:** One weighing split into aliquots gives every day and every experiment block, including the later dark + DCMU control, the same dose. Separate weighings would add dose variation between days, and day is the replicate. Sealed aliquots at −20 °C should keep for a few months; DCMU is chemically stable, so mass loss (evaporation) is the check.
4. **Why flush with DCMU-TAPP:** DCMU partitions into PDMS. Flushing with DCMU-TAPP pre-equilibrates the device and stops leftover BSA or plain media from lowering the dose.
5. **White PPFD:** The white condition has a higher total PPFD than the red conditions. The total PPFD can be recovered from the light calibration data. Because the acquisition light is the same in all conditions, image contrast and tracking are directly comparable.
6. **Pre-exposure:** Light separation exposes all cells to strong white light (80–100 µmol m⁻² s⁻¹) before the experiment. This is identical across conditions, but early time points may still carry a transient from it.
7. **Planned control:** Dark + DCMU is planned as a later DCMU-only control.
8. **Safety:** DCMU is toxic. Handle it with gloves and dispose of DCMU media as chemical waste.
9. **Residues:** DCMU absorbs into plastics and PDMS and is active at sub-µM concentrations. Discard everything that touched DCMU: the stock tube, media tubes, tips, the DCMU devices, their tubing and syringes. Never return any of it to shared use or to the device cleaning cycle.
