# Getting started

TODO: Add a description

## How to Build

The generated code uses a few Maven dependencies e.g., Jackson, UniRest,
and Apache HttpClient. The reference to these dependencies is already
added in the pom.xml file will be installed automatically. Therefore,
you will need internet access for a successful build.

* In order to open the client library in Eclipse click on ``` File -> Import ```.

![Importing SDK into Eclipse - Step 1](https://apidocs.io/illustration/java?step=import0&workspaceFolder=DOCSMORE%20API-Java&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPILib&rootNamespace=com.docsmore.api)

* In the import dialog, select ``` Existing Java Project ``` and click ``` Next ```.

![Importing SDK into Eclipse - Step 2](https://apidocs.io/illustration/java?step=import1&workspaceFolder=DOCSMORE%20API-Java&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPILib&rootNamespace=com.docsmore.api)

* Browse to locate the folder containing the source code. Select the detected location of the project and click ``` Finish ```.

![Importing SDK into Eclipse - Step 3](https://apidocs.io/illustration/java?step=import2&workspaceFolder=DOCSMORE%20API-Java&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPILib&rootNamespace=com.docsmore.api)

* Upon successful import, the project will be automatically built by Eclipse after automatically resolving the dependencies.

![Importing SDK into Eclipse - Step 4](https://apidocs.io/illustration/java?step=import3&workspaceFolder=DOCSMORE%20API-Java&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPILib&rootNamespace=com.docsmore.api)

## How to Use

The following section explains how to use the DOCSMOREAPI library in a new console project.

### 1. Starting a new project

For starting a new project, click the menu command ``` File > New > Project ```.

![Add a new project in Eclipse](https://apidocs.io/illustration/java?step=createNewProject0&workspaceFolder=DOCSMORE%20API-Java&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPILib&rootNamespace=com.docsmore.api)

Next, choose ``` Maven > Maven Project ```and click ``` Next ```.

![Create a new Maven Project - Step 1](https://apidocs.io/illustration/java?step=createNewProject1&workspaceFolder=DOCSMORE%20API-Java&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPILib&rootNamespace=com.docsmore.api)

Here, make sure to use the current workspace by choosing ``` Use default Workspace location ```, as shown in the picture below and click ``` Next ```.

![Create a new Maven Project - Step 2](https://apidocs.io/illustration/java?step=createNewProject2&workspaceFolder=DOCSMORE%20API-Java&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPILib&rootNamespace=com.docsmore.api)

Following this, select the *quick start* project type to create a simple project with an existing class and a ``` main ``` method. To do this, choose ``` maven-archetype-quickstart ``` item from the list and click ``` Next ```.

![Create a new Maven Project - Step 3](https://apidocs.io/illustration/java?step=createNewProject3&workspaceFolder=DOCSMORE%20API-Java&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPILib&rootNamespace=com.docsmore.api)

In the last step, provide a ``` Group Id ``` and ``` Artifact Id ``` as shown in the picture below and click ``` Finish ```.

![Create a new Maven Project - Step 4](https://apidocs.io/illustration/java?step=createNewProject4&workspaceFolder=DOCSMORE%20API-Java&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPILib&rootNamespace=com.docsmore.api)

### 2. Add reference of the library project

The created Maven project manages its dependencies using its ``` pom.xml ``` file. In order to add a dependency on the *DOCSMOREAPILib* client library, double click on the ``` pom.xml ``` file in the ``` Package Explorer ```. Opening the ``` pom.xml ``` file will render a graphical view on the cavas. Here, switch to the ``` Dependencies ``` tab and click the ``` Add ``` button as shown in the picture below.

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/java?step=testProject0&workspaceFolder=DOCSMORE%20API-Java&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPILib&rootNamespace=com.docsmore.api)

Clicking the ``` Add ``` button will open a dialog where you need to specify DOCSMOREAPI in ``` Group Id ``` and DOCSMOREAPILib in the ``` Artifact Id ``` fields. Once added click ``` OK ```. Save the ``` pom.xml ``` file.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/java?step=testProject1&workspaceFolder=DOCSMORE%20API-Java&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPILib&rootNamespace=com.docsmore.api)

### 3. Write sample code

Once the ``` SimpleConsoleApp ``` is created, a file named ``` App.java ``` will be visible in the *Package Explorer* with a ``` main ``` method. This is the entry point for the execution of the created project.
Here, you can add code to initialize the client library and instantiate a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/java?step=testProject2&workspaceFolder=DOCSMORE%20API-Java&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPILib&rootNamespace=com.docsmore.api)

## How to Test

The generated code and the server can be tested using automatically generated test cases. 
JUnit is used as the testing framework and test runner.

In Eclipse, for running the tests do the following:

1. Select the project *DOCSMOREAPILib* from the package explorer.
2. Select "Run -> Run as -> JUnit Test" or use "Alt + Shift + X" followed by "T" to run the Tests.

## Initialization

### 

API client can be initialized as following.

```java

DOCSMOREAPIClient client = new DOCSMOREAPIClient();
```


# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [GetAnAccessTokenController](#get_an_access_token_controller)
* [DOCUMENTFLOWSController](#documentflows_controller)

## <a name="get_an_access_token_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.docsmore.api.controllers.GetAnAccessTokenController") GetAnAccessTokenController

### Get singleton instance

The singleton instance of the ``` GetAnAccessTokenController ``` class can be accessed from the API Client.

```java
GetAnAccessTokenController getAnAccessToken = client.getGetAnAccessToken();
```

### <a name="create_get_auth_token_async"></a>![Method: ](https://apidocs.io/img/method.png "com.docsmore.api.controllers.GetAnAccessTokenController.createGetAuthTOKENAsync") createGetAuthTOKENAsync

> *Tags:*  ``` Skips Authentication ``` 

> Make sure you call this in server side code. Exposing apiKey and clientSecret is a not a good idea on front end.


```java
void createGetAuthTOKENAsync(
        final GetAuthTOKENRequest body,
        final APICallBack<GetAuthTOKENResponse> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    String bodyValue = "{    \"apiKey\": \"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX\",    \"clientSecret\": \"XXXXXXXXXXXXX\"}";
    GetAuthTOKENRequest body = mapper.readValue(bodyValue,new TypeReference<GetAuthTOKENRequest> (){});
    // Invoking the API call with sample inputs
    getAnAccessToken.createGetAuthTOKENAsync(body, new APICallBack<GetAuthTOKENResponse>() {
        public void onSuccess(HttpContext context, GetAuthTOKENResponse response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="documentflows_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.docsmore.api.controllers.DOCUMENTFLOWSController") DOCUMENTFLOWSController

### Get singleton instance

The singleton instance of the ``` DOCUMENTFLOWSController ``` class can be accessed from the API Client.

```java
DOCUMENTFLOWSController dOCUMENTFLOWS = client.getDOCUMENTFLOWS();
```

### <a name="get_document_flow_collection_async"></a>![Method: ](https://apidocs.io/img/method.png "com.docsmore.api.controllers.DOCUMENTFLOWSController.getDocumentFlowCollectionAsync") getDocumentFlowCollectionAsync

> *Tags:*  ``` Skips Authentication ``` 

> Document Flow Collection


```java
void getDocumentFlowCollectionAsync(final APICallBack<List<DocumentFlowCollectionResponse>> callBack)
```

#### Example Usage

```java
// Invoking the API call with sample inputs
dOCUMENTFLOWS.getDocumentFlowCollectionAsync(new APICallBack<List<DocumentFlowCollectionResponse>>() {
    public void onSuccess(HttpContext context, List<DocumentFlowCollectionResponse> response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)



