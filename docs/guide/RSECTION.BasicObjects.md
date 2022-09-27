# RSECTION.BasicObjects package

## Submodules

## RSECTION.BasicObjects.element module


### _class_ RSECTION.BasicObjects.element.Element(no=1, points_no='1 2', thickness=0.0, comment='', params=None, model=<class 'RSECTION.initModel.Model'>)
Bases: `object`


#### _static_ Arc(no=1, points_no=[1, 2], control_point=None, alpha_adjustment_target=ElementArcAlphaAdjustmentTarget.ALPHA_ADJUSTMENT_TARGET_BEGINNING_OF_ARC, thickness=0.0, effective_thickness=[False, None], comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Element Tag


    * **points_no** (*list*) – Points Number


    * **control_point** (*list*) – Control Point coordinate for Arc in [Y, Z]


    * **alpha_adjustment_target** (*enum*) – Element Arc Alpha Adjustment Target Enumeration


    * **thickness** (*float*) – Element Thickness


    * **effective_thickness** (*list*) – Effective Thickness List


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### _static_ Circle(no=1, center_of_cirle=[0.0, 0.0], circle_radius=0.1, thickness=0.0, effective_thickness=[False, None], comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Element Tag


    * **center_of_cirle** (*list*) – Coordinate of Circle Center


    * **circle_radius** (*float*) – Circle Radius


    * **thickness** (*float*) – Element Thickness


    * **effective_thickness** (*list*) – Effective Thickness List


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### _static_ DeleteElement(elements_no='1 2', model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **elements_no** (*str*) – Elements Number


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### _static_ Ellipse(no=1, points_no=[1, 2], control_point=None, thickness=0.0, effective_thickness=[False, None], comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Element Tag


    * **points_no** (*list*) – Points Number


    * **control_point** (*list*) – Control Point coordinate for Ellipse in [Y, Z]


    * **thickness** (*float*) – Element Thickness


    * **effective_thickness** (*list*) – Effective Thickness List


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### _static_ NURBS(no=1, control_points=None, components=None, weights=None, order=None, thickness=0.0, effective_thickness=[False, None], comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Element Tag


    * **control_points** (*str*) – String of Start Point and End Point (example: ‘1 2’)


    * **components** (*list of lists*) – Control Points List
    component = [[start_point_x, start_point_y],

    > [control_point_x, control_point_y],
    > ….,
    > [end_point_x, end_point]]



    * **weights** (*list*) – Control Points Weights


    * **order** (*int*) – Nurbs Order


    * **thickness** (*float*) – Element Thickness


    * **effective_thickness** (*list*) – Effective Thickness List


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### _static_ Parabola(no=1, points_no=[1, 2], control_point=None, alpha=0.0, thickness=0.0, effective_thickness=[False, None], comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Element Tag


    * **points_no** (*list*) – Points Number


    * **control_point** (*list*) – Control Point coordinate for Parabola in [Y, Z]


    * **alpha** (*float*) – Alpha Angle (in Radians)


    * **thickness** (*float*) – Element Thickness


    * **effective_thickness** (*list*) – Effective Thickness List


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### _static_ SingleLine(no=1, points_no='1 2', thickness=0.0, effective_thickness=[False, None], comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Element Tag


    * **points_no** (*str*) – Points Number


    * **thickness** (*float*) – Element Thickness


    * **effective_thickness** (*list*) – Effective Thickness List


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### \__init__(no=1, points_no='1 2', thickness=0.0, comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Element Tag


    * **points_no** (*str*) – Points Number


    * **thickness** (*float*) – Element Thickness


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited


## RSECTION.BasicObjects.line module


### _class_ RSECTION.BasicObjects.line.Line(no=1, points_no='1 2', comment='', params=None, model=<class 'RSECTION.initModel.Model'>)
Bases: `object`


#### _static_ Arc(no=1, points_no=[1, 2], control_point=None, alpha_adjustment_target=LineArcAlphaAdjustmentTarget.ALPHA_ADJUSTMENT_TARGET_BEGINNING_OF_ARC, comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Line Tag


    * **points_no** (*list*) – Points Number


    * **control_point** (*list*) – Control Point coordinate for Arc in [Y, Z]


    * **alpha_adjustment_target** (*enum*) – Line Arc Alpha Adjustment Target Enumeration


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### _static_ Circle(no=1, center_of_cirle=[0.0, 0.0], circle_radius=0.1, comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Line Tag


    * **center_of_cirle** (*list*) – Coordinate of Circle Center


    * **circle_radius** (*float*) – Circle Radius


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### _static_ DeleteLine(lines_no='1 2', model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **lines_no** (*str*) – Line Number


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### _static_ Ellipse(no=1, points_no=[1, 2], control_point=None, comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Line Tag


    * **points_no** (*list*) – Points Number


    * **control_point** (*list*) – Control Point coordinate for Ellipse in [Y, Z]


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### _static_ NURBS(no=1, control_points=None, components=None, weights=None, order=None, comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Line Tag


    * **control_points** (*str*) – String of Start Point and End Point (example: ‘1 2’)


    * **components** (*list of lists*) – Control Points List
    component = [[start_point_x, start_point_y],

    > [control_point_x, control_point_y],
    > ….,
    > [end_point_x, end_point]]



    * **weights** (*list*) – Control Points Weights


    * **order** (*int*) – Nurbs Order


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### _static_ Parabola(no=1, points_no=[1, 2], control_point=None, alpha=0.0, comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Line Tag


    * **points_no** (*list*) – Points Number


    * **control_point** (*list*) – Control Point coordinate for Parabola in [Y, Z]


    * **alpha** (*float*) – Alpha Angle (in Radians)


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### _static_ Polyline(no=1, points_no='1 2', comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Line Tag


    * **points_no** (*str*) – Points Number


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### \__init__(no=1, points_no='1 2', comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Line Tag


    * **points_no** (*str*) – Points Number


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited


## RSECTION.BasicObjects.material module


### _class_ RSECTION.BasicObjects.material.Material(no=1, name='Grade S275', comment='', params=None, model=<class 'RSECTION.initModel.Model'>)
Bases: `object`


#### _static_ DeleteMaterial(materials_no='1 2', model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **materials_no** (*str*) – Materials Number


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### \__init__(no=1, name='Grade S275', comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Material Tag


    * **name** (*str*) – Material Name


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited


## RSECTION.BasicObjects.opening module


### _class_ RSECTION.BasicObjects.opening.Opening(no=1, boundary_lines='1 2 3 4', part_no=1, comment='', params=None, model=<class 'RSECTION.initModel.Model'>)
Bases: `object`


#### _static_ DeleteOpening(openings_no='1 2', model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **openings_no** (*str*) – Openings Number


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### \__init__(no=1, boundary_lines='1 2 3 4', part_no=1, comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Opening Tag


    * **boundary_lines** (*str*) – Boundary Lines Number


    * **part_no** (*int*) – Part Number


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited


## RSECTION.BasicObjects.part module


### _class_ RSECTION.BasicObjects.part.Part(no=1, boundary_lines=None, material_no=1, integrated_objects=True, integrated_objects_auto=True, integrated_openings=None, comment='', params=None, model=<class 'RSECTION.initModel.Model'>)
Bases: `object`


#### _static_ DeletePart(parts_no='1 2', model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **parts_no** (*str*) – Parts Number


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### \__init__(no=1, boundary_lines=None, material_no=1, integrated_objects=True, integrated_objects_auto=True, integrated_openings=None, comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Part Tag


    * **boundary_lines** (*str*) – Boundary Lines Number


    * **material_no** (*int*) – Material Number


    * **integrated_objects** (*bool*) – Enable/Disable Integrated Objects Option


    * **integrated_objects_auto** (*bool*) – Enable/Disable Integrated Objects Auto Option


    * **integrated_openings** (*str*) – Inegrated Openings Line Number


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited


## RSECTION.BasicObjects.point module


### _class_ RSECTION.BasicObjects.point.Point(no=1, coordinate_Y=0.0, coordinate_Z=0.0, comment='', params=None, model=<class 'RSECTION.initModel.Model'>)
Bases: `object`


#### _static_ BetweenTwoLocations(no=1, start_point_y=0.0, start_point_z=0.0, end_point_y=1.0, end_point_z=1.0, point_reference=PointReferenceType.REFERENCE_TYPE_L, parameters=[True, 0.5], offset=0.0, comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Point Tag


    * **start_point_y** (*float*) – Start Point Coordinate Y


    * **start_point_z** (*float*) – Start Point Coordinate Z


    * **end_point_y** (*float*) – End Point Coordinate Y


    * **end_point_z** (*float*) – End Point Coordinate Y


    * **point_reference** (*enum*) – Point Reference Type Enumeration


    * **parameters** (*list*) – Point Reference Parameter List
    for relative reference:

    > parameters = [True, distance_from_start_relative] ex: [True, 0.5]

    for absolute reference:

        parameters = [False, distance_from_start_absolute]



    * **offset** (*float*) – Offset Value


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### _static_ BetweenTwoPoints(no=1, start_point_no=1, end_point_no=2, point_reference=PointReferenceType.REFERENCE_TYPE_L, parameters=[True, 0.5], offset=0.0, comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Point Tag


    * **start_point_no** (*int*) – Start Point Number


    * **end_point_no** (*int*) – End Point Number


    * **point_reference** (*enum*) – Point Reference Type Enumeration


    * **parameters** (*list*) – Point Reference Parameter List
    for relative reference:

    > parameters = [True, distance_from_start_relative] ex: [True, 0.5]

    for absolute reference:

        parameters = [False, distance_from_start_absolute]



    * **offset** (*float*) – Offset Value


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### _static_ DeletePoint(points_no='1 2', model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **points_no** (*str*) – Points Number


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### _static_ OnLine(no=1, line_no=1, point_reference=PointReferenceType.REFERENCE_TYPE_L, parameters=[True, 0.5], comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Point Tag


    * **line_no** (*int*) – Reference Line Number


    * **point_reference** (*enum*) – Point Reference Type Enumeration


    * **parameters** (*list*) – Point Reference Parameter List
    for relative reference:

    > parameters = [True, distance_from_start_relative] ex: [True, 0.5]

    for absolute reference:

        parameters = [False, distance_from_start_absolute]



    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### _static_ Standard(no=1, reference_point=None, coordinate_system=None, comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Point Tag


    * **reference_point** (*int*) – Reference Point Number


    * **coordinate_system** (*list*) – Coordinate System List
    coordinate_system = [coordinate_Y, coordinate_Z]


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### \__init__(no=1, coordinate_Y=0.0, coordinate_Z=0.0, comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Point Tag


    * **coordinate_Y** (*float*) – Y-Coordinate


    * **coordinate_Z** (*float*) – Z-Coordinate


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited


## RSECTION.BasicObjects.section module


### _class_ RSECTION.BasicObjects.section.Section(no=1, name='IPE 80', material_no=1, comment='', params=None, model=<class 'RSECTION.initModel.Model'>)
Bases: `object`


#### _static_ DeleteSection(sections_no='1 2', model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **sections_no** (*str*) – Sections Number


    * **model** (*RSECTION Class**, **optional*) – Model to be edited



#### \__init__(no=1, name='IPE 80', material_no=1, comment='', params=None, model=<class 'RSECTION.initModel.Model'>)

* **Parameters**

    
    * **no** (*int*) – Section Tag


    * **name** (*str*) – Section Name


    * **material_no** (*int*) – Material Number


    * **comment** (*str**, **optional*) – Comments


    * **params** (*dict**, **optional*) – Any WS Parameter relevant to the object and its value in form of a dictionary


    * **model** (*RSECTION Class**, **optional*) – Model to be edited


## Module contents
