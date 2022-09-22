# Basic Objects


## Material


### Material(no, name, comment, params, model)

* **Parameters**

    
    * **no** (*int*) – Material Tag


    * **name** (*str*) – Name of Desired Material (As Named in RSTAB Database)


    * **comment** (*str*, *optional*) – Comments


    * **params** (*dict*, *optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class*, *optional*) – Model to be edited


### Material.DeleteMaterial(materials_no, model)

* **Parameters**

    
    * **materials_no** (*str*) – Numbers of Materials to be deleted


    * **model** (*RSTAB Class*, *optional*) – Model to be edited



## Member


### Member(no, start_node_no, end_node_no, rotation_angle, start_section_no, end_section_no, start_member_hinge_no, end_member_hinge_no, comment, params, model)

* **Parameters**

    
    * **no** (*int*) – Member Tag


    * **start_node_no** (*int*) – Tag of Start Node


    * **end_node_no** (*int*) – Tag of End Node


    * **rotation_angle** (*float*) – Member Rotation Angle


    * **start_section_no** (*int*) – Tag of Start Section


    * **end_section_no** (*int*) – Tag of End Section


    * **start_member_hinge_no** (*int*) – Tag of Start Member Hinge


    * **end_member_hinge_no** (*int*) – Tag of End Member Hinge


    * **comment** (*str*, *optional*) – Comment


    * **params** (*dict*, *optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary



### Member.Beam(no, start_node_no, end_node_no, section_distribution_type, rotation_specification_type, rotation_parameters, start_section_no, end_section_no, distribution_parameters, comment, params, model)

* **Parameters**

    
    * **no** (*int*) – Member Tag


    * **start_node_no** (*int*) – Tag of Start Node


    * **end_node_no** (*int*) – Tag of End Node


    * **section_distribution_type** (*enum*) – Section Distribution Type Enumeration
    for section_distribution_type == MemberSectionDistributionType.SECTION_DISTRIBUTION_TYPE_LINEAR:

    > distribution_parameters = [section_alignment]

    for section_distribution_type == MemberSectionDistributionType.SECTION_DISTRIBUTION_TYPE_TAPERED_AT_BOTH_SIDES:

        distribution_parameters = [section_distance_from_start_is_defined_as_relative, section_distance_from_end_is_defined_as_relative,

            section_distance_from_start_relative/absolute, section_distance_from_end_relative/absolute,
            section_alignment, section_internal]

    for section_distribution_type == MemberSectionDistributionType.SECTION_DISTRIBUTION_TYPE_TAPERED_AT_START_OF_MEMBER:

        distribution_parameters = [section_distance_from_start_is_defined_as_relative, section_distance_from_start_relative/absolute, section_alignment]

    for section_distribution_type == MemberSectionDistributionType.SECTION_DISTRIBUTION_TYPE_TAPERED_AT_END_OF_MEMBER:

        distribution_parameters = [section_distance_from_start_is_defined_as_relative, section_distance_from_start_relative/absolute, section_alignment]

    for section_distribution_type == MemberSectionDistributionType.SECTION_DISTRIBUTION_TYPE_SADDLE:

        distribution_parameters = [section_distance_from_start_is_defined_as_relative, section_distance_from_start_relative/absolute, section_alignment, section_internal]

    for section_distribution_type == MemberSectionDistributionType.SECTION_DISTRIBUTION_TYPE_OFFSET_AT_BOTH_SIDES:

        distribution_parameters = [section_distance_from_start_is_defined_as_relative, section_distance_from_end_is_defined_as_relative,

            section_distance_from_start_relative/absolute, section_distance_from_end_relative/absolute,
            section_alignment, section_internal]

    for section_distribution_type == MemberSectionDistributionType.SECTION_DISTRIBUTION_TYPE_OFFSET_AT_START_OF_MEMBER:

        distribution_parameters = [section_distance_from_start_is_defined_as_relative, section_distance_from_start_relative/absolute, section_alignment]

    for section_distribution_type == MemberSectionDistributionType.SECTION_DISTRIBUTION_TYPE_OFFSET_AT_END_OF_MEMBER:

        distribution_parameters = [section_distance_from_start_is_defined_as_relative, section_distance_from_start_relative/absolute, section_alignment]



    * **rotation_specification_type** (*enum*) – Rotation Specification Type Enumeration


    * **rotation_parameters** (*list*) – Rotation Parameters; 1 or 2 params
    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE:

    > rotation_parameters = [rotation_angle]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_HELP_NODE:

        rotation_parameters = [rotation_help_node, rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_INSIDE_NODE:

        rotation_parameters = [rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_SURFACE:

        rotation_parameters = [rotation_surface, rotation_surface_plane_type]



    * **start_section_no** (*int*) – Tag of Start Section


    * **end_section_no** (*int*) – End of End Section


    * **distribution_parameters** (*list*) – Distribution Parameters


    * **comment** (*str*, *optional*) – Comment


    * **params** (*dict*, *optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary



#### _static_ Buckling(no=1, start_node_no=1, end_node_no=2, rotation_specification_type=MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE, rotation_parameters=[0], section_no=1, comment='', params={'end_modifications_member_end_extension': 0, 'end_modifications_member_end_slope_y': 0, 'end_modifications_member_end_slope_z': 0, 'end_modifications_member_start_extension': 0, 'end_modifications_member_start_slope_y': 0, 'end_modifications_member_start_slope_z': 0, 'is_deactivated_for_calculation': False, 'member_eccentricity_end': 0, 'member_eccentricity_start': 0, 'member_nonlinearity': 0}, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Tag


    * **start_node_no** (*int*) – Tag of Start Node


    * **end_node_no** (*int*) – Tag of End Node


    * **rotation_specification_type** (*enum*) – Rotation Specification Type Enumeration


    * **rotation_parameters** (*list*) – Rotation Parameters
    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE:

    > rotation_parameters = [rotation_angle]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_HELP_NODE:

        rotation_parameters = [rotation_help_node, rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_INSIDE_NODE:

        rotation_parameters = [rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_SURFACE:

        rotation_parameters = [rotation_surface, rotation_surface_plane_type]



    * **section_no** (*int*) – Section Tag


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary



#### _static_ Cable(no=1, start_node_no=1, end_node_no=2, rotation_specification_type=MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE, rotation_parameters=[0], section_no=1, comment='', params={'end_modifications_member_end_extension': 0, 'end_modifications_member_end_slope_y': 0, 'end_modifications_member_end_slope_z': 0, 'end_modifications_member_start_extension': 0, 'end_modifications_member_start_slope_y': 0, 'end_modifications_member_start_slope_z': 0, 'is_deactivated_for_calculation': False}, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Tag


    * **start_node_no** (*int*) – Tag of Start Node


    * **end_node_no** (*int*) – Tag of End Node


    * **rotation_specification_type** (*enum*) – Rotation Specification Type Enumeration


    * **rotation_parameters** (*list*) – Rotation Parameters
    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE:

    > rotation_parameters = [rotation_angle]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_HELP_NODE:

        rotation_parameters = [rotation_help_node, rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_INSIDE_NODE:

        rotation_parameters = [rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_SURFACE:

        rotation_parameters = [rotation_surface, rotation_surface_plane_type]



    * **section_no** (*int*) – Section Tag


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary



#### _static_ Compression(no=1, start_node_no=1, end_node_no=2, rotation_specification_type=MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE, rotation_parameters=[0], section_no=1, comment='', params={'end_modifications_member_end_extension': 0, 'end_modifications_member_end_slope_y': 0, 'end_modifications_member_end_slope_z': 0, 'end_modifications_member_start_extension': 0, 'end_modifications_member_start_slope_y': 0, 'end_modifications_member_start_slope_z': 0, 'is_deactivated_for_calculation': False, 'member_eccentricity_end': 0, 'member_eccentricity_start': 0, 'member_nonlinearity': 0}, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Tag


    * **start_node_no** (*int*) – Tag of Start Node


    * **end_node_no** (*int*) – Tag of End Node


    * **rotation_specification_type** (*enum*) – Rotation Specification Type Enumeration


    * **rotation_parameters** (*list*) – Rotation Parameters
    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE:

    > rotation_parameters = [rotation_angle]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_HELP_NODE:

        rotation_parameters = [rotation_help_node, rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_INSIDE_NODE:

        rotation_parameters = [rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_SURFACE:

        rotation_parameters = [rotation_surface, rotation_surface_plane_type]



    * **section_no** (*int*) – Section Tag


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary



#### _static_ CouplingHingeHinge(no=1, start_node_no=1, end_node_no=2, rotation_specification_type=MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE, rotation_parameters=[0], comment='', params={'is_deactivated_for_calculation': False}, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Tag


    * **start_node_no** (*int*) – Tag of Start Node


    * **end_node_no** (*int*) – Tag of End Node


    * **rotation_specification_type** (*enum*) – Rotation Specification Type Enumeration


    * **rotation_parameters** (*list*) – Rotation Parameters
    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE:

    > rotation_parameters = [rotation_angle]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_HELP_NODE:

        rotation_parameters = [rotation_help_node, rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_INSIDE_NODE:

        rotation_parameters = [rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_SURFACE:

        rotation_parameters = [rotation_surface, rotation_surface_plane_type]



    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ CouplingHingeRigid(no=1, start_node_no=1, end_node_no=2, rotation_specification_type=MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE, rotation_parameters=[0], comment='', params={'is_deactivated_for_calculation': False}, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Tag


    * **start_node_no** (*int*) – Tag of Start Node


    * **end_node_no** (*int*) – Tag of End Node


    * **rotation_specification_type** (*enum*) – Rotation Specification Type Enumeration


    * **rotation_parameters** (*list*) – Rotation Parameters
    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE:

    > rotation_parameters = [rotation_angle]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_HELP_NODE:

        rotation_parameters = [rotation_help_node, rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_INSIDE_NODE:

        rotation_parameters = [rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_SURFACE:

        rotation_parameters = [rotation_surface, rotation_surface_plane_type]



    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ CouplingRigidHinge(no=1, start_node_no=1, end_node_no=2, rotation_specification_type=MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE, rotation_parameters=[0], comment='', params={'is_deactivated_for_calculation': False}, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Tag


    * **start_node_no** (*int*) – Tag of Start Node


    * **end_node_no** (*int*) – Tag of End Node


    * **rotation_specification_type** (*enum*) – Rotation Specification Type Enumeration


    * **rotation_parameters** (*list*) – Rotation Parameters
    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE:

    > rotation_parameters = [rotation_angle]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_HELP_NODE:

        rotation_parameters = [rotation_help_node, rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_INSIDE_NODE:

        rotation_parameters = [rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_SURFACE:

        rotation_parameters = [rotation_surface, rotation_surface_plane_type]



    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ CouplingRigidRigid(no=1, start_node_no=1, end_node_no=2, rotation_specification_type=MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE, rotation_parameters=[0], comment='', params={'is_deactivated_for_calculation': False}, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Tag


    * **start_node_no** (*int*) – Tag of Start Node


    * **end_node_no** (*int*) – Tag of End Node


    * **rotation_specification_type** (*enum*) – Rotation Specification Type Enumeration


    * **rotation_parameters** (*list*) – Rotation Parameters
    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE:

    > rotation_parameters = [rotation_angle]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_HELP_NODE:

        rotation_parameters = [rotation_help_node, rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_INSIDE_NODE:

        rotation_parameters = [rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_SURFACE:

        rotation_parameters = [rotation_surface, rotation_surface_plane_type]



    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ DefinableStiffness(no=1, start_node_no=1, end_node_no=2, rotation_specification_type=MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE, rotation_parameters=[0], definable_stiffness=1, comment='', params={'is_deactivated_for_calculation': False, 'member_eccentricity_end': 0, 'member_eccentricity_start': 0, 'member_hinge_end': 0, 'member_hinge_start': 0, 'member_nonlinearity': 0, 'member_result_intermediate_point': 0}, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Tag


    * **start_node_no** (*int*) – Tag of Start Node


    * **end_node_no** (*int*) – Tag of End Node


    * **rotation_specification_type** (*enum*) – Rotation Specification Type Enumeration


    * **rotation_parameters** (*list*) – Rotation Parameters
    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE:

    > rotation_parameters = [rotation_angle]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_HELP_NODE:

        rotation_parameters = [rotation_help_node, rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_INSIDE_NODE:

        rotation_parameters = [rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_SURFACE:

        rotation_parameters = [rotation_surface, rotation_surface_plane_type]



    * **definable_stiffness** (*int*) – Definable Stiffness Tag


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ DeleteMember(members_no='1 2', model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **members_no** (*str*) – Numbers of Members to be deleted


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Rigid(no=1, start_node_no=1, end_node_no=2, rotation_specification_type=MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE, rotation_parameters=[0], comment='', params={'is_deactivated_for_calculation': False, 'member_eccentricity_end': 0, 'member_eccentricity_start': 0, 'member_hinge_end': 0, 'member_hinge_start': 0, 'member_nonlinearity': 0, 'member_result_intermediate_point': 0, 'support': 0}, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Tag


    * **start_node_no** (*int*) – Tag of Start Node


    * **end_node_no** (*int*) – Tag of End Node


    * **rotation_specification_type** (*enum*) – Rotation Specification Type Enumeration


    * **rotation_parameters** (*list*) – Rotation Parameters
    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE:

    > rotation_parameters = [rotation_angle]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_HELP_NODE:

        rotation_parameters = [rotation_help_node, rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_INSIDE_NODE:

        rotation_parameters = [rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_SURFACE:

        rotation_parameters = [rotation_surface, rotation_surface_plane_type]



    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary



#### _static_ Tension(no=1, start_node_no=1, end_node_no=2, rotation_specification_type=MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE, rotation_parameters=[0], section_no=1, comment='', params={'end_modifications_member_end_extension': 0, 'end_modifications_member_end_slope_y': 0, 'end_modifications_member_end_slope_z': 0, 'end_modifications_member_start_extension': 0, 'end_modifications_member_start_slope_y': 0, 'end_modifications_member_start_slope_z': 0, 'is_deactivated_for_calculation': False, 'member_eccentricity_end': 0, 'member_eccentricity_start': 0, 'member_nonlinearity': 0}, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Tag


    * **start_node_no** (*int*) – Tag of Start Node


    * **end_node_no** (*int*) – Tag of End Node


    * **rotation_specification_type** (*enum*) – Rotation Specification Type Enumeration


    * **rotation_parameters** (*list*) – Rotation Parameters
    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE:

    > rotation_parameters = [rotation_angle]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_HELP_NODE:

        rotation_parameters = [rotation_help_node, rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_INSIDE_NODE:

        rotation_parameters = [rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_SURFACE:

        rotation_parameters = [rotation_surface, rotation_surface_plane_type]



    * **section_no** (*int*) – Section Tag


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary



#### _static_ Truss(no=1, start_node_no=1, end_node_no=2, rotation_specification_type=MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE, rotation_parameters=[0], section_no=1, comment='', params={'end_modifications_member_end_extension': 0, 'end_modifications_member_end_slope_y': 0, 'end_modifications_member_end_slope_z': 0, 'end_modifications_member_start_extension': 0, 'end_modifications_member_start_slope_y': 0, 'end_modifications_member_start_slope_z': 0, 'is_deactivated_for_calculation': False, 'member_eccentricity_end': 0, 'member_eccentricity_start': 0, 'member_nonlinearity': 0}, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Tag


    * **start_node_no** (*int*) – Tag of Start Node


    * **end_node_no** (*int*) – Tag of End Node


    * **rotation_specification_type** (*enum*) – Rotation Specification Type Enumeration


    * **rotation_parameters** (*list*) – Rotation Parameters
    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE:

    > rotation_parameters = [rotation_angle]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_HELP_NODE:

        rotation_parameters = [rotation_help_node, rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_INSIDE_NODE:

        rotation_parameters = [rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_SURFACE:

        rotation_parameters = [rotation_surface, rotation_surface_plane_type]



    * **section_no** (*int*) – Section Tag


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary



#### _static_ TrussOnlyN(no=1, start_node_no=1, end_node_no=2, rotation_specification_type=MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE, rotation_parameters=[0], section_no=1, comment='', params={'end_modifications_member_end_extension': 0, 'end_modifications_member_end_slope_y': 0, 'end_modifications_member_end_slope_z': 0, 'end_modifications_member_start_extension': 0, 'end_modifications_member_start_slope_y': 0, 'end_modifications_member_start_slope_z': 0, 'is_deactivated_for_calculation': False, 'member_eccentricity_end': 0, 'member_eccentricity_start': 0, 'member_nonlinearity': 0}, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Tag


    * **start_node_no** (*int*) – Tag of Start Node


    * **end_node_no** (*int*) – Tag of End Node


    * **rotation_specification_type** (*enum*) – Rotation Specification Type Enumeration


    * **rotation_parameters** (*list*) – Rotation Parameters
    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_ANGLE:

    > rotation_parameters = [rotation_angle]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_HELP_NODE:

        rotation_parameters = [rotation_help_node, rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_INSIDE_NODE:

        rotation_parameters = [rotation_plane_type]

    for rotation_specification_type == MemberRotationSpecificationType.COORDINATE_SYSTEM_ROTATION_VIA_SURFACE:

        rotation_parameters = [rotation_surface, rotation_surface_plane_type]



    * **section_no** (*int*) – Section Tag


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary




## RSTAB.BasicObjects.memberSet module


### _class_ RSTAB.BasicObjects.memberSet.MemberSet(no=1, members_no='1 4 5 8 9 12 13 16 17 20 21 24', member_set_type=SetType.SET_TYPE_GROUP, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### _static_ ContinuousMembers(no=1, members_no='1 4 5 8 9 12 13 16 17 20 21 24', comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Set Tag


    * **members_no** (*str*) – Numbers of Members Contained Within Continuous Member Set


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ GroupOfmembers(no=1, members_no='1 4 5 8 9 12 13 16 17 20 21 24', comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Set Tag


    * **members_no** (*str*) – Numbers of Members Contained Within Group of Members Member Set


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### \__init__(no=1, members_no='1 4 5 8 9 12 13 16 17 20 21 24', member_set_type=SetType.SET_TYPE_GROUP, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Member Set Tag


    * **members_no** (*str*) – Numbers of Members Contained Within Member Set


    * **member_set_type** (*enum*) – Member Set Type Enumeration


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## RSTAB.BasicObjects.node module


### _class_ RSTAB.BasicObjects.node.Node(no=1, coordinate_X=0.0, coordinate_Y=0.0, coordinate_Z=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### _static_ BetweenTwoNodes(no=1, start_node_no=1, end_node_no=2, node_reference=NodeReferenceType.REFERENCE_TYPE_L, length_between_i_and_j=1, parameters=[True, 50], offset_y=0, offset_z=0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Node Tag


    * **start_node_no** (*int*) – Start Node


    * **end_node_no** (*int*) – End Node


    * **node_reference** (*enum*) – Node Reference Enumeration


    * **length_between_i_and_j** (*float*) – Length between 2 Nodes


    * **parameters** (*list*) – if distance_from_start_relative:

        parameters = [True, %]

    if distance_from_start_absolute:

        parameters = [False, magnitude]



    * **offset_y** (*float*) – Offset in Y-Direction


    * **offset_z** (*float*) – Offset in Z-Direction


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ BetweenTwoPoints(no=1, start_point_x=0.0, start_point_y=0.0, start_point_z=0.0, end_point_x=1.0, end_point_y=1.0, end_point_z=1.0, node_reference=NodeReferenceType.REFERENCE_TYPE_L, parameters=[True, 0.5], offset_y=0.0, offset_z=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Node Tag


    * **start_point_x** (*float*) – Start Point in X-Coordinate


    * **start_point_y** (*float*) – Start Point in Y-Coordinate


    * **start_point_z** (*float*) – Start Point in Z-Coordinate


    * **end_point_x** (*float*) – End Point in X-Coordinate


    * **end_point_y** (*float*) – End Point in Y-Coordinate


    * **end_point_z** (*float*) – End Point in Z-Coordinate


    * **node_reference** (*enum*) – Node Reference Enumeration


    * **parameters** (*list*) – if distance_from_start_relative:

        parameters = [True, %]

    if distance_from_start_absolute:

        parameters = [False, magnitude]



    * **offset_y** (*float*) – Offset in Y-Direction


    * **offset_z** (*float*) – Offset in Z-Direction


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ DeleteNode(nodes_no='1 2', model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **nodes_no** (*str*) – Numbers of Nodes to be deleted


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ OnMember(no=1, member_number=1, node_reference=NodeReferenceType.REFERENCE_TYPE_L, length_between_i_and_j=1, parameters=[True, 0.5], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Node Tag


    * **member_number** (*int*) – Member Tag


    * **node_reference** (*enum*) – Node Reference Enumeration


    * **length_between_i_and_j** (*int*) – Length between 2 Nodes


    * **parameters** (*list*) – if distance_from_start_relative:

        parameters = [True, %]

    if distance_from_start_absolute:

        parameters = [False, magnitude]



    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Standard(no=1, coordinate_system=None, coordinate_system_type=NodeCoordinateSystemType.COORDINATE_SYSTEM_CARTESIAN, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Node Tag


    * **coordinate_system** (*list*) – Coordinate System
    for coordinate_system_type == NodeCoordinateSystemType.COORDINATE_SYSTEM_CARTESIAN;

    > coordinate_system = [X, Y, Z]

    for coordinate_system_type == NodeCoordinateSystemType.COORDINATE_SYSTEM_X_CYLINDRICAL;

        coordinate_system = [X, R, θ]

    for coordinate_system_type == NodeCoordinateSystemType.COORDINATE_SYSTEM_Y_CYLINDRICAL;

        coordinate_system = [R, Ύ, θ]

    for coordinate_system_type == NodeCoordinateSystemType.COORDINATE_SYSTEM_Z_CYLINDRICAL;

        coordinate_system = [R, θ, Z]

    for coordinate_system_type == NodeCoordinateSystemType.COORDINATE_SYSTEM_POLAR:

        coordinate_system = [R, θ, φ]



    * **coordinate_system_type** (*enum*) – Coordinate System Type Enumeration


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### \__init__(no=1, coordinate_X=0.0, coordinate_Y=0.0, coordinate_Z=0.0, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Node Tag


    * **coordinate_X** (*float*) – X-Coordinate


    * **coordinate_Y** (*float*) – Y-Coordinate


    * **coordinate_Z** (*float*) – Z-Coordinate


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## RSTAB.BasicObjects.section module


### _class_ RSTAB.BasicObjects.section.Section(no=1, name='IPE 300', material_no=1, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### _static_ DeleteSection(sections_no='1 2', model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **sections_no** (*str*) – Numbers of Sections to be deleted


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### \__init__(no=1, name='IPE 300', material_no=1, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Section Tag


    * **name** (*str*) – Name of Desired Section (As Named in RSTAB Database)


    * **material_no** (*int*) – Tag of Material assigned to Section


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## Module contents
