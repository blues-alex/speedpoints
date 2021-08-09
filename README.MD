## SpeedSpectra.
* Use json files, to control the device, with fields:
    - time - time duration of spectr in quants (one quant equal 50 milliseconds)
    - channels - list of channels values in range 300 - 4096 (for confident switching on of the diode, the minimum recommended value is 300)
* File format:
``` json
[{
    "time": 23,
    "channels": [1540, 1293, 2647, 3954, 1697, 3059, 651, 383, 2300, 830, 2227, 1847, 3863, 3241, 2124, 347]
}, {
    "time": 268,
    "channels": [4070, 446, 1815, 1363, 1388, 3466, 1757, 2187, 1779, 2323, 327, 1487, 3504, 2868, 3485, 3778]
}, {
    "time": 5000,
    "channels": [1929, 2586, 1801, 1579, 3395, 2053, 1485, 1587, 2828, 3363, 717, 961, 1834, 2703, 1496, 3741]
}, {
    "time": 241,
    "channels": [923, 2268, 2892, 2339, 524, 810, 3817, 3380, 1617, 384, 3367, 2105, 579, 2245, 1981, 3502]
}, {
    "time": 43,
    "channels": [3119, 2839, 3258, 3103, 1143, 702, 1268, 1468, 3794, 2376, 968, 3994, 3594, 1127, 678, 3138]
}, {
    "time": 227,
    "channels": [769, 1486, 3119, 1545, 2287, 2604, 3614, 451, 606, 798, 1966, 3545, 2078, 752, 1663, 2771]
}]
```
## Starting application.
* Application takes two parameters:
    - Port "-p" - default use /dev/ttyUSB0
    - Json file with spectra and time "-s" - default ./spectra.json
``` sh
$~ ./SpeedSpectra -p /dev/ttyUSB2 -s ./my_spectra.json
```