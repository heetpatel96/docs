# RSTAB.TypesforConcreteDesign package

## Submodules

## RSTAB.TypesforConcreteDesign.ConcreteDurability module


### _class_ RSTAB.TypesforConcreteDesign.ConcreteDurability.ConcreteDurability(no=1, name='XC 1', members_no='1', member_sets_no='1', surfaces_no='1', exposure_classes_reinforcement=[True, False, False, False], exposure_classes_reinforcement_types=None, exposure_classes_concrete=[False, False, False], exposure_classes_concrete_types=None, structural_class=[<DurabilityStructuralClassType.STANDARD: 1>, False, False, False, False], stainless_steel_reduction=[False], additional_protection_reduction=[False], allowance_deviation=[<DurabilityAllowanceDeviationType.STANDARD: 1>, False], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(no=1, name='XC 1', members_no='1', member_sets_no='1', surfaces_no='1', exposure_classes_reinforcement=[True, False, False, False], exposure_classes_reinforcement_types=None, exposure_classes_concrete=[False, False, False], exposure_classes_concrete_types=None, structural_class=[<DurabilityStructuralClassType.STANDARD: 1>, False, False, False, False], stainless_steel_reduction=[False], additional_protection_reduction=[False], allowance_deviation=[<DurabilityAllowanceDeviationType.STANDARD: 1>, False], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Concrete Durability Tag


    * **name** (*str*) – User Defined Name


    * **members_no** (*str*) – Assigned Members


    * **member_sets_no** (*str*) – Assigned Member Sets


    * **surfaces_no** (*str*) – Assigned Surfaces


    * **exposure_classes_reinforcement** (*list*) – Exposure Classes Reinforcement Parameters


    * **exposure_classes_reinforcement_types** (*list of enum*) – Exposure Classes Reinforcement Type List of Enumeration


    * **exposure_classes_concrete** (*list*) – Exposure Classes Concrete Parameters


    * **exposure_classes_concrete_types** (*list of enum*) – Exposure Classes Concrete Type List of Enumeration


    * **structural_class** (*list*) – Structural Class Parameters


    * **stainless_steel_reduction** (*list*) – Stainless Steel Reduction Parameters


    * **additional_protection_reduction** (*list*) – Additional Protection Reduction


    * **allowance_deviation** (*list*) – Allowance Deviation Parameters


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## RSTAB.TypesforConcreteDesign.ConcreteEffectiveLength module


### _class_ RSTAB.TypesforConcreteDesign.ConcreteEffectiveLength.ConcreteEffectiveLength(no=1, name='EL 1', members_no='1', member_sets_no='1', flexural_buckling_about_y=[True, <ConcreteEffectiveLengthAxisY.STRUCTURE_TYPE_UNBRACED: 1>], flexural_buckling_about_z=[True, <ConcreteEffectiveLengthsAxisZ.STRUCTURE_TYPE_UNBRACED: 1>], nodal_supports=[[<EffectiveLengthSupportType.SUPPORT_TYPE_FIXED_ALL: 0>, True, 0, <EffectiveLengthEccentricityType.ECCENTRICITY_TYPE_NONE: 2>, 0, 0, 0, 0, <SupportStatus.SUPPORT_STATUS_YES: 2>, <RestraintTypeAboutX.SUPPORT_STATUS_NO: 0>, <RestraintTypeAboutZ.SUPPORT_STATUS_NO: 0>, <RestraintTypeWarping.SUPPORT_STATUS_NO: 0>, '1'], [<EffectiveLengthSupportType.SUPPORT_TYPE_FIXED_ALL: 0>, True, 0, <EffectiveLengthEccentricityType.ECCENTRICITY_TYPE_NONE: 2>, 0, 0, 0, 0, <SupportStatus.SUPPORT_STATUS_YES: 2>, <RestraintTypeAboutX.SUPPORT_STATUS_NO: 0>, <RestraintTypeAboutZ.SUPPORT_STATUS_NO: 0>, <RestraintTypeWarping.SUPPORT_STATUS_NO: 0>, '2']], factors=[[1, 1]], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(no=1, name='EL 1', members_no='1', member_sets_no='1', flexural_buckling_about_y=[True, <ConcreteEffectiveLengthAxisY.STRUCTURE_TYPE_UNBRACED: 1>], flexural_buckling_about_z=[True, <ConcreteEffectiveLengthsAxisZ.STRUCTURE_TYPE_UNBRACED: 1>], nodal_supports=[[<EffectiveLengthSupportType.SUPPORT_TYPE_FIXED_ALL: 0>, True, 0, <EffectiveLengthEccentricityType.ECCENTRICITY_TYPE_NONE: 2>, 0, 0, 0, 0, <SupportStatus.SUPPORT_STATUS_YES: 2>, <RestraintTypeAboutX.SUPPORT_STATUS_NO: 0>, <RestraintTypeAboutZ.SUPPORT_STATUS_NO: 0>, <RestraintTypeWarping.SUPPORT_STATUS_NO: 0>, '1'], [<EffectiveLengthSupportType.SUPPORT_TYPE_FIXED_ALL: 0>, True, 0, <EffectiveLengthEccentricityType.ECCENTRICITY_TYPE_NONE: 2>, 0, 0, 0, 0, <SupportStatus.SUPPORT_STATUS_YES: 2>, <RestraintTypeAboutX.SUPPORT_STATUS_NO: 0>, <RestraintTypeAboutZ.SUPPORT_STATUS_NO: 0>, <RestraintTypeWarping.SUPPORT_STATUS_NO: 0>, '2']], factors=[[1, 1]], comment='', params=None, model=<class 'RSTAB.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Concrete Effective Length Tag


    * **name** (*str*) – User Defined Name


    * **members_no** (*str*) – Assigned Members


    * **member_sets_no** (*str*) – Assigned Member Sets


    * **flexural_buckling_about_y** (*list*) – Flexural Buckling About Y Option


    * **flexural_buckling_about_z** (*list*) – Flexural Buckling About Z Option


    * **nodal_supports** (*list of lists*) – Nodal Support Table
    nodal_supports = [[support_type, support_in_z, support_spring_in_y, eccentricity_type,

    > eccentricity_ez, restraint_spring_about_x,
    > restraint_spring_about_z, restraint_spring_warping, support_in_y_type,
    > restraint_about_x_type, restraint_about_z_type, restraint_warping_type, nodes], …]



    * **factors** (*list of lists*) – Factors Table
    factors = [[flexural_buckling_y, flexural_buckling_z]]


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited


## Module contents
