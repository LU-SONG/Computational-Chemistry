# <center> <font color=black>脚本功能及使用方法
---
## python脚本(2024)

|-脚本名称-|-功能-|-使用方法-|
|----------|----------|----------|
|add_H2O.py|Add H2O to the slab.|python3 add_H2O.py|
|add_site_ads.py|Add different adsorbed molecules onto a crystal surface and determine the adsorption position and method based on user input parameters.|python3 add_site_ads.py -h|
|bader2pqr.py|transfer bader output to pgr file for VMD visualization.|python3 bader2pqr.py|
|ck-multi.py|manage and evaluate the completion status of tasks in directories and output the results in a table format.|python3 ck-multi.py -multi_job.pbs|
|d-band.py|extract and evaluate the d-band center energy from VASP calculation results.|python d-band.py|
|DOS_plot.py|plot the projected density of states (PDOS) from data and save the figure.|python DOS_plot.py|
|eps2jpg.py|convert an EPS file to a high-resolution PNG image.|python eps2png.py|
|fix_slab.py|fix the slab in POSCAR.|python3 fix_slab.py -The number of atoms you want to fix.|
|get_cp.py|data to a quadratic polynomial and calculate related statistical quantities.|python get_cp.py|
|get_db.py|store the calculated crystal structure data into a SQLite database.|python get_db.py|
|get_dimer.py|Extract vibrational mode information from a OUTCAR file and add it to a new POSCAR_dimer file for dimer (two-molecule) calculations.|python get_dimer.py|
|neighbor_multi_atoms.py|Calculate and analyze the neighboring atoms of a specified atom in the crystal structure , generate a Markdown formatted table to display the neighboring atoms.|python neighbor_multi_atoms.py -filename -central_atom_index -cutoff|
|out_view.py|Read the crystal structure data from the CONTCAR file and use the matplotlib library to generate top views and two side views (XZ and YZ planes) of the atomic structure.|python out_view.py|
|pos2arc.py|transfer POSCAR to .arc or transfer .arc to POSCAR.|python pos2arc.py -pos2arc/-arc2pos|
|RDF.py|Read data from a Radial Distribution Function (RDF) data file, calculate the average RDF, and plot the RDF graph.|python RDF.py|
|revise_boundary_length.py|Revise boundry atoms view.|Python revise_boundary_length.py filename|
|sort_poscar_atoms.py| sort the same elements in POSCAR.|python sort_poscar_atoms.py|
|vector2ort.py|Converted cells into orthorhombic system|python vector2ort.py|
----
## shell脚本（2024）

|-脚本名称-|-功能-|-使用方法-|
|----------|----------|----------|
|bader.sh|Perform Bader charge analysis of the charge density around atoms to obtain the valence electron count of the atoms.|bader.sh|
|checkinput.sh|get energy and force from OUTCAR/OSZICAR |checkinput.sh|
|checkpospot.sh|Check for VASP input files POSCAR and POTCAR in the current directory and its subdirectories.|checkpospot.sh|
|correct_H.sh|Traverse the current directory and its subdirectories, looking for VASP calculation result files OUTCAR, and use the vaspkit tool to calculate the thermodynamic correction value (deltaG).|correct_H.sh|
|correct-cp2k.sh|Traverse the current directory and its subdirectories, looking for CP2K calculation result files cp2k.out, and use a tool called Shermo to calculate the thermodynamic correction value (deltaG).|correct-cp2k.sh|
|CP2K_OUTPUT_save.sh|Extract the execution time and computation duration from a CP2K calculation result file named cp2k.out, then create a new backup folder based on this information, and copy the relevant CP2K input and output files into this folder.|CP2K_OUTPUT_save.sh|
|fix_all_slab.sh|Batch execute the Python script fix_slab.py.|fix_all_slab.sh|
|g16_out2gjf.sh|Convert geometry (final, input orientation) in all Gaussian .out files in current folder to .gjf file by Multiwfn|g16_out2gjf.sh|
|get_force.sh|eliminate forces of fixed atoms|get_force.sh -fix_value|
|get_hol_ele_cub.sh| generate three different cube files (hole.cub, electron.cub, and CDD.cub), and rename them to include a serial number in the file name.|get_hol_ele_cub.sh|
|incar_modi.sh|Find all lines containing IDIPOL=3 in the INCAR file and comment out these lines.|incar_modi.sh|
|kpoints.sh|To generate KPOINTS file|kpoints.sh  3 3 1|
|mk_pwdfreq.sh|Prepare and modify input files for VASP calculations.|mk_pwdfreq.sh|
|mkfreq.sh|Prepare and modify input files for VASP calculations, and organize all related files into a temporary directory.|mkfreq.sh|
|mk-pbs.sh|Generate job submission scripts (sub.pbs) for different computational tasks, which are used to submit jobs on high-performance computing clusters.|mk-pbs.sh|
|multi_qsub48.sh|Batch modify the NCORE parameter in the INCAR files of all subdirectories under the current directory, setting it to 12, then copy a PBS job submission script named multisub48.pbs to the current directory, and submit the script using the qsub command.|multi_qsub48.sh|
|multi_qsub56.sh|Batch modify the NCORE parameter in the INCAR files of all subdirectories under the current directory, setting it to 14, then copy a PBS job submission script named multisub56.pbs to the current directory, and submit the script using the qsub command.|multi_qsub56.sh|
|pos2potall.sh|Batch generate POTCAR in all subdirectories|pos2potall.sh|
|potall.sh|Batch generate POTCAR in all subdirectories|potall.sh|
|potcar.sh|Rename the old POTCAR to old-POTCAR, and look for POTCAR files matching the command-line arguments from the specified pseudopotential repository path, then concatenate them into the POTCAR file in the current directory.|potcar Cu C H O|
|q48.sh|Check the NCORE parameter in INCAR and submit the 48kgz.pbs job script to the job scheduling system.|q48.sh|
|q56.sh|Check the NCORE parameter in INCAR and submit the 56kgz.pbs job script to the job scheduling system.|q56.sh|
|qsuball.sh|Iterate through all subdirectories in the current directory and execute the qsub command in each subdirectory to submit all .pbs files as jobs.|qsuball.sh|
|save+zip_all_OUTPUT.sh|Copy the VASP calculation related files (CONTCAR, INCAR, KPOINTS, OSZICAR, OUTCAR, POTCAR) from all the first-level subdirectories in the current directory to a temporary directory, then pack these files into a ZIP file, and finally delete the temporary directory.|save+zip_all_OUTPUT.sh|
|save+zip_OUTPUT.sh|Copy the CONTCAR files from all the first-level subdirectories in the current directory to a temporary directory, then pack these files into a ZIP file, and finally delete the temporary directory.|save+zip_OUTPUT.sh|
|scpfiles2cfff.sh|Use the scp command via SSH to copy files or directories from the local machine to a remote server, and handle any interactive prompts that may appear.|scpfiles2cfff.sh -path|
|ta.sh|Get energy and force from OUTCAR/OSZICAR|ta.sh or ta.sh -g|
