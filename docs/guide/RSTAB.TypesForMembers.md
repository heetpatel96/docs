# RSTAB.TypesForMembers package

## Submodules

## RSTAB.TypesForMembers.memberDefinableStiffness module


### _class_ RSTAB.TypesForMembers.memberDefinableStiffness.MemberDefinableStiffness(no=1, name='', members='1', torsional_stiffness=0.0, bending_stiffness_y=0.0, bending_stiffness_z=0.0, axial_stiffness=0.0, shear_stiffness_y=0.0, shear_stiffness_z=0.0, specific_weight=0.0, section_area=0.0, rotation=0.0, thermal_expansion_alpha=0.0, thermal_expansion_width=0.0, thermal_expansion_height=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(no=1, name='', members='1', torsional_stiffness=0.0, bending_stiffness_y=0.0, bending_stiffness_z=0.0, axial_stiffness=0.0, shear_stiffness_y=0.0, shear_stiffness_z=0.0, specific_weight=0.0, section_area=0.0, rotation=0.0, thermal_expansion_alpha=0.0, thermal_expansion_width=0.0, thermal_expansion_height=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Definable Stiffness Tag


    * **name** (*str*) – User Defined Name


    * **members** (*str*) – Assigned Members


    * **torsional_stiffness** (*float*) – Torsional Stiffness


    * **bending_stiffness_y** (*float*) – Bending Stiffness in Y Direction


    * **bending_stiffness_z** (*float*) – Bendign Stiffness in Z Direction


    * **axial_stiffness** (*float*) – Axial Stiffness


    * **shear_stiffness_y** (*float*) – Shear Stiffness in Y Direction


    * **shear_stiffness_z** (*float*) – Shear Stiffness in Z Direction


    * **specific_weight** (*float*) – Specific Weight


    * **section_area** (*float*) – Section Area


    * **rotation** (*float*) – Rotation


    * **thermal_expansion_alpha** (*float*) – Thermal Expansion Alpha Coefficient


    * **thermal_expansion_width** (*float*) – Thermal Expansion Witdh Coefficient


    * **thermal_expansion_height** (*float*) – Thermal Expansion Height Coefficient


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## RSTAB.TypesForMembers.memberEccentricity module


### _class_ RSTAB.TypesForMembers.memberEccentricity.MemberEccentricity(no=1, name='', eccentricity_type=MemberEccentricitySpecificationType.TYPE_RELATIVE, eccentricity_parameters=[<MemberEccentricityHorizontalSectionAlignment.ALIGN_MIDDLE: 1>, <MemberEccentricityVerticalSectionAlignment.ALIGN_MIDDLE: 1>], transverse_offset_type=MemberEccentricityTransverseOffsetType.TRANSVERSE_OFFSET_TYPE_NONE, transverse_offset_parameters=None, axial_offset_active=False, hinge_location_at_node=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(no=1, name='', eccentricity_type=MemberEccentricitySpecificationType.TYPE_RELATIVE, eccentricity_parameters=[<MemberEccentricityHorizontalSectionAlignment.ALIGN_MIDDLE: 1>, <MemberEccentricityVerticalSectionAlignment.ALIGN_MIDDLE: 1>], transverse_offset_type=MemberEccentricityTransverseOffsetType.TRANSVERSE_OFFSET_TYPE_NONE, transverse_offset_parameters=None, axial_offset_active=False, hinge_location_at_node=False, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Eccentricity Tag


    * **name** (*list*) – User Defined Name


    * **eccentricity_type** (*enum*) – Member Eccentricity Specification Type Enumeration


    * **eccentricity_parameters** (*list*) – Eccentricity Parameters List
    for eccentricity_type == MemberEccentricitySpecificationType.TYPE_RELATIVE:

    > eccentricity_parameters = [horizontal_section_alignment, vertical_section_alignment]

    for eccentricity_type == MemberEccentricitySpecificationType.TYPE_ABSOLUTE:

        eccentricity_parameters = [coordinate_system, offset_x, offset_y, offset_z]

    for eccentricity_type == MemberEccentricitySpecificationType.TYPE_RELATIVE_AND_ABSOLUTE:

        eccentricity_parameters = [coordinate_system, offset_x, offset_y, offset_z, horizontal_section_alignment, vertical_section_alignment]



    * **transverse_offset_type** (*enum*) – Member Eccentricity Transverse Offset Type Enumeration


    * **transverse_offset_parameters** (*list*) – Transverse Offset Parameters List
    for transverse_offset_type == MemberEccentricityTransverseOffsetType.TRANSVERSE_OFFSET_TYPE_NONE:

    > transverse_offset_parameters = None

    for transverse_offset_type == MemberEccentricityTransverseOffsetType.TRANSVERSE_OFFSET_TYPE_FROM_SURFACE_THICKNESS:

        transverse_offset_parameters = [transverse_offset_reference_surface, transverse_offset_vertical_alignment]

    for transverse_offset_type == MemberEccentricityTransverseOffsetType.TRANSVERSE_OFFSET_TYPE_FROM_MEMBER_SECTION:

        transverse_offset_parameters = [transverse_offset_reference_member, transverse_offset_member_reference_node, transverse_offset_horizontal_alignment, transverse_offset_vertical_alignment]



    * **axial_offset_active** (*bool*) – Enable/Disable Axial Offset


    * **hinge_location_at_node** (*bool*) – Enable/Disable Hinge Location at Node


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## RSTAB.TypesForMembers.memberHinge module


### _class_ RSTAB.TypesForMembers.memberHinge.MemberHinge(no=1, coordinate_system='Local', member='', translational_release_n=inf, translational_release_vy=inf, translational_release_vz=inf, rotational_release_mt=inf, rotational_release_my=0.0, rotational_release_mz=0.0, translational_release_n_nonlinearity=[<MemberHingeNonlineartiy.NONLINEARITY_TYPE_NONE: 10>], translational_release_vy_nonlinearity=[<MemberHingeNonlineartiy.NONLINEARITY_TYPE_NONE: 10>], translational_release_vz_nonlinearity=[<MemberHingeNonlineartiy.NONLINEARITY_TYPE_NONE: 10>], rotational_release_mt_nonlinearity=[<MemberHingeNonlineartiy.NONLINEARITY_TYPE_NONE: 10>], rotational_release_my_nonlinearity=[<MemberHingeNonlineartiy.NONLINEARITY_TYPE_NONE: 10>], rotational_release_mz_nonlinearity=[<MemberHingeNonlineartiy.NONLINEARITY_TYPE_NONE: 10>], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(no=1, coordinate_system='Local', member='', translational_release_n=inf, translational_release_vy=inf, translational_release_vz=inf, rotational_release_mt=inf, rotational_release_my=0.0, rotational_release_mz=0.0, translational_release_n_nonlinearity=[<MemberHingeNonlineartiy.NONLINEARITY_TYPE_NONE: 10>], translational_release_vy_nonlinearity=[<MemberHingeNonlineartiy.NONLINEARITY_TYPE_NONE: 10>], translational_release_vz_nonlinearity=[<MemberHingeNonlineartiy.NONLINEARITY_TYPE_NONE: 10>], rotational_release_mt_nonlinearity=[<MemberHingeNonlineartiy.NONLINEARITY_TYPE_NONE: 10>], rotational_release_my_nonlinearity=[<MemberHingeNonlineartiy.NONLINEARITY_TYPE_NONE: 10>], rotational_release_mz_nonlinearity=[<MemberHingeNonlineartiy.NONLINEARITY_TYPE_NONE: 10>], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Hinge Tag


    * **coordinate_system** (*str*) – Coordinate System Selection


    * **member** (*str*) – Assigned Members


    * **translational_release_n** (*float*) – Translational Spring Constant X


    * **translational_release_vy** (*float*) – Translational Spring Constant Y


    * **translational_release_vz** (*float*) – Translational Spring Constant Z


    * **rotational_release_mt** (*float*) – Rotational Spring Constant X


    * **rotational_release_my** (*float*) – Rotational Spring Constant Y


    * **rotational_release_mz** (*float*) – Rotational Spring Constant Z


    * **translational_release_n_nonlinearity** (*list*) – Nonlinearity Options Translational X


    * **translational_release_vy_nonlinearity** (*list*) – Nonlinearity Options Translational Y


    * **translational_release_vz_nonlinearity** (*list*) – Nonlinearity Options Translational Z


    * **rotational_release_mt_nonlinearity** (*list*) – Nonlinearity Options Rotational X


    * **rotational_release_my_nonlinearity** (*list*) – Nonlinearity Options Rotational Y


    * **rotational_release_mz_nonlinearity** (*list*) – Nonlinearity Options Rotational Z


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## RSTAB.TypesForMembers.memberNonlinearity module


### _class_ RSTAB.TypesForMembers.memberNonlinearity.MemberNonlinearity(no=1, members='', nonlinearity_type=MemberNonlinearityType.TYPE_FAILURE_IF_TENSION, parameters=None, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(no=1, members='', nonlinearity_type=MemberNonlinearityType.TYPE_FAILURE_IF_TENSION, parameters=None, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Nonlinearity Tag


    * **members** (*str*) – Assigned Members


    * **nonlinearity_type** (*enum*) – Member Nonlinearity Type Enumeration Item


    * **parameters** (*list*) – Nonlinearity Parameters


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## RSTAB.TypesForMembers.memberResultIntermediatePoints module


### _class_ RSTAB.TypesForMembers.memberResultIntermediatePoints.MemberResultIntermediatePoint(no=1, members='', point_count=2, uniform_distribution=True, distances=None, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(no=1, members='', point_count=2, uniform_distribution=True, distances=None, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Result Intermediate Point Tag


    * **members** (*str*) – Assigned Members


    * **point_count** (*int*) – Assigned Point Number


    * **uniform_distribution** (*bool*) – Uniform Distrubition Option


    * **distances** (*list of lists*) – Distances Table


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## RSTAB.TypesForMembers.memberStiffnessModification module


### _class_ RSTAB.TypesForMembers.memberStiffnessModification.MemberStiffnessModification(no=1, assigned_structure_modification='', modification_type=MemberStiffnessModificationType.TYPE_TOTAL_STIFFNESSES_FACTORS, parameters=[1.0], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(no=1, assigned_structure_modification='', modification_type=MemberStiffnessModificationType.TYPE_TOTAL_STIFFNESSES_FACTORS, parameters=[1.0], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Modification Tag


    * **assigned_structure_modification** (*str*) – Assigned Structure Modification


    * **modification_type** (*enum*) – Member Stiffness Modification Type Enumeration Item


    * **parameters** (*list*) – Parameters List
    for modification_type == “TYPE_TOTAL_STIFFNESSES_FACTORS”:

    > parameters = [total_stiffness_factor]

    for modification_type == “TYPE_PARTIAL_STIFFNESSES_FACTORS”:

        parameters = [factor_of_axial_stiffness, factor_of_bending_y_stiffness, factor_of_bending_z_stiffness, partial_stiffness_factor_of_shear_y_stiffness,

            partial_stiffness_factor_of_shear_z_stiffness, partial_stiffness_factor_of_torsion_stiffness, partial_stiffness_factor_of_weight]

    for modification_type == “TYPE_CONCRETE_STRUCTURES_ACI”:

        parameters = [concrete_structure_component_type, factor_of_axial_stiffness, factor_of_bending_y_stiffness, factor_of_bending_z_stiffness]

    for modification_type == “TYPE_CONCRETE_STRUCTURES_CSA”:

        parameters = [concrete_structure_component_type, factor_of_axial_stiffness, factor_of_bending_y_stiffness, factor_of_bending_z_stiffness]

    for modification_type = “TYPE_STEEL_STRUCTURES”:

        parameters = [steel_structure_determine_tau_b, steel_structure_design_method]

    for modification_type = “TYPE_STEEL_STRUCTURES_CSA”:

        parameters = [steel_structure_csa_determine_tau_b, factor_of_axial_stiffness, factor_of_bending_z_stiffness, steel_structure_csa_stiffness_factor_of_shear_y_stiffness,

            steel_structure_csa_stiffness_factor_of_shear_z_stiffness, steel_structure_csa_stiffness_factor_of_torsion_stiffness]



    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## RSTAB.TypesForMembers.memberSupport module


### _class_ RSTAB.TypesForMembers.memberSupport.MemberSupport(no=1, members='', spring_translation_x=0.0, spring_translation_y=0.0, spring_translation_z=[inf, <MemberSupportNonlinearity.NONLINEARITY_NONE: 2>], spring_rotation=0.0, spring_shear_x=0.0, spring_shear_y=0.0, spring_shear_z=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(no=1, members='', spring_translation_x=0.0, spring_translation_y=0.0, spring_translation_z=[inf, <MemberSupportNonlinearity.NONLINEARITY_NONE: 2>], spring_rotation=0.0, spring_shear_x=0.0, spring_shear_y=0.0, spring_shear_z=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Support Tag


    * **members** (*str*) – Assigned Members


    * **spring_translation_x** (*float*) – Translational X Spring Constant


    * **spring_translation_y** (*float*) – Translational Y Spring Constant


    * **spring_translation_z** (*list*) – [Translational Z Spring Constant, Nonlinearity Type]


    * **spring_rotation** (*float*) – Rotational Spring Constant


    * **spring_shear_x** (*float*) – Shear X Spring Constant


    * **spring_shear_y** (*float*) – Shear Y Spring Constant


    * **spring_shear_z** (*float*) – Shear Z Spring Constant


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## RSTAB.TypesForMembers.memberTransverseStiffeners module


### _class_ RSTAB.TypesForMembers.memberTransverseStiffeners.MemberTransverseStiffeners(no=1, members='', member_sets='', components=[{'no': 1, 'cantilever_l_c': 0, 'stiffener_type': <MemberTransverseStiffenerType.STIFFENER_COMPONENT_TYPE_FLAT: 6>, 'position': 1, 'position_type': <MemberTransverseStiffenerPosition.STIFFENER_COMPONENT_POSITION_DOUBLE_SIDED: 0>, 'multiple': False, 'multiple_number': 0, 'definition_type': <MemberTransverseStiffenerDefinitionType.DIMENSION_TYPE_OFFSET: 0>, 'multiple_offset_definition_type': <MemberTransverseStiffenerOffsetType.OFFSET_DEFINITION_TYPE_ABSOLUTE: 0>, 'multiple_offset': 0, 'material': 1, 'consider_stiffener': True, 'thickness': 0.005, 'width': 0.02, 'height': 0, 'non_rigid': False, 'rigid': False, 'width_b_u': 0, 'height_h_u': 0, 'thickness_t_u': 0, 'thickness_s_u': 0, 'width_b': 0, 'thickness_t': 0, 'column_section': 0, 'section': 0, 'full_warping_restraint': False, 'user_defined_restraint': False, 'user_defined_restraint_value': 0, 'note': 'comment'}], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(no=1, members='', member_sets='', components=[{'no': 1, 'cantilever_l_c': 0, 'stiffener_type': <MemberTransverseStiffenerType.STIFFENER_COMPONENT_TYPE_FLAT: 6>, 'position': 1, 'position_type': <MemberTransverseStiffenerPosition.STIFFENER_COMPONENT_POSITION_DOUBLE_SIDED: 0>, 'multiple': False, 'multiple_number': 0, 'definition_type': <MemberTransverseStiffenerDefinitionType.DIMENSION_TYPE_OFFSET: 0>, 'multiple_offset_definition_type': <MemberTransverseStiffenerOffsetType.OFFSET_DEFINITION_TYPE_ABSOLUTE: 0>, 'multiple_offset': 0, 'material': 1, 'consider_stiffener': True, 'thickness': 0.005, 'width': 0.02, 'height': 0, 'non_rigid': False, 'rigid': False, 'width_b_u': 0, 'height_h_u': 0, 'thickness_t_u': 0, 'thickness_s_u': 0, 'width_b': 0, 'thickness_t': 0, 'column_section': 0, 'section': 0, 'full_warping_restraint': False, 'user_defined_restraint': False, 'user_defined_restraint_value': 0, 'note': 'comment'}], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Transverse Stiffener Tag


    * **members** (*str*) – Assigned Members


    * **member_sets** (*str*) – Assigned Member Sets


    * **components** (*list of components*) – List of components dictionary


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### component(_ = {'cantilever_l_c': 0, 'column_section': 0, 'consider_stiffener': True, 'definition_type': MemberTransverseStiffenerDefinitionType.DIMENSION_TYPE_OFFSET, 'full_warping_restraint': False, 'height': 0, 'height_h_u': 0, 'material': 1, 'multiple': False, 'multiple_number': 0, 'multiple_offset': 0, 'multiple_offset_definition_type': MemberTransverseStiffenerOffsetType.OFFSET_DEFINITION_TYPE_ABSOLUTE, 'no': 1, 'non_rigid': False, 'note': 'comment', 'position': 1, 'position_type': MemberTransverseStiffenerPosition.STIFFENER_COMPONENT_POSITION_DOUBLE_SIDED, 'rigid': False, 'section': 0, 'stiffener_type': MemberTransverseStiffenerType.STIFFENER_COMPONENT_TYPE_FLAT, 'thickness': 0.005, 'thickness_s_u': 0, 'thickness_t': 0, 'thickness_t_u': 0, 'user_defined_restraint': False, 'user_defined_restraint_value': 0, 'width': 0.02, 'width_b': 0, 'width_b_u': 0_ )
## Module contents
