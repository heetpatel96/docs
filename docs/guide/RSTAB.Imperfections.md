# RSTAB.Imperfections package

## Submodules

## RSTAB.Imperfections.imperfectionCase module


### _class_ RSTAB.Imperfections.imperfectionCase.ImperfectionCase(no=1, type=ImperfectionType.IMPERFECTION_TYPE_LOCAL_IMPERFECTIONS, assigned_to_load_cases='', assigned_to_load_combinations='', assign_to_combinations_without_assigned_imperfection_case=True, active=True, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### _static_ Group(no=1, assigned_to_load_cases='', assigned_to_load_combinations='', assign_to_combinations_without_assigned_imperfection_case=True, imperfection_cases=[{'no': 1, 'name': 1, 'factor': 1.1, 'operator_type': 'OPERATOR_NONE', 'comment': ''}], active=True, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Imperfection Case


* **Parameters**

    
    * **no** (*int*) – Imperfection Case Tag


    * **assigned_to_load_cases** (*str**, **optional*) – Assigned to Load Case


    * **assigned_to_load_combinations** (*str**, **optional*) – Assigned to Load Combinations


    * **assign_to_combinations_without_assigned_imperfection_case** (*bool*) – Assign to all Load Combinations without assigned Imperfection Case


    * **imperfection_cases** (*list*) – Imperfection Cases items


    * **active** (*bool*) – Active


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ InitialSwayViaTable(no=1, assigned_to_load_cases='', assigned_to_load_combinations='', assign_to_combinations_without_assigned_imperfection_case=True, direction=ImperfectionCaseDirection.IMPERFECTION_CASE_DIRECTION_GLOBAL_Z_OR_USER_DEFINED_W_TRUE, direction_for_level_direction=DirectionForLevelDirection.DIRECTION_X, coordinate_system=1, sway_coefficients_reciprocal=True, level_imperfections=[{'no': 1, 'level': 3, 'e_1': 0, 'theta_1': 0, 'e_2': 0, 'theta_2': 0, 'comment': ''}], active=True, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Imperfection Case Initial Sway via Table


* **Parameters**

    
    * **no** (*int*) – Imperfection Case Tag


    * **assigned_to_load_cases** (*str**, **optional*) – Assigned to Load Case


    * **assigned_to_load_combinations** (*str**, **optional*) – Assigned to Load Combinations


    * **assign_to_combinations_without_assigned_imperfection_case** (*bool*) – Assign to all Load Combinations without assigned Imperfection Case


    * **direction** (*enum*) – Imperfection Case Direction Enumeration


    * **direction_for_level_direction** (*enum*) – Direction For Level Direction Enumeration


    * **coordinate_system** (*int*) – Coordinate system


    * **sway_coefficients_reciprocal** (*bool*) – Sway Coefficient as reciprocal of 1


    * **level_imperfections** (*list*) – Level Imperfections


    * **active** (*bool*) – Active


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ Local(no=1, assigned_to_load_combinations='', assigned_to_load_cases='', comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Imperfection Case Local Imperfections


* **Parameters**

    
    * **no** (*int*) – Imperfection Case Tag


    * **assigned_to_load_combinations** (*str**, **optional*) – Assigned Load Combinations


    * **assigned_to_load_cases** (*str**, **optional*) – Assigned Load Cases


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ NotionalLoads(no=1, assigned_to_load_cases='', assigned_to_load_combinations='', assign_to_combinations_without_assigned_imperfection_case=True, load_case_for_notional_loads=1, active=True, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Imperfection Case


* **Parameters**

    
    * **no** (*int*) – Imperfection Case Tag


    * **assigned_to_load_cases** (*str**, **optional*) – Assigned to Load Case


    * **assigned_to_load_combinations** (*str**, **optional*) – Assigned to Load Combinations


    * **assign_to_combinations_without_assigned_imperfection_case** (*bool*) – Assign to all Load Combinations without assigned Imperfection Case


    * **load_case_for_notional_loads** (*int*) – Load Case for Notional Loads


    * **active** (*bool*) – Active


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### _static_ StaticDeformation(no=1, assigned_to_load_cases='', assigned_to_load_combinations='', assign_to_combinations_without_assigned_imperfection_case=True, direction=ImperfectionCaseDirection.IMPERFECTION_CASE_DIRECTION_GLOBAL_Z_OR_USER_DEFINED_W_TRUE, coordinate_system=1, source=ImperfectionCaseSourceType.SOURCE_TYPE_LOAD_CASE, imperfection_shape_from=1, imperfection_magnitude=0.3, magnitude_assignment_type=ImperfectionCaseAssignmentType.MAGNITUDE_ASSIGNMENT_SPECIFIC_NODE, reference_node=None, active=True, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Static Deformation Type


* **Parameters**

    
    * **no** (*int*) – Imperfection Case Tag


    * **assigned_to_load_cases** (*str**, **optional*) – Assigned to Load Case


    * **assigned_to_load_combinations** (*str**, **optional*) – Assigned to Load Combinations


    * **assign_to_combinations_without_assigned_imperfection_case** (*bool*) – Assign to all Load Combinations without assigned Imperfection Case


    * **direction** (*enum*) – Imperfection Case Direction Enumeration


    * **coordinate_system** (*int*) – Coordinate System


    * **source** (*enum*) – Imperfection Case Source Type Enumeration


    * **imperfection_shape_from** (*int*) – Imperfection Shape From


    * **imperfection_magnitude** (*float*) – Imperfection Magnitude


    * **magnitude_assignment_type** (*enum*) – Imperfection Case Assignment Type Enumeration


    * **reference_node** (*int*) – Reference Node


    * **active** (*bool*) – Active


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### \__init__(no=1, type=ImperfectionType.IMPERFECTION_TYPE_LOCAL_IMPERFECTIONS, assigned_to_load_cases='', assigned_to_load_combinations='', assign_to_combinations_without_assigned_imperfection_case=True, active=True, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Imperfection Case


* **Parameters**

    
    * **no** (*int*) – Imperfection Case Tag


    * **type** (*enum*) – Imperfection Type


    * **assigned_to_load_cases** (*str**, **optional*) – Assigned to Load Case


    * **assigned_to_load_combinations** (*str**, **optional*) – Assigned to Load Combinations


    * **assign_to_combinations_without_assigned_imperfection_case** (*bool*) – Assign to all Load Combinations without Assigned Imperfection Case


    * **active** (*bool*) – Active


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### imperfection_case_item(_: dic_ _ = {'comment': '', 'factor': 1.1, 'name': 1, 'no': 1, 'operator_type': 'OPERATOR_NONE'_ )

#### level_imperfection_item(_: dic_ _ = {'comment': '', 'e_1': 0, 'e_2': 0, 'level': 3, 'no': 1, 'theta_1': 0, 'theta_2': 0_ )
## RSTAB.Imperfections.memberImperfection module


### _class_ RSTAB.Imperfections.memberImperfection.MemberImperfection(no=1, imperfection_case=1, members='1', imperfection_type=MemberImperfectionType.IMPERFECTION_TYPE_INITIAL_SWAY, definition_type=MemberImperfectionDefinitionType.DEFINITION_TYPE_ABSOLUTE, imperfection_direction=ImperfectionDirection.IMPERFECTION_DIRECTION_LOCAL_Z, parameters=[0.035], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(no=1, imperfection_case=1, members='1', imperfection_type=MemberImperfectionType.IMPERFECTION_TYPE_INITIAL_SWAY, definition_type=MemberImperfectionDefinitionType.DEFINITION_TYPE_ABSOLUTE, imperfection_direction=ImperfectionDirection.IMPERFECTION_DIRECTION_LOCAL_Z, parameters=[0.035], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Member Imperfection
An imperfection case must be created before.


* **Parameters**

    
    * **no** (*int*) – Member Imperfection Tag


    * **imperfection_case** (*int*) – Imperfection Case Number


    * **members** (*str*) – Assigned to Members


    * **imperfection_type** (*enum*) – Member Imperfection Type Enumeration


    * **definition_type** (*enum*) – Member Imperfection Definition Type Enumeration


    * **imperfection_direction** (*enum*) – Imperfection Direction Enumeration


    * **parameters** (*list*) – Parameters depending on Imperfection and Definition type


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## RSTAB.Imperfections.membersetImperfection module


### _class_ RSTAB.Imperfections.membersetImperfection.MemberSetImperfection(no=1, imperfection_case=1, member_sets='1', imperfection_type=MemberImperfectionType.IMPERFECTION_TYPE_INITIAL_SWAY, definition_type=MemberImperfectionDefinitionType.DEFINITION_TYPE_ABSOLUTE, imperfection_direction=ImperfectionDirection.IMPERFECTION_DIRECTION_LOCAL_Z, parameters=[0.0022], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(no=1, imperfection_case=1, member_sets='1', imperfection_type=MemberImperfectionType.IMPERFECTION_TYPE_INITIAL_SWAY, definition_type=MemberImperfectionDefinitionType.DEFINITION_TYPE_ABSOLUTE, imperfection_direction=ImperfectionDirection.IMPERFECTION_DIRECTION_LOCAL_Z, parameters=[0.0022], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Member Imperfection
An imperfection case must be created before.


* **Parameters**

    
    * **no** (*int*) – Member Set Imperfection Tag


    * **imperfection_case** (*int*) – Imperfection Case Number


    * **member_sets** (*str*) – Assigned to Member Sets


    * **imperfection_type** (*enum*) – Member Imperfection Type Enumeration


    * **definition_type** (*enum*) – Member Imperfection Definition Type Enumeration


    * **imperfection_direction** (*enum*) – Imperfection Direction Enumeration


    * **parameters** (*list*) – Parameters depending on Imperfection and Definition type


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## Module contents
