## A consise Protein-ligand Moelcular Dynamic Simulation Workflow


![image](https://github.com/user-attachments/assets/05735a11-c1b0-4017-bd8c-4b549f53c6e5)

<a target="_blank" href="https://colab.research.google.com/github/quantaosun/ACPLMD/blob/main/notebook/A_consise_Protein_ligand_Moelcular_Dynamic_Simulation_Workflow.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

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

### Analysis

In the case that ligand is out of pocket due to PBC after the simulation, vmd can be used to wrap them, in `tk console` of vmd
   
```bash
mol new prod_final.pdb  
mol addfile prod.dcd
pbc wrap -compound res -all  # Wraps residues, not atoms
animate write dcd prod_wrapped.dcd
```
Load the `prod_final.pdb` and `prod_wrapped.dcd` to pymol should be fine.


Publications
If you use OpenMM for scientific research, please cite it.

Primary Publication:

Peter Eastman, Raimondas Galvelis, Raúl P. Peláez, Charlles R. A. Abreu, Stephen E. Farr, Emilio Gallicchio, Anton Gorenko, Michael M. Henry, Frank Hu, Jing Huang, Andreas Krämer, Julien Michel, Joshua A. Mitchell, Vijay S. Pande, João PGLM Rodrigues, Jaime Rodriguez-Guerra, Andrew C. Simmonett, Sukrit Singh, Jason Swails, Philip Turner, Yuanqing Wang, Ivy Zhang, John D. Chodera, Gianni De Fabritiis, and Thomas E. Markland. "OpenMM 8: Molecular Dynamics Simulation with Machine Learning Potentials." J. Phys. Chem. B 128(1), pp. 109-116 (2023). DOI: 10.1021/acs.jpcb.3c06662
