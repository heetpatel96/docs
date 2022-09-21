# RSTAB.LoadCasesAndCombinations package

## Submodules

## RSTAB.LoadCasesAndCombinations.designSituation module


### _class_ RSTAB.LoadCasesAndCombinations.designSituation.DesignSituation(no=1, design_situation_type=DesignSituationType.DESIGN_SITUATION_TYPE_A_ACCIDENTAL, active=True, name=None, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(no=1, design_situation_type=DesignSituationType.DESIGN_SITUATION_TYPE_A_ACCIDENTAL, active=True, name=None, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Design Situation Tag


    * **design_situation_type** (*enum*) – Design Situation Type Enumeration


    * **active** (*bool*) – Enable/Disable Design Situation Activity


    * **name** (*str**, **optional*) – User-Defined Name


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## RSTAB.LoadCasesAndCombinations.loadCase module


### _class_ RSTAB.LoadCasesAndCombinations.loadCase.LoadCase(no=1, name='Self-weight', self_weight=[True, 0.0, 0.0, 1.0], comment='Comment', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### _static_ StaticAnalysis(no=1, name='Self-weight', to_solve=True, analysis_settings_no=1, action_category=ActionCategoryType.ACTION_CATEGORY_PERMANENT_G, self_weight=[True, 0.0, 0.0, 10.0], comment='Comment', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Case Tag


    * **name** (*str*) – Load Case Name


    * **to_solve** (*bool*) – Enable/Disbale Load Case Solver Status


    * **analysis_settings_no** (*int*) – Analysis Settings Number


    * **action_category** (*enum*) – Action Category Enumeration


    * **self_weight** (*list*) – Self-weight Considerations
    for self-weight considerations;

    > self_weight = [True, self_weight_factor_x, self_weight_factor_y, self_weight_factor_z]

    for no self-weight considerations;

        self_weight = [False]



    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### \__init__(no=1, name='Self-weight', self_weight=[True, 0.0, 0.0, 1.0], comment='Comment', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Case Tag


    * **name** (*str*) – Load Case Name


    * **self_weight** (*list*) – Self-Weight Parameters
    self_weight = [self_weight_active, self_weight_factor_x, self_weight_factor_y, self_weight_factor_z]


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## RSTAB.LoadCasesAndCombinations.loadCombination module


### _class_ RSTAB.LoadCasesAndCombinations.loadCombination.LoadCombination(no=1, analysis_type=AnalysisType.ANALYSIS_TYPE_STATIC, design_situation=1, user_defined_name=[False], static_analysis_settings=1, consider_imperfection=False, consider_initial_state=False, structure_modification=False, to_solve=True, combination_items=[[1.5, 1, 0, False]], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(no=1, analysis_type=AnalysisType.ANALYSIS_TYPE_STATIC, design_situation=1, user_defined_name=[False], static_analysis_settings=1, consider_imperfection=False, consider_initial_state=False, structure_modification=False, to_solve=True, combination_items=[[1.5, 1, 0, False]], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Combination Tag


    * **analysis_type** (*enum*) – Analysis Type Enumeration


    * **design_situation** (*int*) – Design Situation


    * **user_defined_name** (*list*) – User defined Combination Name


    * **static_analysis_settings** (*int*) – Static Analysis Settings Number


    * **consider_imperfection** (*bool*) – Consider Imperfection Options


    * **consider_initial_state** (*bool*) – Consider Initial State


    * **structure_modification** (*bool*) – Enable/Disable Structure Modification


    * **to_solve** (*bool*) – Decide to solve


    * **combination_items** (*list of list*) – Combination Items
    for Combination Items;

    > combination_items = [[factor, load_case, action, is_leading],…]



    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## RSTAB.LoadCasesAndCombinations.modalAnalysisSettings module


### _class_ RSTAB.LoadCasesAndCombinations.modalAnalysisSettings.ModalAnalysisSettings(no=1, name='Modal Analysis Settings', number_of_modes_method=ModalNumberOfModes.NUMBER_OF_MODES_METHOD_USER_DEFINED, number_of_modes=4, solution_method=ModalSolutionMethod.SOLUTION_METHOD_SHIFTED_INVERSE_POWER_METHOD, find_modes_beyond_frequency=False, frequency_f=10, maxmimum_natural_frequency=1700, effective_modal_mass_factor=0.85, mass_matrix_type=ModalMassMatrixType.MASS_MATRIX_TYPE_CONSISTENT, mass_conversion_type=ModalMassConversionType.MASS_CONVERSION_TYPE_Z_COMPONENTS_OF_LOADS, acting_masses=None, neglect_masses=ModalNeglectMasses.E_NEGLECT_MASSES_NO_NEGLECTION, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### _static_ EffectiveMass(no=1, name='Modal Analysis Effective Mass', solution_method=ModalSolutionMethod.SOLUTION_METHOD_SHIFTED_INVERSE_POWER_METHOD, effective_modal_mass_factor=0.85, mass_matrix_type=ModalMassMatrixType.MASS_MATRIX_TYPE_CONSISTENT, mass_conversion_type=ModalMassConversionType.MASS_CONVERSION_TYPE_Z_COMPONENTS_OF_LOADS, acting_masses=None, neglect_masses=ModalNeglectMasses.E_NEGLECT_MASSES_NO_NEGLECTION, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Setting Tag


    * **name** (*str*) – Setting Name


    * **solution_method** (*enum*) – Modal solution method enumeration


    * **effective_modal_mass_factor** (*float*) – Effective modal mass factor


    * **mass_matrix_type** (*enum*) – Modal Mass Matrix Type Enumeration


    * **mass_conversion_type** (*enum*) – Modal Mass Conversion Type Enumeration


    * **acting_masses** (*list*) – Acting Masses Directions List


    * **neglect_masses** (*enum*) – Modal Neglect Masses Enumeration


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ MaximumFrequency(no=1, name='Modal Analysis Maximum Freq', solution_method=ModalSolutionMethod.SOLUTION_METHOD_SHIFTED_INVERSE_POWER_METHOD, find_modes_beyond_frequency=False, frequency_f=10, maxmimum_natural_frequency=1700, mass_matrix_type=ModalMassMatrixType.MASS_MATRIX_TYPE_CONSISTENT, mass_conversion_type=ModalMassConversionType.MASS_CONVERSION_TYPE_Z_COMPONENTS_OF_LOADS, acting_masses=None, neglect_masses=ModalNeglectMasses.E_NEGLECT_MASSES_NO_NEGLECTION, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Setting Tag


    * **name** (*str*) – Setting Name


    * **solution_method** (*enum*) – Modal solution method enumeration


    * **find_modes_beyond_frequency** (*bool*) – Find modes beyond frequency


    * **frequency_f** (*float*) – Frequency f (Hz)


    * **maxmimum_natural_frequency** (*float*) – Maximum natural frequency


    * **mass_matrix_type** (*enum*) – Modal Mass Matrix Type Enumeration


    * **mass_conversion_type** (*enum*) – Modal Mass Conversion Type Enumeration


    * **acting_masses** (*list*) – Acting Masses Directions List


    * **neglect_masses** (*enum*) – Modal Neglect Masses Enumeration


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ UserDefined(no=1, name='Modal Analysis User Defined', number_of_modes=4, solution_method=ModalSolutionMethod.SOLUTION_METHOD_SHIFTED_INVERSE_POWER_METHOD, find_modes_beyond_frequency=False, frequency_f=10, mass_matrix_type=ModalMassMatrixType.MASS_MATRIX_TYPE_CONSISTENT, mass_conversion_type=ModalMassConversionType.MASS_CONVERSION_TYPE_Z_COMPONENTS_OF_LOADS, acting_masses=None, neglect_masses=ModalNeglectMasses.E_NEGLECT_MASSES_NO_NEGLECTION, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Setting Tag


    * **name** (*str*) – Setting Name


    * **number_of_modes** (*int*) – Number of modes


    * **solution_method** (*enum*) – Modal solution method enumeration


    * **find_modes_beyond_frequency** (*bool*) – Find modes beyond frequency


    * **frequency_f** (*float*) – Frequency f (Hz)


    * **mass_matrix_type** (*enum*) – Modal Mass Matrix Type Enumeration


    * **mass_conversion_type** (*enum*) – Modal Mass Conversion Type Enumeration


    * **acting_masses** (*list*) – Acting Masses Directions List


    * **neglect_masses** (*enum*) – Modal Neglect Masses Enumeration


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### \__init__(no=1, name='Modal Analysis Settings', number_of_modes_method=ModalNumberOfModes.NUMBER_OF_MODES_METHOD_USER_DEFINED, number_of_modes=4, solution_method=ModalSolutionMethod.SOLUTION_METHOD_SHIFTED_INVERSE_POWER_METHOD, find_modes_beyond_frequency=False, frequency_f=10, maxmimum_natural_frequency=1700, effective_modal_mass_factor=0.85, mass_matrix_type=ModalMassMatrixType.MASS_MATRIX_TYPE_CONSISTENT, mass_conversion_type=ModalMassConversionType.MASS_CONVERSION_TYPE_Z_COMPONENTS_OF_LOADS, acting_masses=None, neglect_masses=ModalNeglectMasses.E_NEGLECT_MASSES_NO_NEGLECTION, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Setting Tag


    * **name** (*str*) – Setting Name


    * **number_of_modes_method** (*enum*) – Method for dertermining the number of nodes


    * **number_of_modes** (*int*) – Number of modes


    * **solution_method** (*enum*) – Modal solution method enumeration


    * **find_modes_beyond_frequency** (*bool*) – Find modes beyond frequency


    * **frequency_f** (*float*) – Frequency f (Hz)


    * **maxmimum_natural_frequency** (*float*) – Maximum natural frequency


    * **effective_modal_mass_factor** (*float*) – Effective modal mass factor


    * **mass_matrix_type** (*enum*) – Modal Mass Matrix Type Enumeration


    * **mass_conversion_type** (*enum*) – Modal Mass Conversion Type Enumeration


    * **acting_masses** (*list*) – Acting Masses Directions List


    * **neglect_masses** (*enum*) – Modal Neglect Masses Enumeration


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## RSTAB.LoadCasesAndCombinations.resultCombination module


### _class_ RSTAB.LoadCasesAndCombinations.resultCombination.ResultCombination(no=1, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(no=1, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Result Combination Tag


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## RSTAB.LoadCasesAndCombinations.spectralAnalysisSettings module


### _class_ RSTAB.LoadCasesAndCombinations.spectralAnalysisSettings.SpectralAnalysisSettings(no=1, name='SRSS | SRSS', periodic_combination=PeriodicResponseCombinationRule.SRSS, directional_combination=DirectionalComponentCombinationRule.SRSS, equivalent_linear_combination=False, save_mode_results=False, signed_dominant_mode_results=False, directional_component_scale_value=0.3, damping_for_cqc_rule=CqsDampingRule.CONSTANT_FOR_EACH_MODE, constant_d_for_each_mode=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(no=1, name='SRSS | SRSS', periodic_combination=PeriodicResponseCombinationRule.SRSS, directional_combination=DirectionalComponentCombinationRule.SRSS, equivalent_linear_combination=False, save_mode_results=False, signed_dominant_mode_results=False, directional_component_scale_value=0.3, damping_for_cqc_rule=CqsDampingRule.CONSTANT_FOR_EACH_MODE, constant_d_for_each_mode=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Sprectral Analysis Settings Tag


    * **name** (*str*) – Sprectral Analysis Settings Name


    * **periodic_combination** (*enum*) – Periodic Combination Rule Enumeration


    * **directional_combination** (*enum*) – Directional Component Combination Rule Enumeration


    * **equivalent_linear_combination** (*bool*) – Equivalent Linear Combination Boolean


    * **save_mode_results** (*bool*) – Save Mode Results Boolean


    * **signed_dominant_mode_results** (*bool*) – Signed Dominant Mode Results Boolean


    * **directional_component_scale_value** (*float*) – Directional Component Scale Value


    * **damping_for_cqc_rule** (*enum*) – Cqs Damping Rule Enumeration


    * **constant_d_for_each_mode** (*float*) – Constant d for Each Mode


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## RSTAB.LoadCasesAndCombinations.stabilityAnalysisSettings module


### _class_ RSTAB.LoadCasesAndCombinations.stabilityAnalysisSettings.StabilityAnalysisSettings(no=1, name=None, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### _static_ EigenvalueMethod(no=1, name=None, number_of_lowest_eigenvalues=4, considered_favored_effect=True, critical_load_factor=None, minimum_initial_strain=1e-05, local_torsional_rotations=None, eigenvalue_method=StabilityAnalysisSettingsEigenvalueMethod.EIGENVALUE_METHOD_LANCZOS, matrix_type=StabilityAnalysisSettingsMatrixType.MATRIX_TYPE_STANDARD, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Stability Analysis Setting Tag


    * **name** (*str**, **optional*) – Stability Analysis Setting Name


    * **number_of_lowest_eigenvalues** (*int*) – Number of Lowest Eigenvalues


    * **considered_favored_effect** (*bool*) – Considered Favored Effect


    * **critical_load_factor** (*int**, **optional*) – Critical Load Factor
    for find_eigenvectors_beyond_critical_load_factor == False:

    > critical_load_factor = None

    for find_eigenvectors_beyond_critical_load_factor == True:

        critical_load_factor = int



    * **minimum_initial_strain** (*optional*) – Minimum Initial Strain
    for minimum initial strain application:

    > minimum_initial_strain != 0 or minimum_initial_strain

    for no minimum initial strain application:

        minimum_initial_strain == 0 or minimum_initial_strain is None



    * **local_torsional_rotations** (*optional*) – Local Torsional Rotations
    for no local torsional rotations display:

    > local_torsional_rotations = None

    for local torsional rotations display:

        local_torsional_rotations = double



    * **eigenvalue_method** (*enum*) – StabilityAnalysisSettings Eigenvalue Method Enumeration


    * **matrix_type** (*enum*) – StabilityAnalysisSettings Matrix Type Enumeration


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ IncrementalyMethodWithEigenvalue(no=1, name=None, number_of_lowest_eigenvalues=4, considered_favored_effect=True, critical_load_factor=None, minimum_initial_strain=1e-05, local_torsional_rotations=None, incrementally_increasing_loading=[1.0, 0.1, 10, 100], stopping_of_load_increasing=None, save_results_of_all_increments=False, eigenvalue_method=StabilityAnalysisSettingsEigenvalueMethod.EIGENVALUE_METHOD_LANCZOS, matrix_type=StabilityAnalysisSettingsMatrixType.MATRIX_TYPE_STANDARD, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Stability Analysis Setting Tag


    * **name** (*str**, **optional*) – Stability Analysis Setting Name


    * **number_of_lowest_eigenvalues** (*int*) – Number of Lowest Eigenvalues


    * **considered_favored_effect** (*bool*) – Considered Favored Effect


    * **critical_load_factor** (*int**, **optional*) – Critical Load Factor
    for find_eigenvectors_beyond_critical_load_factor == False:

    > critical_load_factor = None

    for find_eigenvectors_beyond_critical_load_factor == True:

        critical_load_factor = int



    * **minimum_initial_strain** (*optional*) – Minimum Initial Strain
    for minimum initial strain application:

    > minimum_initial_strain != 0 or minimum_initial_strain

    for no minimum initial strain application:

        minimum_initial_strain is None



    * **local_torsional_rotations** (*optional*) – Local Torsional Rotations
    for no local torsional rotations display:

    > local_torsional_rotations = None

    for local torsional rotations display:

        local_torsional_rotations = double



    * **incrementally_increasing_loading** (*list*) – Incrementally Increasing Loading
    incrementally_increasing_loading = [initial_load_factor, load_factor_increment, refinement_of_the_last_load_increment, maximum_number_of_load_increments]


    * **stopping_of_load_increasing** (*list**, **optional*) – Stopping of Load Increasing
    for stopping of load increasing deactivated:

    > stopping_of_load_increasing = None

    for result u:

        stopping_of_load_increasing = [StabilityAnalysisSettingsStoppingOfLoadIncreasingResult.RESULT_TYPE_DISPLACEMENT_U, limit_result_displacement, limit_node]

    for result uX:

        stopping_of_load_increasing = [StabilityAnalysisSettingsStoppingOfLoadIncreasingResult.RESULT_TYPE_DISPLACEMENT_U_X, limit_result_displacement, limit_node]

    for result uY:

        stopping_of_load_increasing = [StabilityAnalysisSettingsStoppingOfLoadIncreasingResult.RESULT_TYPE_DISPLACEMENT_U_Y, limit_result_displacement, limit_node]

    for result uZ:

        stopping_of_load_increasing = [StabilityAnalysisSettingsStoppingOfLoadIncreasingResult.RESULT_TYPE_DISPLACEMENT_U_Z, limit_result_displacement, limit_node]

    for result phi:

        stopping_of_load_increasing = [StabilityAnalysisSettingsStoppingOfLoadIncreasingResult.RESULT_TYPE_ROTATION_PHI, limit_result_rotation, limit_node]

    for result phiX:

        stopping_of_load_increasing = [StabilityAnalysisSettingsStoppingOfLoadIncreasingResult.RESULT_TYPE_ROTATION_PHI_X, limit_result_rotation, limit_node]

    for result phiY:

        stopping_of_load_increasing = [StabilityAnalysisSettingsStoppingOfLoadIncreasingResult.RESULT_TYPE_ROTATION_PHI_Y, limit_result_rotation, limit_node]

    for result phiZ:

        stopping_of_load_increasing = [StabilityAnalysisSettingsStoppingOfLoadIncreasingResult.RESULT_TYPE_ROTATION_PHI_Z, limit_result_rotation, limit_node]



    * **save_results_of_all_increments** (*bool**, **optional*) – Save Results of All Increments


    * **eigenvalue_method** (*enum*) – StabilityAnalysisSettings Eigenvalue Method Enumeration


    * **matrix_type** (*enum*) – StabilityAnalysisSettings Matrix Type Enumeration


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ IncrementalyMethodWithoutEigenvalue(no=1, name=None, minimum_initial_strain=1e-05, local_torsional_rotations=None, incrementally_increasing_loading=[1.0, 0.1, 10, 100], stopping_of_load_increasing=None, save_results_of_all_increments=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Stability Analysis Setting Tag


    * **name** (*str**, **optional*) – Stability Analysis Setting Name


    * **minimum_initial_strain** (*optional*) – Minimum Initial Strain
    for minimum initial strain application:

    > minimum_initial_strain != 0 or minimum_initial_strain

    for no minimum initial strain application:

        minimum_initial_strain == 0 or minimum_initial_strain is None



    * **local_torsional_rotations** (*optional*) – Local Torsional Rotations
    for no local torsional rotations display:

    > local_torsional_rotations = None

    for local torsional rotations display:

        local_torsional_rotations = double



    * **incrementally_increasing_loading** (*list*) – Incrementally Increasing Loading
    incrementally_increasing_loading = [initial_load_factor, load_factor_increment, refinement_of_the_last_load_increment, maximum_number_of_load_increments]


    * **stopping_of_load_increasing** (*list**, **optional*) – Stopping of Load Increasing
    for stopping of load increasing deactivated:

    > stopping_of_load_increasing = None

    for result u:

        stopping_of_load_increasing = [StabilityAnalysisSettingsStoppingOfLoadIncreasingResult.RESULT_TYPE_DISPLACEMENT_U, limit_result_displacement, limit_node]

    for result uX:

        stopping_of_load_increasing = [StabilityAnalysisSettingsStoppingOfLoadIncreasingResult.RESULT_TYPE_DISPLACEMENT_U_X, limit_result_displacement, limit_node]

    for result uY:

        stopping_of_load_increasing = [StabilityAnalysisSettingsStoppingOfLoadIncreasingResult.RESULT_TYPE_DISPLACEMENT_U_Y, limit_result_displacement, limit_node]

    for result uZ:

        stopping_of_load_increasing = [StabilityAnalysisSettingsStoppingOfLoadIncreasingResult.RESULT_TYPE_DISPLACEMENT_U_Z, limit_result_displacement, limit_node]

    for result phi:

        stopping_of_load_increasing = [StabilityAnalysisSettingsStoppingOfLoadIncreasingResult.RESULT_TYPE_ROTATION_PHI, limit_result_rotation, limit_node]

    for result phiX:

        stopping_of_load_increasing = [StabilityAnalysisSettingsStoppingOfLoadIncreasingResult.RESULT_TYPE_ROTATION_PHI_X, limit_result_rotation, limit_node]

    for result phiY:

        stopping_of_load_increasing = [StabilityAnalysisSettingsStoppingOfLoadIncreasingResult.RESULT_TYPE_ROTATION_PHI_Y, limit_result_rotation, limit_node]

    for result phiZ:

        stopping_of_load_increasing = [StabilityAnalysisSettingsStoppingOfLoadIncreasingResult.RESULT_TYPE_ROTATION_PHI_Z, limit_result_rotation, limit_node]



    * **save_results_of_all_increments** (*bool**, **optional*) – Save Results of All Increments


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### \__init__(no=1, name=None, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Stability Analysis Setting Tag


    * **name** (*str*) – Stability Analysis Setting Name


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


## RSTAB.LoadCasesAndCombinations.staticAnalysisSettings module


### _class_ RSTAB.LoadCasesAndCombinations.staticAnalysisSettings.StaticAnalysisSettings(no=1, name=None, analysis_type=StaticAnalysisType.GEOMETRICALLY_LINEAR, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### _static_ GeometricallyLinear(no=1, name=None, load_modification=[False, 1, False], bourdon_effect=False, mass_conversion=[False, 0, 0, 0], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Static Analysis Setting Tag


    * **name** (*str*) – Static Analysis Setting Name


    * **load_modification** (*list*) – Load Modification Parameters
    load_modification = [loading_by_multiplier_factor, multiplier_factor, dividing_results]


    * **mass_conversion** (*list*) – Mass Conversion Parameters
    mass_conversion = [mass_conversion_enabled, mass_conversion_factor_in_direction_x, mass_conversion_factor_in_direction_y, mass_conversion_factor_in_direction_z]


    * **comment** (*str*) – Comments


    * **params** (*dict*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class*) – Model to be edited



#### _static_ LargeDeformation(no=1, name=None, iterative_method=StaticAnalysisSettingsIterativeMethodForNonlinearAnalysis.NEWTON_RAPHSON, precision_of_convergence_criteria_for_nonlinear_calculation=0, max_number_of_iterations=100, number_of_load_increments=1, load_modification=[False, 1, False], bourdon_effect=True, mass_conversion=[False, 0, 0, 1], comment='', params={'save_results_of_all_load_increments': False}, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Static Analysis Setting Tag


    * **name** (*str*) – Static Analysis Setting Name


    * **iterative_method** (*enum*) – Static Analysis Settings Iterative Method for Non-linear Analysis Enumeration


    * **precision_of_convergence_criteria_for_nonlinear_calculation** (*float*) – Precision of Convergence defaults to 0


    * **max_number_of_iterations** (*float*) – Maximum Number of Iterations


    * **number_of_load_increments** (*float*) – Number of Load Increments


    * **load_modification** (*list*) – Load Modification Parameters
    load_modification = [loading_by_multiplier_factor, multiplier_factor, dividing_results]


    * **bourdon_effect** (*bool*) – Bourdon Effect Boolean


    * **mass_conversion** (*list*) – Mass Conversion Parameters
    mass_conversion = [mass_conversion_enabled, mass_conversion_factor_in_direction_x, mass_conversion_factor_in_direction_y, mass_conversion_factor_in_direction_z]


    * **comment** (*str*) – Comments


    * **params** (*dict*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class*) – Model to be edited



#### _static_ SecondOrderPDelta(no=1, name=None, max_number_of_iterations=100, number_of_load_increments=1, load_modification=[False, 0, False], precision_of_convergence_criteria_for_nonlinear_calculation=0, favorable_effect_due_to_tension_in_members=False, bourdon_effect=True, internal_forces_to_deformed_structure=[True, True, True, True], mass_conversion=[False, 0, 0, 1], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Static Analysis Setting Tag


    * **name** (*str*) – Static Analysis Setting Name


    * **max_number_of_iterations** (*int*) – Maximum Number of Iterations


    * **number_of_load_increments** (*int*) – Number of Load Increments


    * **load_modification** (*list*) – Modify Loading by Multiplier Factor
    load_modification = [modify_loading_by_multiplier_factor, loading_multiplier_factor, divide_results_by_loading_factor]


    * **precision_of_convergence_criteria_for_nonlinear_calculation** (*float*) – Precision of Convergence defaults to 0


    * **favorable_effect_due_to_tension_in_members** (*bool*) – Favorable Effect due to Tension In Members Boolean


    * **bourdon_effect** (*bool*) – Bourdon Effect Boolean


    * **internal_forces_to_deformed_structure** (*list*) – Internal Forces to Deformed Structure List
    internal_forces_to_deformed_structure = [refer_internal_forces_to_deformed_structure, internal_forces_to_deformed_structure_for_moments, internal_forces_to_deformed_structure_for_normal_forces, internal_forces_to_deformed_structure_for_shear_forces]


    * **mass_conversion** (*list*) – Mass Conversion Parameters
    mass_conversion = [mass_conversion_enabled, mass_conversion_factor_in_direction_x, mass_conversion_factor_in_direction_y, mass_conversion_factor_in_direction_z]


    * **comment** (*str*) – Comments


    * **params** (*dict*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class*) – Model to be edited



#### \__init__(no=1, name=None, analysis_type=StaticAnalysisType.GEOMETRICALLY_LINEAR, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Static Analysis Setting Tag


    * **name** (*str*) – Static Analysis Setting Name


    * **analysis_type** (*enum*) – Analysis Type Enumeration


    * **comment** (*str*) – Comments


    * **params** (*dict*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class*) – Model to be edited


## Module contents
