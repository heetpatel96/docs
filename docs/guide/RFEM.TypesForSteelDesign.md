# Types for Steel Design

Go to *[[source]](https://github.com/Dlubal-Software/RFEM_Python_Client/tree/main/RFEM/TypesForSteelDesign)*

## SteelBoundaryConditions

### SteelBoundaryConditions(no, user_defined_name, members, member_sets, intermediate_nodes, different_properties_supports, different_properties_hinges, nodal_supports, member_hinges, comment, params, model)

* **Parameters**

    
    * **no** (*int*) – Boundary Conditions Tag


    * **user_defined_name** (*str*) – User Defined Boundary Conditions Name


    * **members** (*str*) – Assigned Members


    * **member_sets** (*str*) – Assigned Member Sets


    * **intermediate_nodes** (*bool*) – Enable/Disable Intermediate Nodes Option


    * **different_properties_supports** (*bool*) – Different Properties Option for Supports


    * **different_properties_hinges** (*bool*) – Different Properties Option for Hinges


    * **nodal_supports** (*list of lists*) – Nodal Supports Table Definition

        > nodal_supports[i][0] (int)= Node Sequence No.     
        nodal_supports[i][1] (enum)= Support Type Enumeration   
        nodal_supports[i][2] (bool)= Support in X Direction Option  
        nodal_supports[i][3] (bool)= Support in Y Direction Option  
        nodal_supports[i][4] (bool)= Support in Z Direction Option  
        nodal_supports[i][5] (bool)= Restraint About X Option   
        nodal_supports[i][6] (bool)= Restraint About Y Option   
        nodal_supports[i][7] (bool)= Restraint About Z Option   
        nodal_supports[i][8] (bool)= Restraint Warping Option   
        nodal_supports[i][9] (float)= Rotation Magnitude    
        nodal_supports[i][10] (float)= Rotation About X Magnitude   
        nodal_supports[i][11] (float)= Rotation About Y Magnitude   
        nodal_supports[i][12] (float)= Rotation About Z Magnitude   
        nodal_supports[i][13] (float)= Support Spring X     
        nodal_supports[i][14] (float)= Support Spring Y     
        nodal_supports[i][15] (float)= Support Spring Z     
        nodal_supports[i][16] (float)= Restraint Spring About X Magnitude       
        nodal_supports[i][17] (float)= Restraint Spring About Y Magnitude   
        nodal_supports[i][18] (float)= Restraint Spring About Z Magnitude   
        nodal_supports[i][19] (float)= Restraint Spring Warping Magnitude   
        nodal_supports[i][20] (enum)= Eccentricity Type in Z Enumeration    
        nodal_supports[i][21] (float)= Eccentricity in X Magnitude  
        nodal_supports[i][22] (float)= Eccentricity in Y Magnitude  
        nodal_supports[i][23] (float)= Eccentricity in Z Magnitude  
        nodal_supports[i][24] (str)= Assigned Nodes     


    * **member_hinges** (*list of lists*) – Member Hinges Table Definition

        > member_hinges[i][0] = Node Sequence No.   
        member_hinges[i][1] = Release in X Option   
        member_hinges[i][2] = Release in Y Option   
        member_hinges[i][3] = Release in Z Option   
        member_hinges[i][4] = Release About X Option    
        member_hinges[i][5] = Release About Y Option    
        member_hinges[i][6] = Release About Z Option    
        member_hinges[i][7] = Release Warping Option    
        member_hinges[i][8] = Release Spring in X Magnitude     
        member_hinges[i][9] = Release Spring in Y Magnitude     
        member_hinges[i][10] = Release Spring in Z Magnitude    
        member_hinges[i][11] = Release Spring About X Magnitude     
        member_hinges[i][12] = Release Spring About Y Magnitude     
        member_hinges[i][13] = Release Spring About Z Magnitude     
        member_hinges[i][14] = Release Spring Warping Magnitude     
        member_hinges[i][15] = Assigned Nodes   


    * **comment** (*str*, *optional*) – Comment


    * **params** (*dict*, *optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RFEM Class, optional*) – Model to be edited



## SteelEffectiveLengths


### SteelEffectiveLengths(no, members, member_sets, flexural_buckling_about_y, flexural_buckling_about_z, torsional_buckling, lateral_torsional_buckling, principal_section_axes, geometric_section_axes, user_defined_name, nodal_supports, factors, intermediate_nodes, different_properties, factors_definition_absolute, import_from_stability_analysis_enabled, determination_of_mcr, comment, params, model)

* **Parameters**

    
    * **no** (*int*) – Steel Effective Length Tag


    * **members** (*str*) – Assigned Members


    * **member_sets** (*str*) – Assigned Member Sets


    * **flexural_buckling_about_y** (*bool*) – Flexural Buckling About Y Option


    * **flexural_buckling_about_z** (*bool*) – Flexural Buckling About Z Option


    * **torsional_buckling** (*bool*) – Torsional Buckling Option


    * **lateral_torsional_buckling** (*bool*) – Lateral Torsional Buckling Option


    * **principal_section_axes** (*bool*) – Principal Section Axes Option


    * **geometric_section_axes** (*bool*) – Geometric Section Axes Option


    * **user_defined_name** (*str*) – User Defined Effective Length Name


    * **nodal_supports** (*list of lists*) – Nodal Supports Table Definition

        > nodal_supports[i][0] (enum): Support Type Enumeration Type    
        nodal_supports[i][1] (bool): Support in Z Option    
        nodal_supports[i][2] (float): Support Spring in Y Coefficient   
        nodal_supports[i][3] (enum): Eccentricity Type Enumeration Type     
        nodal_supports[i][4] (float): Eccentricity in Z Direction   
        nodal_supports[i][5] (float): Restraint Spring About X Coefficient  
        nodal_supports[i][6] (float): Restraint Spring About Z Coefficient  
        nodal_supports[i][7] (float): Restraint Spring Warping Coefficient  
        nodal_supports[i][8] (enum): Support Type in Y Enumeration Type     
        nodal_supports[i][9] (enum): Restraint Type in X Enumeration Type   
        nodal_supports[i][10] (enum): Restraint Type in Z Enumeration Type  
        nodal_supports[i][11] (enum): Restraint Type Warping Enumeration Type   
        nodal_supports[i][12] (str): Assigned Nodes     


    * **factors** (*list of lists*) – Effective Length Factors

        > factors[i][0] (float): Flexural Buckling in U Coefficient     
        factors[i][1] (float): Flexural Buckling in V Coefficient   
        factors[i][2] (float): Flexural Buckling in Y Coefficient   
        factors[i][3] (float): Flexural Buckling in Z Coefficient   
        factors[i][4] (float): Torsional Buckling Coefficient   
        factors[i][5] (float): Lateral Torsional Buckling Coefficient       
        factors[i][6] (float): Lateral Torsional Buckling Top Coefficient   
        factors[i][7] (float): Lateral Torsional Buckling Bottom Coefficient    
        factors[i][8] (float): Twist Restraint Coefficient  
        factors[i][9] (float): Lateral Torsional Restraint Coefficient  
        factors[i][10] (float): Critical Moment     


    * **intermediate_nodes** (*bool*) – Intermediate Nodes Option


    * **different_properties** (*bool*) – Different Properties Option


    * **factors_definition_absolute** (*bool*) – Absolute Factors Definition Option


    * **import_from_stability_analysis_enabled** (*bool*) – Import From Stability Analysis Option


    * **determination_of_mcr** (*enum*) – Steel Effective Lengths Determination Mcr Europe Enumeration Item


    * **comment** (*str*, *optional*) – Comment


    * **params** (*dict*, *optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RFEM Class, optional*) – Model to be edited



## SteelMemberLocalSectionReduction

### SteelMemberLocalSectionReduction(no, members, member_sets, components, user_defined_name, comment, params, model)

* **Parameters**

    
    * **no** (*int*) – Member Local Section Reduction Tag


    * **members** (*str*) – Assigned Members


    * **member_sets** (*str*) – Assigned Member Sets


    * **components** (*list of lists*) – Components Table Definition

        > components[i][0] (enum): Steel Member Local Section Reduction Type Enumeration    

        > components[i][1] (float): Position Value  

        > components[i][2] (bool): Enable/Disable Multiple Option 

        > components[i][3] (enum): Fastener Definition Type Enumeration   
                >> * for components[i][3] == FastenerDefinitionType.DEFINITION_TYPE_ABSOLUTE:     
                components[i][4] (float): Reduction Area        
                >> * for components[i][3] == FastenerDefinitionType.DEFINITION_TYPE_RELATIVE:      
                components[i][4] (float): Reduction Area Factor (value must be between 0.0 and 1.0)

        > if components[i][2] == True   
        components[i][5] (int): Multiple Number         
        components[i][6] (enum): Multiple Offset Definition Type Enumeration    
                >> * for MultipleOffsetDefinitionType.OFFSET_DEFINITION_TYPE_ABSOLUTE:          
                components[i][7] (float): Multiple Offset Value         
                >> * for MultipleOffsetDefinitionType.OFFSET_DEFINITION_TYPE_RELATIVE:              
                components[i][7] (float): Multiple Offset Value (value must be between 0.0 and 1.0)  


    * **user_defined_name** (*str*) – User Defined Local Section Reduction Name


    * **comment** (*str*, *optional*) – Comment


    * **params** (*dict*, *optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RFEM Class, optional*) – Model to be edited



## SteelMemberRotationalRestraint


### SteelMemberRotationalRestraint(no, user_defined_name, definition_type, members, member_sets, categories, parameters, comment, params, model)

* **Parameters**

    
    * **no** (*int*) – Steel Member Rotational Restraint Tag


    * **user_defined_name** (*list*) – User Defined Member Rotational Restraint Name

        > * for user_defined_name[0] == False:  
                pass
        
        > * for user_defined_name == True:  
                user_defined_name[1] = Defined Name
    

    * **definition_type** (*enum*) – Steel Member Rotational Restraint Type Enumeration


    * **members** (*str*) – Assigned Members


    * **member_sets** (*str*) – Assigned Member Sets


    * **categories** (*list*) – Categories List


        > * for definition_type = SteelMemberRotationalRestraintType.TYPE_CONTINUOUS:   
                categories[0] = Sheeting Material Name      
                categories[1] = Sheeting Name   
                categories[2] = Position of Sheeting    
                categories[3] = Continuous Beam Effect  
                categories[4] = Section Deformation Option  
        
        > * for definition_type = SteelMemberRotationalRestraintType.TYPE_DISCRETE:     
                categories[0] = Section Material Name   
                categories[1] = Section Name    
                categories[2] = Rotational Stifness     
                categories[3] = Continuous Beam Effect  
                categories[4] = Section Deformation Option  
        
        > * for definition_type = SteelMemberRotationalRestraintType.TYPE_MANUALLY:     
                categories = None


    * **parameters** (*list*) – Parameters List


        > * for definition_type = SteelMemberRotationalRestraintType.TYPE_CONTINUOUS:   
                parameters[0] = Modulus of Elasticity   
                parameters[1] = Sheeting Thickness  
                parameters[2] = Sheeting Moment of Inertia  
                parameters[3] = Sheeting Distance of Ribs   
                parameters[4] = Width of Sheeting Flanges   
                parameters[5] = Spring Stiffness    
                parameters[6] = Beam Spacing    

        > * for definition_type = SteelMemberRotationalRestraintType.TYPE_DISCRETE:     
                parameters[0] = Modulus of Elasticity       
                parameters[1] = Section Moment of Inertia   
                parameters[2] = Purlin Spacing  
                parameters[3] = Beam Spacing    
        
        > * for definition_type = SteelMemberRotationalRestraintType.TYPE_MANUALLY:     
                parameters[0] = Rotational Spring Stifness      


    * **comment** (*str*, *optional*) – Comment


    * **params** (*dict*, *optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RFEM Class, optional*) – Model to be edited



## SteelMemberShearPanel


### SteelMemberShearPanel(no, user_defined_name, definition_type, members, member_sets, categories, parameters, comment, params)

* **Parameters**

    
    * **no** (*int*) – Steel Member Rotational Restraint Tag


    * **user_defined_name** (*list*) – User Defined Member Shear Panel Name

        > * for user_defined_name[0] == False:  
                pass
        
        > * for user_defined_name == True:  
                user_defined_name[1] = Defined Name
    

    * **definition_type** (*enum*) – Steel Member Shear Panel Definition Type Enumeration


    * **members** (*str*) – Assigned Members


    * **member_sets** (*str*) – Assigned Member Sets


    * **categories** (*list*) – Categories List


        > * for definition_type == SteelMemberShearPanelDefinitionType.DEFINITION_TYPE_TRAPEZOIDAL_SHEETING:    
                categories[0] = Section Position Enumeration Type   
                categories[1] = Sheeting Name   
                categories[2] = Fastening Arrangment Enumeration Type   
                
        > * for definition_type == SteelMemberShearPanelDefinitionType.DEFINITION_TYPE_BRACING:     
                categories[0] = Section Position Enumeration Type   
                categories[1] = Diagonal Section Name   
                categories[2] = Post Section Name       
                
        > * for definition_type == SteelMemberShearPanelDefinitionType.DEFINITION_TYPE_TRAPEZOIDAL_SHEETING_AND_BRACING:    
                categories[0] = Section Position Enumeration Type   
                categories[1] = Sheeting Name   
                categories[2] = Digonal Section Name    
                categories[3] = Post Section Name   
                categories[4] = Fastening Arrangment Enumeration Type   
                
        > * for definition_type == SteelMemberShearPanelDefinitionType.DEFINITION_TYPE_DEFINE_S_PROV:   
                categories[0] = Section Position Enumeration Type   


    * **parameters** (*list*) – Parameters List


        > * for definition_type == SteelMemberShearPanelDefinitionType.DEFINITION_TYPE_TRAPEZOIDAL_SHEETING:    
                parameters[0] = Panel Length    
                parameters[1] = Beam Spacing    
                parameters[2] = K1 Coefficient  
                parameters[3] = K2 Coefficient  
            >> * if categories[0] == "POSITION_DEFINE":  
                    parameters[4] = Position on Section Value   
                
        > * for definition_type == SteelMemberShearPanelDefinitionType.DEFINITION_TYPE_BRACING:     
                parameters[0] = Panel Length    
                parameters[1] = Beam Spacing    
                parameters[2] = Post Spacing    
                parameters[3] = Number of Bracings  
                parameters[4] = Diagonals Section Area  
                parameters[5] = Post Section Area   
            >> * if categories[0] == "POSITION_DEFINE":  
                    parameters[6] = Position on Section Value   
                
        > * for definition_type == SteelMemberShearPanelDefinitionType.DEFINITION_TYPE_TRAPEZOIDAL_SHEETING_AND_BRACING:    
                parameters[0] = Panel Length    
                parameters[1] = Beam Spacing    
                parameters[2] = K1 Coefficient  
                parameters[3] = K2 Coefficient      
                parameters[4] = Post Spacing    
                parameters[5] = Number of Bracing   
                parameters[6] = Diagonals Section Area  
                parameters[7] = Post Section Area   
            >> * if categories[0] == "POSITION_DEFINE":  
                    parameters[8] = Position on Section Value   
                
        > * for definition_type == SteelMemberShearPanelDefinitionType.DEFINITION_TYPE_DEFINE_S_PROV:   
                parameters[0] = Stifness    
            >> * if categories[0] == "POSITION_DEFINE":  
                    parameters[1] = Position on Section Value   


    * **comment** (*str*, *optional*) – Comment


    * **params** (*dict*, *optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary