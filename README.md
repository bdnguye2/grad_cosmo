# COSMO
Addressing the research question: Is the outlying charge error 
significant in the gradient calculations? Is the outlying charge 
correction enough to remedy the issue?

TODO: Develop a set of molecules to test the error (Jenny and Matthew)
* Made a directory called benchmark with a file for unoptimized anions
containing both small(less than 50 atoms) and large(bigger than 50 atoms)
anions

TODO: Decide on the COSMO parameters to test (Matthew)
* Dft
	- grid 5
	- func pbe0
	- weight derivatives
* stepsize .001
* scfconv 6
* denconv 1d-7
* rij
* def2-SVP

cosmo parameters:
* nppa 1082
* nspa 92 
* dielectric constant 80 (water)
 
chose these parameters to maintain consistancy with the ground state calculations.
 However the basis set was changed to be stronger

TODO: Compute the outlying charge error (Jenny and Matthew)

* Determine the converged single point energy calculations for each molecule
with the given parameters
* Read, understand, and, if necessary, modify the NumForce script to compute
the gradients (dE/dxyz) with COSMO
* Determine the significance of the outlying charge error
