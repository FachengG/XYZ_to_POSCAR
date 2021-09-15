# Purpose
This script is designed for the purpose: transfer a molecule from xyz into POSCAR. Please put the box information in the second line of xyz file (learn more at "input xyz file example" section). If the box is not defined, a default 100x100x100 box will be used. 
When using it trnasfer 3D/2D material from xyz to POSCAR, be careful. 
## Feature
1. The molecule recentered at the box's center.
2. Transfer multi xyz files to POSCAR files at one time.
3. No need for install any python library. 
4. Easy to use.
# How to use the code:
1. Put the xyz files in the same folder with this script.
2. Run:
```
python3 xyz_to_POSCAR.py
```
The POSCAR files with Cartesian coordinates will be generated in the folder.
# Input xyz file format:
```
<number of atoms>
[x1,y1,z1,x2,y2,z2,x3,y3,z3] # Define of the box
<element> <X> <Y> <Z>
...
```
# Example:
### xyz input:
```
3
[60,0,0,0,40,0,0,0,50]
C 10 10 10
O 1 1 1
O 21 21 21
```
### POSCAR output:
```
Input file generated from example.xyz
1.0
 60.0 0.0 0.0
 0.0 40.0 0.0
 0.0 0.0 50.0
 C O
 1 2
Cartesian
  29.333333333333336  19.333333333333336  24.333333333333336
  20.333333333333336  10.333333333333334  15.333333333333334
  40.333333333333336  30.333333333333336  35.333333333333336
```
