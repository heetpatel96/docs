# RSTAB.SpecialObjects package

## Submodules

## RSTAB.SpecialObjects.nodalRelease module


### _class_ RSTAB.SpecialObjects.nodalRelease.NodalRelease(comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
## RSTAB.SpecialObjects.structureModification module


### _class_ RSTAB.SpecialObjects.structureModification.StructureModification(no=1, modify_stiffnesses={'deactivate_members_enabled': False, 'modify_stiffness_member_reinforcement': False, 'modify_stiffness_surface_reinforcement': False, 'modify_stiffness_timber_members_due_moisture_class': False, 'modify_stiffnesses_gamma_m': False, 'modify_stiffnesses_line_hinges': False, 'modify_stiffnesses_line_supports': False, 'modify_stiffnesses_materials': False, 'modify_stiffnesses_member_hinges': False, 'modify_stiffnesses_member_supports': False, 'modify_stiffnesses_members': False, 'modify_stiffnesses_nodal_supports': False, 'modify_stiffnesses_sections': False, 'modify_stiffnesses_surface_supports': False, 'modify_stiffnesses_surfaces': False, 'nonlinearities_disabled_line_hinges': False, 'nonlinearities_disabled_line_supports': False, 'nonlinearities_disabled_material_nonlinearity_models': False, 'nonlinearities_disabled_material_temperature_nonlinearities': False, 'nonlinearities_disabled_member_hinges': False, 'nonlinearities_disabled_member_nonlinearities': False, 'nonlinearities_disabled_member_supports': False, 'nonlinearities_disabled_member_types': False, 'nonlinearities_disabled_nodal_supports': False, 'nonlinearities_disabled_solid_types_contact_or_surfaces_contact': False, 'nonlinearities_disabled_surface_supports': False}, modify_stiffnesses_materials_list=None, modify_stiffnesses_sections_list=None, modify_stiffnesses_members_list=None, modify_stiffnesses_surfaces_list=None, modify_stiffnesses_member_hinges_list=None, modify_stiffnesses_line_hinges_list=None, modify_stiffnesses_nodal_supports_list=None, modify_stiffnesses_line_supports_list=None, modify_stiffnesses_member_supports_list=None, modify_stiffnesses_surface_supports_list=None, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(no=1, modify_stiffnesses={'deactivate_members_enabled': False, 'modify_stiffness_member_reinforcement': False, 'modify_stiffness_surface_reinforcement': False, 'modify_stiffness_timber_members_due_moisture_class': False, 'modify_stiffnesses_gamma_m': False, 'modify_stiffnesses_line_hinges': False, 'modify_stiffnesses_line_supports': False, 'modify_stiffnesses_materials': False, 'modify_stiffnesses_member_hinges': False, 'modify_stiffnesses_member_supports': False, 'modify_stiffnesses_members': False, 'modify_stiffnesses_nodal_supports': False, 'modify_stiffnesses_sections': False, 'modify_stiffnesses_surface_supports': False, 'modify_stiffnesses_surfaces': False, 'nonlinearities_disabled_line_hinges': False, 'nonlinearities_disabled_line_supports': False, 'nonlinearities_disabled_material_nonlinearity_models': False, 'nonlinearities_disabled_material_temperature_nonlinearities': False, 'nonlinearities_disabled_member_hinges': False, 'nonlinearities_disabled_member_nonlinearities': False, 'nonlinearities_disabled_member_supports': False, 'nonlinearities_disabled_member_types': False, 'nonlinearities_disabled_nodal_supports': False, 'nonlinearities_disabled_solid_types_contact_or_surfaces_contact': False, 'nonlinearities_disabled_surface_supports': False}, modify_stiffnesses_materials_list=None, modify_stiffnesses_sections_list=None, modify_stiffnesses_members_list=None, modify_stiffnesses_surfaces_list=None, modify_stiffnesses_member_hinges_list=None, modify_stiffnesses_line_hinges_list=None, modify_stiffnesses_nodal_supports_list=None, modify_stiffnesses_line_supports_list=None, modify_stiffnesses_member_supports_list=None, modify_stiffnesses_surface_supports_list=None, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Structural Modification
Modify only objects allready existing and used/assigned in the model.


* **Parameters**

    
    * **no** (*int**, **optional*) – Structure Modification Tag


    * **modify_stiffnesses** (*dict**, **optional*) – Modify Stiffnesses


    * **modify_stiffnesses_materials_list** (*list**, **optional*) – Modify Stiffnesses Materials List


    * **modify_stiffnesses_sections_list** (*list**, **optional*) – Modify Stiffnesses Sections List


    * **modify_stiffnesses_members_list** (*list**, **optional*) – Modify Stiffnesses Members List


    * **modify_stiffnesses_surfaces_list** (*list**, **optional*) – Modify Stiffnesses Surfaces List


    * **modify_stiffnesses_member_hinges_list** (*list**, **optional*) – Modify Stiffnesses Member Hinges List


    * **modify_stiffnesses_line_hinges_list** (*list**, **optional*) – Modify Stiffnesses Line Hinges List


    * **modify_stiffnesses_nodal_supports_list** (*list**, **optional*) – Modify Stiffnesses Nodal Supports List


    * **modify_stiffnesses_line_supports_list** (*list**, **optional*) – Modify Stiffnesses Line Support List


    * **modify_stiffnesses_member_supports_list** (*list**, **optional*) – Modify Stiffnesses Member Suppoorts List


    * **modify_stiffnesses_surface_supports_list** (*list**, **optional*) – Modify Stiffnesses Surface Supports List


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



#### line_hinge_item(_ = {'C_phi_x': 0, 'C_phi_y': 0, 'C_phi_z': 0, 'C_u_x': 1, 'C_u_y': 0, 'C_u_z': 0, 'no': 1_ )

#### line_support_item(_ = {'C_phi_X': 0, 'C_phi_Y': 0, 'C_phi_Z': 0, 'C_u_X': 1, 'C_u_Y': 0, 'C_u_Z': 0_ )

#### material_item(_ = {'E_and_G': 1.5, 'comment': 'comment', 'material_name': 1, 'modification_type': 'DIVISION_FACTOR', 'no': 1_ )

#### member_hinge_item(_ = {'C_phi_x': 0, 'C_phi_y': 0, 'C_phi_z': 0, 'C_u_x': 1, 'C_u_y': 0, 'C_u_z': 0, 'member_side': 'Start', 'no': 1_ )

#### member_item(_ = {'comment': '', 'member_modification': 1, 'members': '11', 'no': 2_ )

#### member_support_item(_ = {'C_phi_x': 0, 'C_s_x': 0, 'C_s_y': 0, 'C_s_z': 0, 'C_u_x': 1, 'C_u_y': 0, 'C_u_z': 0_ )

#### modify_stiffness(_ = {'deactivate_members_enabled': False, 'modify_stiffness_member_reinforcement': False, 'modify_stiffness_surface_reinforcement': False, 'modify_stiffness_timber_members_due_moisture_class': False, 'modify_stiffnesses_gamma_m': False, 'modify_stiffnesses_line_hinges': False, 'modify_stiffnesses_line_supports': False, 'modify_stiffnesses_materials': False, 'modify_stiffnesses_member_hinges': False, 'modify_stiffnesses_member_supports': False, 'modify_stiffnesses_members': False, 'modify_stiffnesses_nodal_supports': False, 'modify_stiffnesses_sections': False, 'modify_stiffnesses_surface_supports': False, 'modify_stiffnesses_surfaces': False, 'nonlinearities_disabled_line_hinges': False, 'nonlinearities_disabled_line_supports': False, 'nonlinearities_disabled_material_nonlinearity_models': False, 'nonlinearities_disabled_material_temperature_nonlinearities': False, 'nonlinearities_disabled_member_hinges': False, 'nonlinearities_disabled_member_nonlinearities': False, 'nonlinearities_disabled_member_supports': False, 'nonlinearities_disabled_member_types': False, 'nonlinearities_disabled_nodal_supports': False, 'nonlinearities_disabled_solid_types_contact_or_surfaces_contact': False, 'nonlinearities_disabled_surface_supports': False_ )

#### nodal_support_item(_ = {'C_phi_X': 0, 'C_phi_Y': 0, 'C_phi_Z': 0, 'C_u_X': 1, 'C_u_Y': 0, 'C_u_Z': 0_ )

#### section_item(_ = {'A': 1.0, 'A_y': 1.0, 'A_z': 1.0, 'I_y': 1.0, 'I_z': 1.0, 'J': 1.0, 'no': 1, 'section_name': 'IPN 300'_ )

#### surface_item(_ = {'comment': '', 'no': 1, 'surface_modification': 1, 'surfaces': '2'_ )

#### surface_support_item(_ = {'C_u_X': 1, 'C_u_Y': 0, 'C_u_Z': 0, 'C_v_xz': 0, 'C_v_yz': 0_ )
## Module contents
