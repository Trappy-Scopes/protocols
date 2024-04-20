---
author: Camila Costa
editor: Yatharth Bhasin
description: This describes the processes to inoculate Petri plates with Chlamydomonas: the agar solution for the medium, the Petri plates preparation, and how to streak them up with cells.
attribution: [https://www.hispanagar.com/en/why-agar-used-microbiology, 
https://agargel.com.br/en/agar-agar/]
related protocols: ./inoculation/streaking_agar_plates.md 
---

# Protocol for preparation of agar plates



## Overview

1. Preparation of agar solution
2. Preparation of petri plates



## 1. Preparation of agar solution

1. Add **1.5 %** (w/v) of agar to **~ 300 mL** of TAP (weight the agar powder on a beaker and then add the TAP).
2. Mix with a magnetic stirrer with no heating. The dissolution will be done *a posteriori*, before filling the Petri plates.
3. Store the solution in a glass bottle, not completely full to allow for liquid expansion during the posterior melting.
4. Label(a) and send to autoclave (for **20 min**, at **121 ºC**), with no water bath (see below).
5. Collect from the autoclave and store at room temperature. 



## 2. Petri plates preparation

1. Melt small volumes (**~ 300 mL**) of agar containing TAP in the microwave (around **4 min** in total). Very importantly, the bottle lid must be twisted, leaving the bottle unsealed (but not open), otherwise it may explode.

	```exp.user_prompt(auto_name); exp.delay("microwave", 4*60)```

2. After a while (**1-2 min**), check the solution for solid material, and slowly agitate it, holding the bottle and making small circles in the air (use gloves!). The solution might expand due to overeating of the liquid fraction, so the agitation must be done with care.

	```exp.user_prompt("cooldown process"); exp.delay("cooldown", 2*60)```

3. Heat the solution until no more solid material is present (it should look translucid with a brownish colour).

	```exp.time_task("heating")```

4. Pour the solution in 25 mL Petri plates, until all the liquid portions are joined together, covering the whole plate base (approximately half plate height).

	```exp.time_task("pour")```

5. Do not dispose the plates on top of each other, to reduce condensation effects. Leave them at room temperature. After some time, once the agar is solid, they can be stored (see Fig. 1 below).

	```exp.confirm("done")```

## Figures

<img src="/Users/byatharth/code/yatharthb97.github.io/static/images/classnotes/image-20240420125927015.png" alt="image-20240420125927015" style="zoom:10%;" /> 	Figure 1: Stored, solidified agar plates.



<img src="/Users/byatharth/code/yatharthb97.github.io/static/images/classnotes/image-20240420125952165.png" alt="image-20240420125952165" style="zoom:10%;" />     Figure 2: Inoculated agar plates.



<img src="/Users/byatharth/code/yatharthb97.github.io/static/images/classnotes/image-20240420130026103.png" alt="image-20240420130026103" style="zoom:20%;" />      Figure 3: Scheme of the streaking path.



## Additional information

1. *Agar solutions are commonly used in culture media, due to its chemico-physical properties: melting point of 85-95 ºC, setting point of 32-45 ºC, it’s insoluble in cold water but easily dissolved in boiling water, with a very high absorbance (up to 20 times its weight), setting as a firm gel at very low concentrations. In its dry state, it’s aseptic, being mixed with nutrients to create the perfect environment for a certain organism development.*

2. *Note: It should be avoided to expose agar solutions to high temperatures and pH <* *6.0 for long periods.*

