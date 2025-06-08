## A consise Protein-ligand Moelcular Dynamic Simulation Workflow

It is another workfolw for a normal protein-ligand simulation, try to keep it simple. 

The idea is try to use as less packages as possible.


* Core MD Engine  
  - `openmm` (GPU-accelerated MD)  
  - `openmmforcefields` (Force field handling)  
  - `pdbfixer` (Structure preparation)  
  - `PyMOL` (Structure preparation/visualization/Analysis)  

* Parameterization for small molecules  
  - `openff-toolkit` (SMIRNOFF force fields)  

* Environment  
  - `colabconda` (Package management in Colab)  

* NOT USED 
 * `Ambertools` (Alternative to OpenFF pipeline)  
 * `rdkit` (Chemical informatics - replaced by OpenFF)

![image](https://github.com/user-attachments/assets/05735a11-c1b0-4017-bd8c-4b549f53c6e5)
