# Solver 

The solver is the main object of VOSP. It takes different parameters listed below.

| Parameter | Description |
|---------|---------|
| DT     | time step     |
| end time     | the simulation will run until the time reaches end_time      |
| LX     | Length of the simulation     |
| NX     | Number of points in the spatial direction     |
| NV     | Number of points in the velocity direction     |
| lambda     | Length of simulation divided by lambda debye     |
| Save every N iteration     | The solver will save the potential and the species data in an h5 file every N iteration      |
