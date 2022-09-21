# RSTAB.TypesForNodes package

## Submodules

## RSTAB.TypesForNodes.nodalSupport module


### _class_ RSTAB.TypesForNodes.nodalSupport.NodalSupport(no=1, nodes_no='1 2', support=NodalSupportType.HINGED, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Bases: `object`


#### \__init__(no=1, nodes_no='1 2', support=NodalSupportType.HINGED, comment='', params=None, model=<class 'RSTAB.initModel.Model'>)
Nodal Support


* **Parameters**

    
    * **no** (*int*) – Nodal Support Tag


    * **nodes_no** (*str*) – Assigned to Nodes


    * **support** (*enum** or **list*) – Support Definition List


    * **comment** (*str**, **optional*) – Comment


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSTAB Class**, **optional*) – Model to be edited



* **Raises**

    **ValueError** – ‘Support parameter can be enum or list with 6 items.’



### RSTAB.TypesForNodes.nodalSupport.setNodalSupportConditions(clientObject, C_u_X, C_u_Y, C_u_Z, C_phi_X, C_phi_Y, C_phi_Z)
Sets Nodal Support Conditions


* **Parameters**

    
    * **clientObject** – Client Model Object | Nodal Support


    * **C_u_X** (*float*) – Translational Support Conditions in Respected Direction


    * **Y** (*float*) – Translational Support Conditions in Respected Direction


    * **Z** (*float*) – Translational Support Conditions in Respected Direction


    * **C_phi_X** (*float*) – Rotational Support Conditions about Respected Axis


    * **Y** – Rotational Support Conditions about Respected Axis


    * **Z** – Rotational Support Conditions about Respected Axis



* **Returns**

    Initialized Client Model Object | Nodal Support



* **Return type**

    clientObject


## Module contents
