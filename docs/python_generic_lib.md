# Getting started

TODO: Add a description

## How to Build


You must have Python ```2 >=2.7.9``` or Python ```3 >=3.4``` installed on your system to install and run this SDK. This SDK package depends on other Python packages like nose, jsonpickle etc. 
These dependencies are defined in the ```requirements.txt``` file that comes with the SDK.
To resolve these dependencies, you can use the PIP Dependency manager. Install it by following steps at [https://pip.pypa.io/en/stable/installing/](https://pip.pypa.io/en/stable/installing/).

Python and PIP executables should be defined in your PATH. Open command prompt and type ```pip --version```.
This should display the version of the PIP Dependency Manager installed if your installation was successful and the paths are properly defined.

* Using command line, navigate to the directory containing the generated files (including ```requirements.txt```) for the SDK.
* Run the command ```pip install -r requirements.txt```. This should install all the required dependencies.

![Building SDK - Step 1](https://apidocs.io/illustration/python?step=installDependencies&workspaceFolder=DOCSMORE%20API-Python)


## How to Use

The following section explains how to use the Docsmoreapi SDK package in a new project.

### 1. Open Project in an IDE

Open up a Python IDE like PyCharm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PyCharm - Step 1](https://apidocs.io/illustration/python?step=pyCharm)

Click on ```Open``` in PyCharm to browse to your generated SDK directory and then click ```OK```.

![Open project in PyCharm - Step 2](https://apidocs.io/illustration/python?step=openProject0&workspaceFolder=DOCSMORE%20API-Python)     

The project files will be displayed in the side bar as follows:

![Open project in PyCharm - Step 3](https://apidocs.io/illustration/python?step=openProject1&workspaceFolder=DOCSMORE%20API-Python&projectName=docsmoreapi)     

### 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PyCharm - Step 1](https://apidocs.io/illustration/python?step=createDirectory&workspaceFolder=DOCSMORE%20API-Python&projectName=docsmoreapi)

Name the directory as "test"

![Add a new project in PyCharm - Step 2](https://apidocs.io/illustration/python?step=nameDirectory)
   
Add a python file to this project with the name "testsdk"

![Add a new project in PyCharm - Step 3](https://apidocs.io/illustration/python?step=createFile&workspaceFolder=DOCSMORE%20API-Python&projectName=docsmoreapi)

Name it "testsdk"

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?step=nameFile)

In your python file you will be required to import the generated python library using the following code lines

```Python
from docsmoreapi.docsmoreapi_client import DocsmoreapiClient
```

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?step=projectFiles&workspaceFolder=DOCSMORE%20API-Python&libraryName=docsmoreapi.docsmoreapi_client&projectName=docsmoreapi&className=DocsmoreapiClient)

After this you can write code to instantiate an API client object, get a controller object and  make API calls. Sample code is given in the subsequent sections.

### 3. Run the Test Project

To run the file within your test project, right click on your Python file inside your Test project and click on ```Run```

![Run Test Project - Step 1](https://apidocs.io/illustration/python?step=runProject&workspaceFolder=DOCSMORE%20API-Python&libraryName=docsmoreapi.docsmoreapi_client&projectName=docsmoreapi&className=DocsmoreapiClient)


## How to Test

You can test the generated SDK and the server with automatically generated test
cases. unittest is used as the testing framework and nose is used as the test
runner. You can run the tests as follows:

  1. From terminal/cmd navigate to the root directory of the SDK.
  2. Invoke ```pip install -r test-requirements.txt```
  3. Invoke ```nosetests```

## Initialization

### 

API client can be initialized as following.

```python

client = DocsmoreapiClient()
```



# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [GetAnAccessTokenController](#get_an_access_token_controller)
* [DOCUMENTFLOWSController](#documentflows_controller)

## <a name="get_an_access_token_controller"></a>![Class: ](https://apidocs.io/img/class.png ".GetAnAccessTokenController") GetAnAccessTokenController

### Get controller instance

An instance of the ``` GetAnAccessTokenController ``` class can be accessed from the API Client.

```python
 get_an_access_token_client = client.get_an_access_token
```

### <a name="create_get_auth_token"></a>![Method: ](https://apidocs.io/img/method.png ".GetAnAccessTokenController.create_get_auth_token") create_get_auth_token

> *Tags:*  ``` Skips Authentication ``` 

> Make sure you call this in server side code. Exposing apiKey and clientSecret is a not a good idea on front end.

```python
def create_get_auth_token(self,
                              body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body_value = "{    \"apiKey\": \"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX\",    \"clientSecret\": \"XXXXXXXXXXXXX\"}"
body = json.loads(body_value)

result = get_an_access_token_client.create_get_auth_token(body)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="documentflows_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DOCUMENTFLOWSController") DOCUMENTFLOWSController

### Get controller instance

An instance of the ``` DOCUMENTFLOWSController ``` class can be accessed from the API Client.

```python
 document_flows_client = client.document_flows
```

### <a name="get_document_flow_collection"></a>![Method: ](https://apidocs.io/img/method.png ".DOCUMENTFLOWSController.get_document_flow_collection") get_document_flow_collection

> *Tags:*  ``` Skips Authentication ``` 

> Document Flow Collection

```python
def get_document_flow_collection(self)
```

#### Example Usage

```python

result = document_flows_client.get_document_flow_collection()

```


[Back to List of Controllers](#list_of_controllers)



