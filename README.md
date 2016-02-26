# readsmart
A python package for reading and parsing i/o files related to the SMART model 

# examples

```python
# Import readsmart package 
import readsmart as rs

# Specify file locations
atm_file = 'icrccm_62.atm'
rad_file = 'earth_standard_hitran08_50_100000cm-1_clearsky_toa.rad'

# Plot atm
rs.atm(atm_file, skiprows=11)
```
<img src="https://github.com/jlustigy/readsmart/blob/master/example_files/plots/example_atm.png" width="100%" height="100%" align="middle" />

```python
# Plot flux
rs.rad(rad_file, plot=True, getdata=False)
```
<img src="https://github.com/jlustigy/readsmart/blob/master/example_files/plots/example_rad1.png" width="50%" height="50%" align="middle" />

```python
# Plot radiance streams
rs.rad(rad_file, plot=True, getdata=False, ptype='rad', xran=[1.0,15])
```
<img src="https://github.com/jlustigy/readsmart/blob/master/example_files/plots/example_rad2.png" width="50%" height="50%" align="middle" />

```python
# Specify jacobian file extension tag
jext = '.j_O3'
# Plot Radiance Jacobians
rs.jacobians(rad_file, jext, plot=True, getdata=False, xran=[3.0,5.0], pran=[100.,10000.])
```
<img src="https://github.com/jlustigy/readsmart/blob/master/example_files/plots/example_jacobians.png" width="100%" height="100%" align="middle" />
