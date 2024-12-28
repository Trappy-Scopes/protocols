
# Protocol for selecting swimmers

Selection of swimmers from a batch culture of CR is performed to get a low density of cells which have both flagella intact, i.e. good swimmers.

Preferably, this procedure should be done after 2 hours of the beginning of the light cycle.


## Requirements

1. Cell culture of CR
2. White vials with lids
3. Fresh media (Blue bottles)
4. (optional) Ballast for centrifuge
5. Centrifuge
6. Enclosure with strong light on the top



## Procedure

0. Select cultures that are in the log growth phase: 6th day or 10^6 cells per mL.
1. Place the cell culture in the centrifuge and spin at 500rcf for 10mins at 25ºC.
	

	```python
	exp.delay("Centrifugation", 10*60)
	```
2. After the centrifugation finishes, carefully bring the tubes to the bench and replace the caps with parafilm.
3. Place the culture tubes in an enclosure with strong white light for 30 mins.
4. After this is done, isolate 35% of the cell culture into broad lid vials (Vss). The following table can be used to get the correct volume/densities:
    | Volume (mL) | 35% Volume (mL)  | 40% Volume (mL) |
    |-------------|------------------|-----------------|
    | 1           | 0.35             | 0.4             |
    | 1.5         | 0.525            | 0.6             |
    | 2           | 0.7              | 0.8             |
    | 6           | 2.1              | 2.4             |
    | 7           | 2.45             | 2.8             |
    | 8           | 2.8              | 3.2             |
    | 9           | 3.15             | 3.6             |
    | 10          | 3.5              | 4.0             |
    | 12          | 4.2              | 4.8             |
    | 15          | 5.25             | 6.0             |
    | 16          | 5.6              | 6.4             |
    | 17          | 5.95             | 6.8             |
    | 18          | 6.3              | 7.2             |
    | 19          | 6.65             | 7.6             |
    | 20          | 7.0              | 8.0             |

5. The density of these cultures should be around 10^5 cells per mL. The culture can be further diluted by addition of fresh media to about 5X10^5 cells.

​	You can use the formula: C1V1 = C2V2 and Vadd = V2 - Vss

6. The culture is ready for use. Its done.