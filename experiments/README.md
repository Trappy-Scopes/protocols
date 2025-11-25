## Experiment protocols



## Selection of swimmers :: [current protocol](./selectswimmers.md)

This is aapted from a few different literature sources. However, the bulk of the calculation is adapted from Baumchen 2025.[^baumchen2025]:

### Settling by centrifugation

The cell culture is centrifuged to force the cells to settle at the bottom. Then, the cells are incubated in light to let the small fast swimmers separate from the rest of the culture by swimming to the top. The time and accelaration of centrifugation is determined by Stoke's law based on the terminal velocity $v$:


$$
v = \frac{2}{9}\frac{\rho_{cell} - \rho_{fluid}}{\mu}aR_{cell}^2 = 0.19\ \frac{mm}{s}
$$


given the $\rho_{cel}l − \rho_{fluid} \approx 50 kg/m^3$; the viscosity of the fluid $\mu \approx 1mPa\cdot s$, $R_{cell} \approx 3.5 \mu m$, which is the diamter of the smaller cells with the median $\tilde{R}_{cell} \approx 5.5 \mu m$ (at 1000 hours, obtained from Coulter counter experiments); and $a=200g$ (fixed). Based on the terminal speed, the time taken by cells to settle down can be calculated using the height of the :

For a standard $50mL$ centrifuge conical tube (Sarstedt), and different culture volumes, the height of the liquid columns are as follows (measures):

| Volume (mL) | Height (mm) | Time to settle (minutes and seconds) @200g |
| ----------- | ----------- | ------------------------------------------ |
| 10          | 28          | 2"27'                                      |
| 15          | 38          | 3"20'                                      |
| 20          | 46          | 4"2'                                       |
| 25          | 55          | 4"49'                                      |
| 30          | 64          | 5"36'                                      |
| 40          | 80          | 7"1'                                       |
| 45          | 90          | 7"53'                                      |

**Result 1**:  small bacth cultures, i.e. with volumes of $15-20 mL$, a centrifugation time of **10 minutes** is sufficent and a conservative estimate to ensure that all the cells (the smallest to the largest) settle down. The centrifugation acceleration of $200g$ has been checked to ensure that the cells (CC125 WT strain) can endure it.

```
1"10'
1"35'
1"55'
2"17'
2"40'
3"20'
3"45'
```

### Separation by light exposure

We rely on the phototactic nature of the cells to separate small fast swimmers from old large cells. Fast cells typically have a speeds of $80-200 \mu m/s$. Using the lower estimate of $v_{fast} \approx 80 \mu m/s$, we can calculate the time taken for the cells to reach the top, assuming the cells exhibit directed photoactic swimming. We also assume an upper limit for slow cells to be $v_{slow} \approx 40 \mu m/s$.

| Volume (mL) | Height (mm) | Time to swim up  for $v_{fast}$ | Time to swim up  for $v_{slow}$ |
| ----------- | ----------- | ------------------------------- | ------------------------------- |
| 10          | 28          | 0"35'                           | 1"10'                           |
| 15          | 38          | 0"47'                           | 1"35'                           |
| 20          | 46          | 0"57'                           | 1"55'                           |
| 25          | 55          | 1"8'                            | 2"17'                           |
| 30          | 64          | 1"20'                           | 2"40'                           |
| 40          | 80          | 1"40'                           | 3"20'                           |
| 45          | 90          | 1"52'                           | 3"45'                           |

A time window between the last two columns must be chosen for an effective isolation of fast swimmers. This calculation does not take into account the undirected motion of the cell, and also the finite volume ($0.5 - 1.5 mL$) isolated from the top.



[baumchen2025]: Catalan, R. E., Fragkopoulos, A. A., Girot, A., Lorenz, M. & Bäumchen, O. Preparation, maintenance and propagation of synchronous cultures of photoactive Chlamydomonas cells. *Nat Protoc* 1–26 (2025) doi:[10.1038/s41596-024-01135-3](https://doi.org/10.1038/s41596-024-01135-3)]

