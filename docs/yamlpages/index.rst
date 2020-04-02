.. _yaml_head:

YAML Files for Simulation
#########################

YANK now supports setting up entire simulations with easy to read and write `YAML files <http://www.yaml.org/about.html>`_.
No longer do you need to remember long command line arguments with many ``--`` flags, you can just write a
``yank.yaml`` file and call ``yank script --yaml=yank.yaml`` to carry out all your preparation and simulations.
Below are the valid YAML options. We also have example YANK simulations which use YAML files to run.

To see examples and some of the recommended stock settings, check out the :doc:`cookbook`! To see *all* options
available to the YAML scripts: check out the detailed list below.

All Pages
---------

.. toctree::
   :maxdepth: 1

   options <options>
   molecules <molecules>
   solvents <solvents>
   systems <systems>
   mcmc <mcmc>
   samplers <samplers>
   protocols <protocols>
   experiments <experiments>
   Combinatorial Options <combinatorial>
   YAML Versions <version>
   cookbook

Detailed Options List
---------------------
* :doc:`options <options>`

  * :ref:`General Options: <yaml_options_options>`

    * :ref:`verbose <yaml_options_verbose>`
    * :ref:`resume_setup <yaml_options_resume_setup>`
    * :ref:`resume_simulation <yaml_options_resume_simulation>`
    * :ref:`output_dir <yaml_options_output_dir>`
    * :ref:`setup_dir <yaml_options_setup_dir>`
    * :ref:`experiments_dir <yaml_options_experiments_dir>`
    * :ref:`platform <yaml_options_platform>`
    * :ref:`precision <yaml_options_precision>`
    * :ref:`max_n_contexts <yaml_options_max_n_contexts>`
    * :ref:`switch_experiment_interval <yaml_options_switch_experiment_interval>`
    * :ref:`processes_per_experiment <yaml_options_processes_per_experiment>`

  * :ref:`System and Simulation Prep <yaml_options_sys_and_sim_prep>`

    * :ref:`randomize_ligand <yaml_options_randomize_ligand>`
    * :ref:`randomize_ligand_sigma_multiplier <yaml_options_randomize_ligand_sigma_multiplier>`
    * :ref:`randomize_ligand_close_cutoff <yaml_options_ligand_close_cutoff>`
    * :ref:`temperature <yaml_options_temperature>`
    * :ref:`pressure <yaml_options_pressure>`
    * :ref:`hydrogen_mass <yaml_options_hydrogen_mass>`
    * :ref:`constraints <yaml_options_constraints>`

  * :ref:`Simulation Parameters: <yaml_options_simulation_parameters>`

    * :ref:`switch_phase_interval <yaml_options_switch_phase_interval>`
    * :ref:`minimize <yaml_options_minimize>`
    * :ref:`minimize_max_iterations <yaml_options_minimize_max_iterations>`
    * :ref:`minimize_tolerance <yaml_options_minimize_tolerance>`
    * :ref:`number_of_equilibration_iterations <yaml_options_number_of_equilibration_iterations>`
    * :ref:`equilibration_timestep <yaml_options_equilibration_timestep>`
    * :ref:`default_number_of_iterations <yaml_options_default_number_of_iterations>`
    * :ref:`default_nsteps_per_iteration <yaml_options_default_nsteps_per_iteration>`
    * :ref:`default_timestep <yaml_options_default_timestep>`
    * :ref:`checkpoint_interval <yaml_options_checkpoint_interval>`
    * :ref:`store_solute_trajectory <yaml_options_store_solute_trajectory>`
    * :ref:`constraint_tolerance <yaml_options_constraint_tolerance>`
    * :ref:`yaml_options_anisotropic_dispersion_cutoff`

  * :ref:`Alchemy Parameters <yaml_options_alchemy_parameters>`

    * :ref:`annihilate_electrostatics <yaml_options_annihilate_electrostatics>`
    * :ref:`annihilate_sterics <yaml_options_annihilate_sterics>`
    * :ref:`softcore_alpha <yaml_options_alchemical_sterics>`
    * :ref:`softcore_beta <yaml_options_alchemical_electrostatics>`
    * :ref:`softcore_a <yaml_options_alchemical_sterics>`
    * :ref:`softcore_b <yaml_options_alchemical_sterics>`
    * :ref:`softcore_c <yaml_options_alchemical_sterics>`
    * :ref:`softcore_d <yaml_options_alchemical_electrostatics>`
    * :ref:`softcore_e <yaml_options_alchemical_electrostatics>`
    * :ref:`softcore_f <yaml_options_alchemical_electrostatics>`
    * :ref:`alchemical_pme_treatment <yaml_options_alchemical_pme_treatment>`
    * :ref:`disable_alchemical_dispersion_correction <yaml_options_disable_alchemical_dispersion_correction>`
    * :ref:`split_alchemical_forces <yaml_options_split_alchemical_forces>`

* :doc:`molecules <molecules>`

  * :ref:`Specifying Molecules <yaml_molecules_specify_names>`

    * :ref:`filepath <yaml_molecules_filepath>`
    * :ref:`smiles <yaml_molecules_smiles>`
    * :ref:`name <yaml_molecules_name>`
    * :ref:`strip_protons <yaml_molecules_strip_protons>`
    * :ref:`pdbfixer <yaml_molecules_pdbfixer>`
    * :ref:`modeller <yaml_molecules_modeller>`
    * :ref:`select <yaml_molecules_select>`

  * :ref:`Assigning Missing Parameters <yaml_molecules_assign_charges>`

    * :ref:`antechamber <yaml_molecules_antechamber>`
    * :ref:`openeye <yaml_molecules_openeye>`

  * :ref:`Assigning Extra Information <yaml_molecules_extras>`

    * :ref:`leap <yaml_molecules_leap>`
    * :ref:`epik <yaml_molecules_epik>`
    * :ref:`regions <yaml_molecules_regions>`

* :doc:`solvents <solvents>`

  * :ref:`OpenMM System Creation Options <yaml_solvents_openmm_system_options>`

    * :ref:`nonbonded_method <yaml_solvents_nonbonded_method>`
    * :ref:`nonbonded_cutoff <yaml_solvents_nonbonded_cutoff>`
    * :ref:`switch_distance <yaml_solvents_switch_distance>`
    * :ref:`rigid_water <yaml_solvents_rigid_water>`
    * :ref:`implicit_solvent <yaml_solvents_implicit_solvent>`
    * :ref:`implicit_solvent_salt_conc <yaml_options_implicit_solvent_salt_conc>`
    * :ref:`solute_dielectric <yaml_options_solute_dielectric>`
    * :ref:`solvent_dielectric <yaml_options_solvent_dielectric>`
    * :ref:`ewald_error_tolerance <yaml_options_ewald_error_tol>`

  * :ref:`LEaP Solvation Options <yaml_solvents_LEaP_options>`

    * :ref:`clearance <yaml_solvents_clearance>`
    * :ref:`positive_ion <yaml_solvents_positive_ion>`
    * :ref:`negative_ion <yaml_solvents_negative_ion>`
    * :ref:`ionic_strength <yaml_solvents_ionic_strength>`

* :doc:`systems <systems>`

  * :ref:`Ligand/Receptor Free Energies Setup by YANK <yaml_systems_receptor_ligand>`

    * :ref:`ligand <yaml_systems_receptor_ligand>`
    * :ref:`receptor <yaml_systems_receptor_ligand>`
    * :ref:`solvent <yaml_systems_receptor_ligand>`
    * :ref:`pack <yaml_systems_receptor_ligand>`
    * :ref:`leap <yaml_systems_receptor_ligand>`

      * :ref:`parameters <yaml_systems_receptor_ligand>`

  * :ref:`Hydration Free Energies Setup by YANK <yaml_systems_hydration>`

    * :ref:`solute <yaml_systems_hydration>`
    * :ref:`solvent1 <yaml_systems_hydration>`
    * :ref:`solvent2 <yaml_systems_hydration>`
    * :ref:`leap <yaml_systems_hydration>`

  * :ref:`Arbitrary Phase Free Energies Setup by User <yaml_systems_user_defined>`

    * :ref:`phase1_path <yaml_systems_user_defined>`
    * :ref:`phase2_path <yaml_systems_user_defined>`
    * :ref:`ligand_dsl <yaml_systems_user_defined>`
    * :ref:`solvent_dsl <yaml_systems_user_defined>`
    * :ref:`solvent <yaml_systems_user_defined>`
    * :ref:`gromacs_include_dir <yaml_systems_user_defined>`

* :doc:`mcmc_moves <mcmc>`

  * :ref:`MCMC Moves Syntax <yaml_mcmc_example>`

* :doc:`samplers <samplers>`

  * :ref:`Samplers syntax <yaml_samplers_example>`
  * :ref:`yaml_samplers_multistatesampler`

    .. note:: All options under here are global to the other samplers

    * :ref:`yaml_samplers_locality`

  * :ref:`yaml_samplers_repexsampler`

    * :ref:`yaml_samplers_replica_mixing_scheme`

  * :ref:`yaml_samplers_samssampler`

    * :ref:`yaml_samplers_state_update_scheme`
    * :ref:`yaml_samplers_gamm0`
    * :ref:`yaml_samplers_flatness_threshold`

  * :ref:`yaml_samplers_online_analysis_parameters`

    * :ref:`yaml_samplers_online_analysis_interval`
    * :ref:`yaml_samplers_online_analysis_target_error`
    * :ref:`yaml_samplers_online_analysis_minimum_iterations`

* :doc:`protocols <protocols>`

  * :ref:`Protocols Syntax <yaml_protocols_example>`

    * :ref:`alchemical_path <yaml_protocols_example>`

      * :ref:`lambda_electrostatics <yaml_protocols_alchemical_path>`
      * :ref:`lambda_sterics <yaml_protocols_alchemical_path>`

    * :ref:`Automatic alchemical path Generation <yaml_protocols_auto>`

  * :ref:`How-To Video <yaml_protocols_video>`

* :doc:`experiments <experiments>`

  * :ref:`Experiments Syntax <yaml_experiments_syntax>`

    * :ref:`system <yaml_experiments_syntax>`
    * :ref:`sampler <yaml_experiments_syntax>`
    * :ref:`protocol <yaml_experiments_syntax>`
    * :ref:`options <yaml_experiments_syntax>`
    * :ref:`restraint <yaml_experiments_syntax>`

  * :ref:`Running Multiple Experiments <yaml_experiments_syntax>`

* :doc:`version <version>`
