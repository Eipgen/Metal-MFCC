# Metal-MFCC

## Description 

Metal molecular fractionation with conjugate caps (Metal-MFCC) approach is developed for efficient linear-scaling quantum calculation of potential energy and atomic forces of metalloprotein. In this approach, the potential energy of a given protein is calculated by a linear combination of potential energies of the neighboring residues, two-body interaction energy between non-neighboring residues that are spatially in close contact and the potential energy of the metal binding group. The calculation of each fragment is embedded in a field of point charges representing the remaining protein environment.

## Metal-MFCC for protein 
![cover image](./Metal-MFCC_protein.png)
## Metal-MFCC for Metalloprotein 
![cover image](./Metal-MFCC_1aay.png)


## install
```
# suppose you install intelmpi
module load intel/2023.0.0
module load intel/impi/2021.8.0
module load mkl
mpif90  -Wall *.F90 -o metal-mfcc.x
```
## usage 
```
# generate the frag
./metal-mfcc.x <input

# run g16 job and compute the log file

./metal-mfff.x <input
# you can find results in mfcc.out
cat mfcc.out
```


## Reference:
* Xu, M.;  Zhu, T.; Zhang, J. Z. H., A Force Balanced Fragmentation Method for ab Initio Molecular Dynamic Simulation of Protein. Front. Chem. 2018, 6, 189.
* Xu, M.;  He, X.;  Zhu, T.; Zhang, J. Z. H., A Fragment Quantum Mechanical Method for Metalloproteins. J. Chem. Theory Comput. 2019, 15 (2), 1430-1439.
