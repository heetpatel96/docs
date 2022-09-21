# RSTAB.Loads package

## Submodules

## RSTAB.Loads.imposedNodalDeformation module


### _class_ RSTAB.Loads.imposedNodalDeformation.ImposedNodalDeformation(no=1, load_case_no=1, node_no='1', load_parameter=None, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(no=1, load_case_no=1, node_no='1', load_parameter=None, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **node_no** (*str*) – Assigned node(s)


    * **load_parameter** (*list*) – Load Parameters List
    load_parameter = [imposed_displacement_x, imposed_displacement_y, imposed_displacement_z, imposed_rotation_x, imposed_rotation_y imposed_rotation_z]


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## RSTAB.Loads.memberLoad module


### _class_ RSTAB.Loads.memberLoad.MemberLoad(no=1, load_case_no=1, members_no='1', load_direction=LoadDirectionType.LOAD_DIRECTION_LOCAL_Z, magnitude=2000, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### _static_ AxialDisplacement(no=1, load_case_no=1, members_no='1', load_direction=MemberLoadDirection.LOAD_DIRECTION_LOCAL_X, magnitude=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **members_no** (*str*) – Assigned Member(s)


    * **load_direction** (*enum*) – Member Load Direction Enumeration


    * **magnitude** (*float*) – Load Magnitude


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ AxialStrain(no=1, load_case_no=1, members_no='1', load_distribution=MemberLoadDistribution.LOAD_DISTRIBUTION_UNIFORM, load_direction=MemberLoadDirection.LOAD_DIRECTION_LOCAL_X, load_parameter=None, list_reference=False, load_over_total_length=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **members_no** (*str*) – Assigned Member(s)


    * **load_distribution** (*enum*) – Member Load Distribution Enumeration


    * **load_direction** (*enum*) – Member Load Direction Enumeration


    * **load_parameter** (*list/list of lists*) – Load Parameter List
    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_UNIFORM:

    > load_parameter = [epsilon]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_TRAPEZIODAL:

        load_parameter = [epsilon1, epsilon2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_TAPERED:

        load_parameter = [epsilon1, epsilon2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_TAPERED:

        load_parameter = [epsilon1, epsilon2, epsilon3]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_VARYING:

        load_parameter = [[distance, magnitude], …]



    * **list_reference** (*bool*) – Enable/Disable List Reference Option


    * **load_over_total_length** (*bool*) – Enable/Disable Load Over Total Length Option


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Displacement(no=1, load_case_no=1, members_no='1', load_distribution=MemberLoadDistribution.LOAD_DISTRIBUTION_UNIFORM, load_direction=MemberLoadDirection.LOAD_DIRECTION_LOCAL_Z, load_parameter=None, list_reference=False, load_over_total_length=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **members_no** (*str*) – Assigned Member(s)


    * **load_distribution** (*enum*) – Member Load Distribution Enumeration


    * **load_direction** (*enum*) – Member Load Direction Enumeration


    * **load_parameter** (*list/list of lists*) – Load Parameter List
    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_UNIFORM:

    > load_parameter = [magnitude]

    for load_distrubition == MemberLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_1:

        load_parameter = [magnitude, distance_a_is_defined_as_relative = False, distance_a]

    for load_distrubition == MemberLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_N:

        load_parameter = [magnitude, distance_a_is_defined_as_relative = False, distance_b_is_defined_as_relative = False, distance_a, distance_b]

    for load_distrubition == MemberLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_2x2:

        load_parameter = [magnitude, distance_a_is_defined_as_relative = False, distance_b_is_defined_as_relative = False, distance_c_is_defined_as_relative = False, distance_a, distance_b, distance_c]

    for load_distrubition == MemberLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_2:

        load_parameter = [magnitude_1, magnitude_2, distance_a_is_defined_as_relative = False, distance_b_is_defined_as_relative = False, distance_a, distance_b]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_VARYING:

        load_parameter = [[distance, magnitude], …]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_TRAPEZIODAL:

        load_parameter = [magnitude_1, magnitude_2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_TAPERED:

        load_parameter = [magnitude_1, magnitude_2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_PARABOLIC:

        load_parameter = [magnitude_1, magnitude_2, magnitude_3]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_VARYING:

        load_parameter = [[distance, magnitude], …]



    * **list_reference** (*bool*) – Enable/Disable List Reference Option


    * **load_over_total_length** (*bool*) – Enable/Disable Load Over Total Length Option


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Force(no=1, load_case_no=1, members_no='1', load_distribution=MemberLoadDistribution.LOAD_DISTRIBUTION_UNIFORM, load_direction=MemberLoadDirection.LOAD_DIRECTION_LOCAL_Z, load_parameter=None, force_eccentricity=False, list_reference=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **members_no** (*str*) – Assigned Member(s)


    * **load_distribution** (*enum*) – Member Load Distribution Enumeration


    * **load_direction** (*enum*) – Member Load Direction Enumeration


    * **load_parameter** (*float/list/list of lists*) – Load Parameter List
    for load_distribution == LOAD_DISTRIBUTION_UNIFORM:

    > load_parameter = magnitude

    for load_distribution == LOAD_DISTRIBUTION_UNIFORM_TOTAL:

        load_parameter = magnitude

    for load_distribution == LOAD_DISTRIBUTION_CONCENTRATED_1:

        load_parameter = [relative_distance = False, magnitude, distance_a]

    for load_distribution == LOAD_DISTRIBUTION_CONCENTRATED_N:

        load_parameter = [relative_distance_a = False, relative_distance_b = False, magnitude, count_n, distance_a, distance_b]

    for load_distribution == LOAD_DISTRIBUTION_CONCENTRATED_2x2:

        load_parameter = [relative_distance_a = False, relative_distance_b = False, relative_distance_c = False, magnitude, distance_a, distance_b, distance_c]

    for load_distribution == LOAD_DISTRIBUTION_CONCENTRATED_2:

        load_parameter = [relative_distance_a = False, relative_distance_b = False, magnitude_1, magnitude_2, distance_a, distance_b]

    for load_distribution == LOAD_DISTRIBUTION_CONCENTRATED_VARYING:

        load_parameter = [[distance, magnitude], …]

    for load_distribution == LOAD_DISTRIBUTION_TRAPEZOIDAL:

        load_parameter = [relative_distance_a = False, relative_distance_b = False,magnitude_1, magnitude_2, distance_a, distance_b]

    for load_distribution == LOAD_DISTRIBUTION_TAPERED:

        load_parameter = [relative_distance_a = False, relative_distance_b = False,magnitude_1, magnitude_2, distance_a, distance_b]

    for load_distribution == LOAD_DISTRIBUTION_PARABOLIC:

        load_parameter = [magnitude_1, magnitude_2, magnitude_3]

    for load_distribution == LOAD_DISTRIBUTION_VARYING:

        load_parameter = [[distance, magnitude], …]

    for load_distribution == LOAD_DISTRIBUTION_VARYING_IN_Z:

        load_parameter = [[distance, magnitude], …]



    * **force_eccentricity** (*bool*) – Enable/Disable Force Eccentricity Option


    * **list_reference** (*bool*) – Enable/Disable List Reference Option


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary
    for force_eccentricity == True:

    > params = {‘eccentricity_horizontal_alignment’: MemberLoadEccentricityHorizontalAlignment.ALIGN_NONE,

    >     ’eccentricity_vertical_alignment’: MemberLoadEccentricityVerticalAlignment.ALIGN_NONE,
    >     ‘eccentricity_section_middle’: MemberLoadEccentricitySectionMiddle.LOAD_ECCENTRICITY_SECTION_MIDDLE_CENTER_OF_GRAVITY,
    >     ‘is_eccentricity_at_end_different_from_start’: False,
    >     ‘eccentricity_y_at_end’: 0.0,
    >     ‘eccentricity_y_at_start’: 0.0,
    >     ‘eccentricity_z_at_end’: 0.0,
    >     ‘eccentricity_z_at_start’: 0.0}



    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ InitialPrestress(no=1, load_case_no=1, members_no='1', load_direction=MemberLoadDirection.LOAD_DIRECTION_LOCAL_X, magnitude=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **members_no** (*str*) – Assigned Member(s)


    * **load_direction** (*enum*) – Member Load Direction Enumeration


    * **magnitude** (*float*) – Load Magnitude


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Mass(no=1, load_case_no=1, members_no='1', individual_mass_components=False, mass_components=None, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **members_no** (*str*) – Assigned Member(s)


    * **individual_mass_components** (*bool*) – Enable/Disable Individual Mass Components Option


    * **mass_components** (*list*) – Mass Components List
    if individual_mass_components == False:

    > mass_components = [M]

    else:

        mass_components = [Mx, My, Mz, Ix, Iy, Iz]



    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Moment(no=1, load_case_no=1, members_no='1', load_distribution=MemberLoadDistribution.LOAD_DISTRIBUTION_UNIFORM, load_direction=MemberLoadDirection.LOAD_DIRECTION_LOCAL_Z, load_parameter=None, list_reference=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **members_no** (*str*) – Assigned Member(s)


    * **load_distribution** (*enum*) – Load Distribution Enumeration


    * **load_direction** (*enum*) – Load Direction Enumeration


    * **load_parameter** (*float/list/list of lists*) – Load Parameter List
    for load_distribution == LOAD_DISTRIBUTION_UNIFORM:

    > load_parameter = magnitude

    for load_distribution == LOAD_DISTRIBUTION_CONCENTRATED_1:

        load_parameter = [relative_distance = False, magnitude, distance_a]

    for load_distribution == LOAD_DISTRIBUTION_CONCENTRATED_N:

        load_parameter = [relative_distance_a = False, relative_distance_b = False, magnitude, count_n, distance_a, distance_b]

    for load_distribution == LOAD_DISTRIBUTION_CONCENTRATED_2x2:

        load_parameter = [relative_distance_a = False, relative_distance_b = False, relative_distance_c = False, magnitude, distance_a, distance_b, distance_c]

    for load_distribution == LOAD_DISTRIBUTION_CONCENTRATED_2:

        load_parameter = [relative_distance_a = False, relative_distance_b = False, magnitude_1, magnitude_2, distance_a, distance_b]

    for load_distribution == LOAD_DISTRIBUTION_CONCENTRATED_VARYING:

        load_parameter = [[distance, magnitude], …]

    for load_distribution == LOAD_DISTRIBUTION_TRAPEZOIDAL:

        load_parameter = [relative_distance_a = False, relative_distance_b = False,magnitude_1, magnitude_2, distance_a, distance_b]

    for load_distribution == LOAD_DISTRIBUTION_TAPERED:

        load_parameter = [relative_distance_a = False, relative_distance_b = False,magnitude_1, magnitude_2, distance_a, distance_b]

    for load_distribution == LOAD_DISTRIBUTION_PARABOLIC:

        load_parameter = [magnitude_1, magnitude_2, magnitude_3]

    for load_distribution == LOAD_DISTRIBUTION_VARYING:

        load_parameter = [[distance, magnitude], …]



    * **list_reference** (*bool*) – Enable/Disable List Reference Option


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ PipeContentFull(no=1, load_case_no=1, members_no='1', load_direction_orientation=MemberLoadDirectionOrientation.LOAD_DIRECTION_FORWARD, specific_weight=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **members_no** (*str*) – Assigned Member(s)


    * **load_direction_orientation** (*enum*) – Member Load Direction Enumeration


    * **specific_weight** (*float*) – Specific Weight


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ PipeContentPartial(no=1, load_case_no=1, members_no='1', load_direction_orientation=MemberLoadDirectionOrientation.LOAD_DIRECTION_FORWARD, specific_weight=0.0, filling_height=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **members_no** (*str*) – Assigned Member(s)


    * **load_direction_orientation** (*enum*) – Member Load Direction Enumeration


    * **specific_weight** (*float*) – Specific Weight


    * **filling_height** (*float*) – Filling Height


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ PipeInternalPressure(no=1, load_case_no=1, members_no='1', pressure=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **members_no** (*str*) – Assigned Member(s)


    * **pressure** (*float*) – Pressure


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Precamber(no=1, load_case_no=1, members_no='1', load_distribution=MemberLoadDistribution.LOAD_DISTRIBUTION_UNIFORM, load_direction=MemberLoadDirection.LOAD_DIRECTION_LOCAL_Z, load_parameter=None, list_reference=False, load_over_total_length=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **members_no** (*str*) – Assigned Member(s)


    * **load_distribution** (*enum*) – Member Load Distribution Enumeration


    * **load_direction** (*enum*) – Member Load Direction Enumeration


    * **load_parameter** (*list/list of lists*) – Load Parameter List
    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_UNIFORM:

    > load_parameter = [magnitude]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_TRAPEZIODAL:

        load_parameter = [magnitude_1, magnitude_2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_TAPERED:

        load_parameter = [magnitude_1, magnitude_2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_PARABOLIC:

        load_parameter = [magnitude_1, magnitude_2, magnitude_3]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_VARYING:

        load_parameter = [[distance, magnitude], …]



    * **list_reference** (*bool*) – Enable/Disable List Reference Option


    * **load_over_total_length** (*bool*) – Enable/Disable Load Over Total Length Option


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ RotaryMotion(no=1, load_case_no=1, members_no='1', angular_acceleration=1.0, angular_velocity=2.0, axis_definition_type=MemberLoadAxisDefinitionType.AXIS_DEFINITION_TWO_POINTS, axis_orientation=MemberLoadAxisDefinitionAxisOrientation.AXIS_POSITIVE, axis_definition=MemberLoadAxisDefinition.AXIS_X, axis_definition_p1=[1, 0, 1], axis_definition_p2=[0, 1, 0], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **members_no** (*str*) – Assigned Member(s)


    * **angular_acceleration** (*float*) – Angular Acceleration


    * **angular_velocity** (*float*) – Angular Velocity


    * **axis_definition_type** (*enum*) – Member Load Axis Definition Type Enumeration


    * **axis_orientation** (*enum*) – Member Load Axis Orientation Enumeration


    * **axis_definition** (*enum*) – Member Load Axis Definition Enumeration


    * **axis_definition_p1** (*list*) – P1 List [X, Y, Z]


    * **axis_definition_p2** (*list*) – P2 List [X, Y, Z]


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Rotation(no=1, load_case_no=1, members_no='1', load_distribution=MemberLoadDistribution.LOAD_DISTRIBUTION_UNIFORM, load_direction=MemberLoadDirection.LOAD_DIRECTION_LOCAL_Z, load_parameter=None, list_reference=False, load_over_total_length=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **members_no** (*str*) – Assigned Member(s)


    * **load_distribution** (*enum*) – Member Load Distribution Enumeration


    * **load_direction** (*enum*) – Member Load Direction Enumeration


    * **load_parameter** (*list/list of lists*) – Load Parameter List
    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_UNIFORM:

    > load_parameter = [magnitude]

    for load_distrubition == MemberLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_1:

        load_parameter = [magnitude, distance_a_is_defined_as_relative = False, distance_a]

    for load_distrubition == MemberLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_N:

        load_parameter = [magnitude, distance_a_is_defined_as_relative = False, distance_b_is_defined_as_relative = False, distance_a, distance_b]

    for load_distrubition == MemberLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_2x2:

        load_parameter = [magnitude, distance_a_is_defined_as_relative = False, distance_b_is_defined_as_relative = False, distance_c_is_defined_as_relative = False, distance_a, distance_b, distance_c]

    for load_distrubition == MemberLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_2:

        load_parameter = [magnitude_1, magnitude_2, distance_a_is_defined_as_relative = False, distance_b_is_defined_as_relative = False, distance_a, distance_b]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_VARYING:

        load_parameter = [[distance, magnitude], …]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_TRAPEZIODAL:

        load_parameter = [magnitude_1, magnitude_2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_TAPERED:

        load_parameter = [magnitude_1, magnitude_2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_PARABOLIC:

        load_parameter = [magnitude_1, magnitude_2, magnitude_3]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_VARYING:

        load_parameter = [[distance, magnitude], …]



    * **list_reference** (*bool*) – Enable/Disable List Reference Option


    * **load_over_total_length** (*bool*) – Enable/Disable Load Over Total Length Option


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Temperature(no=1, load_case_no=1, members_no='1', load_distribution=MemberLoadDistribution.LOAD_DISTRIBUTION_UNIFORM, load_direction=MemberLoadDirection.LOAD_DIRECTION_LOCAL_Z, load_parameter=None, list_reference=False, load_over_total_length=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **members_no** (*str*) – Assigned Member(s)


    * **load_distribution** (*enum*) – Member Load Distribution Enumeration


    * **load_direction** (*enum*) – Member Load Direction Enumeration


    * **load_parameter** (*list/list of lists*) – Load Parameter List
    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_UNIFORM:

    > load_parameter = [tt, tb]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_TRAPEZIODAL:

        for load_over_total_length == False:

            load_parameter = [tt1, tt2, tb1, tb2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

        for load_over_total_length == True:

            load_parameter = [tt1, tt2, tb1, tb2]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_TAPERED:

        load_parameter = [tt1, tt2, tb1, tb2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_PARABOLIC:

        load_parameter = [tb1, tb2, tb3, tt1, tt2, tt3]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_VARYING:

        load_parameter = [[distance, magnitude], …]



    * **list_reference** (*bool*) – List Reference Boolean


    * **load_over_total_length** (*bool*) – Enable/Disable Load Over Total Length Option


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ TemperatureChange(no=1, load_case_no=1, members_no='1', load_distribution=MemberLoadDistribution.LOAD_DISTRIBUTION_UNIFORM, load_direction=MemberLoadDirection.LOAD_DIRECTION_LOCAL_Z, load_parameter=None, list_reference=False, load_over_total_length=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **members_no** (*str*) – Assigned Member(s)


    * **load_distribution** (*enum*) – Member Load Distribution


    * **load_direction** (*enum*) – Member Load Direction Enumeration


    * **load_parameter** (*list/list of lists*) – Load Parameter List
    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_UNIFORM:

    > load_parameter = [tc, delta_t]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_TRAPEZIODAL:

        for load_over_total_length == False:

            load_parameter = [delta_t_1, delta_t_2, t_c_1, t_c_2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

        for load_over_total_length == True:

            load_parameter = [delta_t_1, delta_t_2, t_c_1, t_c_2]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_TAPERED:

        load_parameter = [delta_t_1, delta_t_2, t_c_1, t_c_2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_PARABOLIC:

        load_parameter = [delta_t_1, delta_t_2, delta_t_3, t_c_1, t_c_2, t_c_3]

    for load_distribution == MemberLoadDistribution.LOAD_DISTRIBUTION_VARYING:

        load_parameter = [[distance, magnitude], …]



    * **list_reference** (*bool*) – Enable/Disable List Reference Option


    * **load_over_total_length** (*bool*) – Enable/Disable Load Over Total Length Option


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### \__init__(no=1, load_case_no=1, members_no='1', load_direction=LoadDirectionType.LOAD_DIRECTION_LOCAL_Z, magnitude=2000, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **members_no** (*str*) – Assigned Members


    * **load_direction** (*enum*) – Load Directin Enumeration


    * **magnitude** (*float*) – Load Magnitude


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


## RSTAB.Loads.membersetload module


### _class_ RSTAB.Loads.membersetload.MemberSetLoad(no=1, load_case_no=1, member_sets='1', load_direction=LoadDirectionType.LOAD_DIRECTION_LOCAL_Z, magnitude=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### _static_ AxialDisplacement(no=1, load_case_no=1, member_sets='1', load_direction=MemberSetLoadDirection.LOAD_DIRECTION_LOCAL_X, magnitude=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **member_sets** (*str*) – Assigned Member Set


    * **load_direction** (*enum*) – MemberSet Load Direction Enumeration


    * **magnitude** (*float*) – Load Magnitude


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ AxialStrain(no=1, load_case_no=1, member_sets='1', load_distribution=MemberSetLoadDistribution.LOAD_DISTRIBUTION_UNIFORM, load_direction=MemberSetLoadDirection.LOAD_DIRECTION_LOCAL_X, load_parameter=None, load_over_total_length=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **member_sets** (*str*) – Assigned Member Sets


    * **load_distribution** (*enum*) – MemberSet Load Distribution Enumeration


    * **load_direction** (*enum*) – MemberSet Load Direction Enumeration


    * **load_parameter** (*list/list of lists*) – Load Parameters
    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_UNIFORM:

    > load_parameter = [epsilon]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_TRAPEZIODAL:

        for load_over_total_length: bool= False:

            load_parameter = [epsilon1, epsilon2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

        for load_over_total_length: bool= True:

            load_parameter = [epsilon1, epsilon2]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_TAPERED:

        load_parameter = [epsilon1, epsilon2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_TAPERED:

        load_parameter = [epsilon1, epsilon2, epsilon3]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_VARYING:

        load_parameter = [[distance, delta_distance, magnitude], …]



    * **load_over_total_length** (*bool*) – Load Over Total Length Option


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Displacement(no=1, load_case_no=1, member_sets='1', load_distribution=MemberSetLoadDistribution.LOAD_DISTRIBUTION_UNIFORM, load_direction=MemberSetLoadDirection.LOAD_DIRECTION_LOCAL_Z, load_parameter=None, load_over_total_length=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **member_sets** (*str*) – Assigned Member Sets


    * **load_distribution** (*enum*) – MemberSet Load Distribution Enumeration


    * **load_direction** (*enum*) – MemberSet Load Direction Enumeration


    * **load_parameter** (*list/list of lists*) – Load Parameters
    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_UNIFORM:

    > load_parameter = [magnitude]

    for load_distrubition = MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_1:

        load_parameter = [magnitude, distance_a_is_defined_as_relative = False, distance_a]

    for load_distrubition = MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_N:

        load_parameter = [magnitude, distance_a_is_defined_as_relative = False, distance_b_is_defined_as_relative = False, distance_a, distance_b]

    for load_distrubition = MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_2x2:

        load_parameter = [magnitude, distance_a_is_defined_as_relative = False, distance_b_is_defined_as_relative = False, distance_c_is_defined_as_relative = False, distance_a, distance_b, distance_c]

    for load_distrubition = MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_2:

        load_parameter = [magnitude_1, magnitude_2, distance_a_is_defined_as_relative = False, distance_b_is_defined_as_relative = False, distance_a, distance_b]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_VARYING:

        load_parameter = [[distance, delta_distance, magnitude], …]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_TRAPEZIODAL:

        load_parameter = [magnitude_1, magnitude_2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_TAPERED:

        load_parameter = [magnitude_1, magnitude_2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_PARABOLIC:

        load_parameter = [magnitude_1, magnitude_2, magnitude_3]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_VARYING:

        load_parameter = [[distance, delta_distance, magnitude], …]



    * **load_over_total_length** (*bool*) – Load Over Total Length Option


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Force(no=1, load_case_no=1, member_sets='1', load_distribution=MemberSetLoadDistribution.LOAD_DISTRIBUTION_UNIFORM, load_direction=MemberSetLoadDirection.LOAD_DIRECTION_LOCAL_Z, load_parameter=None, force_eccentricity=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **member_sets** (*str*) – Assigned Member Sets


    * **load_distribution** (*enum*) – MemberSet Load Distribution Enumeration


    * **load_direction** (*enum*) – MemberSet Load Direction Enumeration


    * **load_parameter** (*list/list of lists*) – Load Parameter
    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_UNIFORM:

    > load_parameter = [magnitude]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_UNIFORM_TOTAL:

        load_parameter = [magnitude]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_1:

        load_parameter = [relative_distance = False, magnitude, distance_a]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_N:

        load_parameter = [relative_distance_a = False, relative_distance_b = False, magnitude, count_n, distance_a, distance_b]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_2x2:

        load_parameter = [relative_distance_a = False, relative_distance_b = False, relative_distance_c = False, magnitude, distance_a, distance_b, distance_c]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_2:

        load_parameter = [relative_distance_a = False, relative_distance_b = False, magnitude_1, magnitude_2, distance_a, distance_b]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_VARYING:

        load_parameter = [[distance, delta_distance, magnitude], …]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_TRAPEZOIDAL:

        load_parameter = [relative_distance_a = False, relative_distance_b = False,magnitude_1, magnitude_2, distance_a, distance_b]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_TAPERED:

        load_parameter = [relative_distance_a = False, relative_distance_b = False,magnitude_1, magnitude_2, distance_a, distance_b]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_PARABOLIC:

        load_parameter = [magnitude_1, magnitude_2, magnitude_3]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_VARYING:

        load_parameter = [[distance, delta_distance, magnitude], …]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_VARYING_IN_Z:

        load_parameter = [[distance, delta_distance, magnitude], …]



    * **force_eccentricity** (*bool*) – Force Eccentricity Option


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary
    for force_eccentricity == True:

    > params = {‘eccentricity_horizontal_alignment’: MemberSetLoadEccentricityHorizontalAlignment.ALIGN_NONE,
    > ‘eccentricity_vertical_alignment’: MemberSetLoadEccentricityVerticalAlignment.ALIGN_NONE,
    > ‘eccentricity_section_middle’: MemberSetLoadEccentricitySectionMiddle.LOAD_ECCENTRICITY_SECTION_MIDDLE_CENTER_OF_GRAVITY,
    > ‘is_eccentricity_at_end_different_from_start’: False,
    > ‘eccentricity_y_at_end’: 0.0,
    > ‘eccentricity_y_at_start’: 0.0,
    > ‘eccentricity_z_at_end’: 0.0,
    > ‘eccentricity_z_at_start’: 0.0}



    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ InitialPrestress(no=1, load_case_no=1, member_sets='1', load_direction=MemberSetLoadDirection.LOAD_DIRECTION_LOCAL_X, magnitude=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **member_sets** (*str*) – Assigned Member Sets


    * **load_direction** (*enum*) – MemberSet Load Direction Enumeration


    * **magnitude** (*float*) – Load Magnitude


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Mass(no=1, load_case_no=1, member_sets='1', individual_mass_components=False, mass_components=None, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **member_sets** (*str*) – Assigned Member Sets


    * **individual_mass_components** (*bool*) – Individiual Mass Components Option


    * **mass_components** (*list*) – Mass Components


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Moment(no=1, load_case_no=1, member_sets='1', load_distribution=MemberSetLoadDistribution.LOAD_DISTRIBUTION_UNIFORM, load_direction=MemberSetLoadDirection.LOAD_DIRECTION_LOCAL_Z, load_parameter=None, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **member_sets** (*str*) – Assigned Member Sets


    * **load_distribution** (*enum*) – MemberSet Load Distribution Enumeration


    * **load_direction** (*enum*) – MemberSet Load Direction Enumeration


    * **load_parameter** (*list/list of lists*) – Load Parameters
    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_UNIFORM:

    > load_parameter = [magnitude]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_1:

        load_parameter = [relative_distance = False, magnitude, distance_a]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_N:

        load_parameter = [relative_distance_a = False, relative_distance_b = False, magnitude, count_n, distance_a, distance_b]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_2x2:

        load_parameter = [relative_distance_a = False, relative_distance_b = False, relative_distance_c = False, magnitude, distance_a, distance_b, distance_c]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_2:

        load_parameter = [relative_distance_a = False, relative_distance_b = False, magnitude_1, magnitude_2, distance_a, distance_b]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_VARYING:

        load_parameter = [[distance, delta_distance, magnitude], …]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_TRAPEZOIDAL:

        load_parameter = [relative_distance_a = False, relative_distance_b = False,magnitude_1, magnitude_2, distance_a, distance_b]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_TAPERED:

        load_parameter = [relative_distance_a = False, relative_distance_b = False,magnitude_1, magnitude_2, distance_a, distance_b]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_PARABOLIC:

        load_parameter = [magnitude_1, magnitude_2, magnitude_3]

    for load_distribution == MemberSetLoadDistribution.LOAD_DISTRIBUTION_VARYING:

        load_parameter = [[distance, delta_distance, magnitude], …]



    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ PipeContentFull(no=1, load_case_no=1, member_sets='1', load_direction_orientation=MemberSetLoadDirectionOrientation.LOAD_DIRECTION_FORWARD, specific_weight=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **member_sets** (*str*) – Assigned Member Sets


    * **load_direction_orientation** (*enum*) – MemberSet Load Direction Orientation Enumeration


    * **specific_weight** (*float*) – Specific Weight


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ PipeContentPartial(no=1, load_case_no=1, member_sets='1', load_direction_orientation=MemberSetLoadDirectionOrientation.LOAD_DIRECTION_FORWARD, specific_weight=0.0, filling_height=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **member_sets** (*str*) – Assigned Member Sets


    * **load_direction_orientation** (*enum*) – MemberSet Load Direction Orientation Enumeration


    * **specific_weight** (*float*) – Specific Weight


    * **filling_height** (*float*) – Filling Height


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ PipeInternalPressure(no=1, load_case_no=1, member_sets='1', pressure=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **member_sets** (*str*) – Assigned Member Sets


    * **pressure** (*float*) – Pressure


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Precamber(no=1, load_case_no=1, member_sets='1', load_distribution=MemberSetLoadDistribution.LOAD_DISTRIBUTION_UNIFORM, load_direction=MemberSetLoadDirection.LOAD_DIRECTION_LOCAL_Z, load_parameter=None, load_over_total_length=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **member_sets** (*str*) – Assigned Member Sets


    * **load_distribution** (*enum*) – MemberSet Load Distribution Enumeration


    * **load_direction** (*enum*) – MemberSet Load Direction Enumeration


    * **load_parameter** (*list/list of lists*) – Load Parameters
    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_UNIFORM:

    > load_parameter = [magnitude]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_TRAPEZIODAL:

        for load_over_total_length: bool= False:

            load_parameter = [magnitude_1, magnitude_2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

        for load_over_total_length: bool= True:

            load_parameter = [magnitude_1, magnitude_2]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_TAPERED:

        load_parameter = [magnitude_1, magnitude_2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_PARABOLIC:

        load_parameter = [magnitude_1, magnitude_2, magnitude_3]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_VARYING:

        load_parameter = [[distance, delta_distance, magnitude], …]



    * **load_over_total_length** (*bool*) – Load Over Total Lenth Option


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ RotaryMotion(no=1, load_case_no=1, member_sets='1', angular_acceleration=0.0, angular_velocity=0.0, axis_definition_type=MemberSetLoadAxisDefinitionType.AXIS_DEFINITION_TWO_POINTS, axis_orientation=MemberSetLoadAxisDefinitionAxisOrientation.AXIS_POSITIVE, axis_definition=MemberSetLoadAxisDefinition.AXIS_X, axis_definition_p1=None, axis_definition_p2=None, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **member_sets** (*str*) – Assigned Member Sets


    * **angular_acceleration** (*float*) – Angular Acceleration


    * **angular_velocity** (*float*) – Angular Velocity


    * **axis_definition_type** (*enum*) – MemberSet Load Axis Definition Type Enumeration


    * **axis_orientation** (*enum*) – MemberSet Load Axis Orientation Enumeration


    * **axis_definition** (*enum*) – MemberSet Load Axis Definition Enumeration


    * **axis_definition_p1** (*list*) – Axis Definition First Point


    * **axis_definition_p2** (*list*) – Axis Definition Second Point


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Rotation(no=1, load_case_no=1, member_sets='1', load_distribution=MemberSetLoadDistribution.LOAD_DISTRIBUTION_UNIFORM, load_direction=MemberSetLoadDirection.LOAD_DIRECTION_LOCAL_Z, load_parameter=None, load_over_total_length=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **member_sets** (*str*) – Assigned Member Sets


    * **load_distribution** (*enum*) – MemberSet Load Distribution Enumeration


    * **load_direction** (*enum*) – MemberSet Load Direction Enumeration


    * **load_parameter** (*list/list of lists*) – Load Parameters
    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_UNIFORM:

    > load_parameter = [magnitude]

    for load_distrubition = MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_1:

        load_parameter = [magnitude, distance_a_is_defined_as_relative = False, distance_a]

    for load_distrubition = MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_N:

        load_parameter = [magnitude, distance_a_is_defined_as_relative = False, distance_b_is_defined_as_relative = False, distance_a, distance_b]

    for load_distrubition = MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_2x2:

        load_parameter = [magnitude, distance_a_is_defined_as_relative = False, distance_b_is_defined_as_relative = False, distance_c_is_defined_as_relative = False, distance_a, distance_b, distance_c]

    for load_distrubition = MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_2:

        load_parameter = [magnitude_1, magnitude_2, distance_a_is_defined_as_relative = False, distance_b_is_defined_as_relative = False, distance_a, distance_b]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_CONCENTRATED_VARYING:

        load_parameter = [[distance, delta_distance, magnitude], …]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_TRAPEZIODAL:

        load_parameter = [magnitude_1, magnitude_2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_TAPERED:

        load_parameter = [magnitude_1, magnitude_2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_PARABOLIC:

        load_parameter = [magnitude_1, magnitude_2, magnitude_3]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_VARYING:

        load_parameter = [[distance, delta_distance, magnitude], …]



    * **load_over_total_length** (*bool*) – Load Over Total Length


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Temperature(no=1, load_case_no=1, member_sets='1', load_distribution=MemberSetLoadDistribution.LOAD_DISTRIBUTION_UNIFORM, load_direction=MemberSetLoadDirection.LOAD_DIRECTION_LOCAL_Z, load_parameter=None, load_over_total_length=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **member_sets** (*str*) – Assigned Member Sets


    * **load_distribution** (*enum*) – MemberSet Load Distribution Enumeration


    * **load_direction** (*enum*) – MemberSet Load Direction Enumeration


    * **load_parameter** (*list/list of lists*) – Load Parameters
    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_UNIFORM:

    > load_parameter = [tt, tb]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_TRAPEZIODAL:

        for load_over_total_length: bool= False:

            load_parameter = [tt1, tt2, tb1, tb2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

        for load_over_total_length: bool= True:

            load_parameter = [tt1, tt2, tb1, tb2]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_TAPERED:

        load_parameter = [tt1, tt2, tb1, tb2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_PARABOLIC:

        load_parameter = [tb1, tb2, tb3, tt1, tt2, tt3]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_VARYING:

        load_parameter = [[distance, delta_distance, magnitude], …]



    * **load_over_total_length** (*bool*) – Enable/Disable Load Over Total Length Option


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ TemperatureChange(no=1, load_case_no=1, member_sets='1', load_distribution=MemberSetLoadDistribution.LOAD_DISTRIBUTION_UNIFORM, load_direction=MemberSetLoadDirection.LOAD_DIRECTION_LOCAL_Z, load_parameter=None, load_over_total_length=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **member_sets** (*str*) – Assigned Member Sets


    * **load_distribution** (*enum*) – MemberSet Load Distribution Enumeration


    * **load_direction** (*enum*) – MemberSet Load Direction Enumeration


    * **load_parameter** (*list/list of lists*) – Load Parameters
    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_UNIFORM:

    > load_parameter = [tc, delta_t]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_TRAPEZIODAL:

        for load_over_total_length: bool= False:

            load_parameter = [delta_t_1, delta_t_2, t_c_1, t_c_2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

        for load_over_total_length: bool= True:

            load_parameter = [delta_t_1, delta_t_2, t_c_1, t_c_2]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_TAPERED:

        load_parameter = [delta_t_1, delta_t_2, t_c_1, t_c_2, distance_a_relative = False, distance_a_relative = False, a_distance, b_distance]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_PARABOLIC:

        load_parameter = [delta_t_1, delta_t_2, delta_t_3, t_c_1, t_c_2, t_c_3]

    for load_distribution = MemberSetLoadDistribution.LOAD_DISTRIBUTION_VARYING:

        load_parameter = [[distance, delta_distance, magnitude], …]



    * **load_over_total_length** (*bool*) – Load Over Total Length Option


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### \__init__(no=1, load_case_no=1, member_sets='1', load_direction=LoadDirectionType.LOAD_DIRECTION_LOCAL_Z, magnitude=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **member_sets** (*str*) – Assigned Member Sets


    * **load_direction** (*enum*) – Load Direction Enumeration


    * **magnitude** (*float*) – Load Magnitude


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## RSTAB.Loads.nodalLoad module


### _class_ RSTAB.Loads.nodalLoad.NodalLoad(no=1, load_case_no=1, nodes_no='1', load_direction=LoadDirectionType.LOAD_DIRECTION_GLOBAL_Z_OR_USER_DEFINED_W, magnitude=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### _static_ Components(no=1, load_case_no=1, nodes_no='1', components=None, specific_direction=False, force_eccentricity=False, shifted_display=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **nodes_no** (*str*) – Assigned Nodes


    * **components** (*list*) – Component Magnitude List


    * **specific_direction** (*bool*) – Enable/Disable Specific Direction Option


    * **force_eccentricity** (*bool*) – Enable/Disable Force Direction Option


    * **shifted_display** (*bool*) – Enable/Disable Shifted Display Option


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – For specific_direction type DIRECTION_TYPE_ROTATED_VIA_3_ANGLES;

        params={‘specific_direction’ : [NodalLoadSpecificDirectionType.DIRECTION_TYPE_ROTATED_VIA_3_ANGLES, NodalLoadAxesSequence, angle_1, angle_2, angle_3, angle_x, angle_y, angle_z]}

    For specific_direction type DIRECTION_TYPE_PARALLEL_TO_CS_OF_LINE;

        params={‘specific_direction’ : [NodalLoadSpecificDirectionType.DIRECTION_TYPE_PARALLEL_TO_CS_OF_LINE, line_no]}

    For specific_direction type DIRECTION_TYPE_PARALLEL_TO_CS_OF_MEMBER;

        params={‘specific_direction’ : [NodalLoadSpecificDirectionType.DIRECTION_TYPE_PARALLEL_TO_CS_OF_MEMBER, member_no]}

    For force_eccentricity;

        params={‘force_eccentricity’ : [ex, ey, ez]}

    For shifted_display;

        params={‘shifted_display’ : [offset_x, offset_y, offset_y, distance]}



    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Force(no=1, load_case_no=1, nodes_no='1', load_direction=LoadDirectionType.LOAD_DIRECTION_GLOBAL_Z_OR_USER_DEFINED_W, magnitude=0.0, force_eccentricity=False, specific_direction=False, shifted_display=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **nodes_no** (*str*) – Assigned Nodes


    * **load_direction** (*enum*) – Load Direction Enumeration


    * **magnitude** (*float*) – Force Magnitude


    * **force_eccentricity** (*bool*) – Enable/Disable Force Eccentricity Option


    * **specific_direction** (*bool*) – Enable/Disable Specific Direction Option


    * **shifted_display** (*bool*) – Enable/Disable Shifted Display Option


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – For specific_direction type DIRECTION_TYPE_ROTATED_VIA_3_ANGLES;

        params={‘specific_direction’ : [NodalLoadSpecificDirectionType.DIRECTION_TYPE_ROTATED_VIA_3_ANGLES, NodalLoadAxesSequence, angle_1, angle_2, angle_3, angle_x, angle_y, angle_z]}

    For specific_direction type DIRECTION_TYPE_DIRECTED_TO_NODE;

        params={‘specific_direction’ : [NodalLoadSpecificDirectionType.DIRECTION_TYPE_DIRECTED_TO_NODE, nodes_no]}

    For specific_direction type DIRECTION_TYPE_PARALLEL_TO_TWO_NODES;

        params={‘specific_direction’ : [NodalLoadSpecificDirectionType.DIRECTION_TYPE_PARALLEL_TO_TWO_NODES, nodes_no]}

    For specific_direction type DIRECTION_TYPE_PARALLEL_TO_CS_OF_LINE;

        params={‘specific_direction’ : [NodalLoadSpecificDirectionType.DIRECTION_TYPE_PARALLEL_TO_CS_OF_LINE, line_no]}

    For specific_direction type DIRECTION_TYPE_PARALLEL_TO_CS_OF_MEMBER;

        params={‘specific_direction’ : [NodalLoadSpecificDirectionType.DIRECTION_TYPE_PARALLEL_TO_CS_OF_MEMBER, member_no]}

    For force_eccentricity;

        params={‘force_eccentricity’ : [ex, ey, ez]}

    For shifted_display;

        params={‘shifted_display’ : [offset_x, offset_y, offset_y, distance]}



    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Mass(no=1, load_case_no=1, nodes_no='1', individual_mass_components=False, mass=None, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Load Case Number


    * **nodes_no** (*str*) – Assigned Nodes


    * **individual_mass_components** (*bool*) – Enable/Disable Mass Component Option


    * **mass** (*list*) – if individual_mass_components == False:

        mass = [M]

    elif individual_mass_components == True:

        mass = [Mx, My, Mz, Ix, Iy, Iz]



    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Moment(no=1, load_case_no=1, nodes_no='1', load_direction=LoadDirectionType.LOAD_DIRECTION_GLOBAL_Z_OR_USER_DEFINED_W, moment_magnitude=0.0, specific_direction=False, shifted_display=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **nodes_no** (*str*) – Assigned Nodes


    * **load_direction** (*enum*) – Load Direction Enumeration


    * **moment_magnitude** (*float*) – Moment Magnitude


    * **specific_direction** (*bool*) – Enable/Disable Specific Direction Option


    * **shifted_display** (*bool*) – Enable/Disable Shifted Display Option


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – For specific_direction type DIRECTION_TYPE_ROTATED_VIA_3_ANGLES;

        params={‘specific_direction’ : [NodalLoadSpecificDirectionType.DIRECTION_TYPE_ROTATED_VIA_3_ANGLES, NodalLoadAxesSequence, angle_1, angle_2, angle_3, angle_x, angle_y, angle_z]}

    For specific_direction type DIRECTION_TYPE_DIRECTED_TO_NODE;

        params={‘specific_direction’ : [NodalLoadSpecificDirectionType.DIRECTION_TYPE_DIRECTED_TO_NODE, nodes_no]}

    For specific_direction type DIRECTION_TYPE_PARALLEL_TO_TWO_NODES;

        params={‘specific_direction’ : [NodalLoadSpecificDirectionType.DIRECTION_TYPE_PARALLEL_TO_TWO_NODES, nodes_no]}

    For specific_direction type DIRECTION_TYPE_PARALLEL_TO_CS_OF_LINE;

        params={‘specific_direction’ : [NodalLoadSpecificDirectionType.DIRECTION_TYPE_PARALLEL_TO_CS_OF_LINE, line_no]}

    For specific_direction type DIRECTION_TYPE_PARALLEL_TO_CS_OF_MEMBER;

        params={‘specific_direction’ : [NodalLoadSpecificDirectionType.DIRECTION_TYPE_PARALLEL_TO_CS_OF_MEMBER, member_no]}

    For shifted_display;

        params={‘shifted_display’ : [offset_x, offset_y, offset_y, distance]}



    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### \__init__(no=1, load_case_no=1, nodes_no='1', load_direction=LoadDirectionType.LOAD_DIRECTION_GLOBAL_Z_OR_USER_DEFINED_W, magnitude=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Load Tag


    * **load_case_no** (*int*) – Assigned Load Case


    * **nodes_no** (*str*) – Assigned Nodes


    * **load_direction** (*enum*) – Load Direction Enumeration


    * **magnitude** (*float*) – Force Magnitude


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## Module contents
