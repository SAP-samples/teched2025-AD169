# Exercise 1 - Test the Action Project

There is an action project which will be used in this hands-on project for Joule skill creation. The action project is already created. In this section, let us test the action project.
<br>1: In the left panel of the lobby area, expand ‘Connectors’ and click on ‘Actions’
<br>2: Search for the action project, ‘WarehouseWorkloadDetermination’. Click on it to open

<br> <img width="940" height="374" alt="image" src="https://github.com/user-attachments/assets/ab1723c9-cc76-4cd0-8927-30a36ce27b3c" />


2.	Insert this line of code.
```abap
response->set_text( |Hello World! | ). 
```



## Exercise 1.2 Sub Exercise 2 Description

After completing these steps you will have...

1.	Enter this code.
```abap
DATA(lt_params) = request->get_form_fields(  ).
READ TABLE lt_params REFERENCE INTO DATA(lr_params) WITH KEY name = 'cmd'.
  IF sy-subrc <> 0.
    response->set_status( i_code = 400
                     i_reason = 'Bad request').
    RETURN.
  ENDIF.

```

2.	Click here.
<br>![](/exercises/ex1/images/01_02_0010.png)


## Summary

You've now ...

Continue to - [Exercise 2 - Exercise 2 Description](../ex2/README.md)

