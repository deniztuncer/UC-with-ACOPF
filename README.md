# UC-with-ACOPF

This text file contains information about the Unit Commitment problem with Alternating Current (AC) Power Flows instances that are created by Deniz Tuncer and Burak Kocuk, from Sabanci University.

Each generator is randomly assigned one out of three types. According to their types, we assign ramp up/down rates, minimum up/down times, startup cost, and fixed generation cost.

For buses, we randomly assign a real demand profile out of three profiles whereas for the reactive demand follows a single reactive demand profile. 

For demand profiles, we assume that peak demand of the demand profile is equal to the demand of the AC OPF instance and normalize the demand accordingly.


For each generator type, parameters are calculated as follows:

Type 1 Generator
	RampUpRate = RampDownRate = max ( Pmin, Pmax/2 )
	MinUp = MinDw = 2
	
Type 2 Generator
	RampUpRate = RampDownRate = max ( Pmin, Pmax/3 )
	MinUp = MinDw = 3

Type 3 Generator
	RampUpRate = RampDownRate = max ( Pmin, Pmax/4 )
	MinUp = MinDw = 4

For the fixed and startup cost of generator, we make them dependent to the linear production cost of generator, which is present in the Pglib-OPF and NESTA instances.

	FixedCost = 5 * LinearCost
	StartUpCost = 100 * LinearCost

For buses, there are three real demand profiles as follows:

	profile1 = [0.68, 0.64, 0.61, 0.60, 0.60, 0.62, 0.67, 0.74, 0.80, 0.84, 0.89, 0.92, 0.94, 0.95, 0.97, 0.99, 1, 0.96, 0.96, 0.92, 0.92, 0.88, 0.78, 0.76]

	profile2 = [0.67, 0.63, 0.6, 0.59, 0.59, 0.6, 0.74, 0.86, 0.95, 0.96, 0.96, 0.95, 0.95, 0.95, 0.93, 0.94, 0.99, 1, 1, 0.96, 0.91, 0.83, 0.73, 0.63]

	profile3 = [0.57, 0.64, 0.68, 0.71, 0.75, 0.78, 0.82, 0.85, 0.88, 0.92, 0.97, 1, 0.92, 0.88, 0.85, 0.78, 0.71, 0.78, 0.85, 0.92, 0.85, 0.78, 0.71, 0.64]

The reactive demand profile is as follows:

	profile = [0.684375, 0.645108696, 0.619836957, 0.604483696, 0.605706522, 0.626902174, 0.677309783, 0.69375, 0.729755435, 0.808423913, 0.893070652, 0.922282609, 0.946059783, 0.951494565, 0.972146739, 0.999184783, 1, 0.963858696, 0.960869565, 0.927173913, 0.927038043, 0.908831522, 0.765353261, 0.763994565]


In the txt files, we provide the generator types and the bus types, for the instances associated with the PGLib-OPF.

The instances are created based on PGLib for OPF, which can be accessed at:
https://github.com/power-grid-lib/pglib-opf

The instances created according to this procedure can be accessed at:
https://sites.google.com/site/burakkocuk/research

The associated paper can be accessed at:
https://arxiv.org/abs/2201.01496
