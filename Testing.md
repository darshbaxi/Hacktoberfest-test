# MindsDB Editor Testing Report

This document contains the results of testing the MindsDB Editor commands based on the provided resources.

## Test Results

## Create Project

**Command**:

  import mindsdb_sdk
   <br> 
  server = mindsdb_sdk.connect('localhost')   
  server = mindsdb_sdk.connect(login='login-id', password='')
   <br> 
  project = server.create_project('testing-file')
   <br> 
   <br>

   
**Expected Output:**

  ![create_project](https://github.com/darshbaxi/Hacktoberfest-test/assets/119887723/cc04e5cd-8272-4903-9d47-0104cbc40e64)


**Status**: [Pass]

 
## Drop Project

**Command**:

  import mindsdb_sdk
   <br> 
  server = mindsdb_sdk.connect('localhost')
   <br> 
  server = mindsdb_sdk.connect(login='login-id', password='')
   <br> 
  print("Before Drop_project command")
   <br> 
  print(server.list_projects())
   <br> 
  server.drop_project('testing-file')
   <br> 
  print("After Drop_project command")
   <br> 
  print(server.list_projects()) 
   <br>
   <br>



**Expected Output:**

  ![Drop_project](https://github.com/darshbaxi/Hacktoberfest-test/assets/119887723/3bf39f47-645d-4cdf-b0bf-82410f781baf)

**Status**: [Pass]


## List Projects

**Command**: 

  import mindsdb_sdk
  <br>
  server = mindsdb_sdk.connect('localhost')
  <br>
  server = mindsdb_sdk.connect(login='login-id', password='')
  <br>
  print(server.list_projects())
  <br>
  <br>
  

**Expected Output:**

  ![list_project](https://github.com/darshbaxi/Hacktoberfest-test/assets/119887723/02b67f88-b5ad-41fc-a981-6343620f4296)

**Status**: [Pass]


## Query Projects

**Command**: 

  import mindsdb_sdk
  <br>
  server = mindsdb_sdk.connect('localhost')
  <br>
  server = mindsdb_sdk.connect(login='login-id', password='')
  <br>
  project=server.get_project('test1')
  <br>
  query=project.query('select sentiment from test1.amazonreview where review="For the sake of my 5 and 8-year-old grandchildren entertainment, we decided to get                                                                 the Kindle Fire HD 8. They have a blast playing Amazon games that weve loaded onto the device.";')
  <br>
  print(query.fetch())
  <br>
  <br>


**Expected Output:**

  ![Query fetch](https://github.com/darshbaxi/Hacktoberfest-test/assets/119887723/01a6d033-4fd9-43d8-a65f-464cc0ae2574)

**Status**: [Pass]



