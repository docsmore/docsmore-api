# Getting started

TODO: Add a description

## How to Build


The generated code has dependencies over external libraries like UniRest. These dependencies are defined in the ```PodFile``` file that comes with the SDK. 
To resolve these dependencies, we use the Cocoapods package manager.
Visit https://guides.cocoapods.org/using/getting-started.html to setup Cocoapods on your system.
Open command prompt and type ```pod --version```. This should display the current version of Cocoapods installed if the installation was successful.

Using command line, navigate to the directory containing the generated files (including ```PodFile```) for the SDK. 
Run the command ```pod install```. This should install all the required dependencies and create the ```pods``` directory in your project directory.

![Installing dependencies using Cocoapods](https://apidocs.io/illustration/objc?step=AddDependencies&workspaceFolder=DOCSMORE%20API-ObjC&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPI&rootNamespace=DOCSMOREAPI)

Open the project workspace using the (DOCSMOREAPI.xcworkspace) file. Invoke the build process using `Command(⌘)+B` shortcut key or using the `Build` menu as shown below.

![Building SDK using Xcode](https://apidocs.io/illustration/objc?step=BuildSDK&workspaceFolder=DOCSMORE%20API-ObjC&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPI&rootNamespace=DOCSMOREAPI)


## How to Use

The generated code is a Cocoa Touch Static Library which can be used in any iOS project. The support for these generated libraries go all the way back to iOS 6.

The following section explains how to use the DOCSMOREAPI library in a new iOS project.     
### 1. Starting a new project
To start a new project, left-click on the ```Create a new Xcode project```.
![Create Test Project - Step 1](https://apidocs.io/illustration/objc?step=Test1&workspaceFolder=DOCSMORE%20API-ObjC&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPI&rootNamespace=DOCSMOREAPI)

Next, choose **Single View Application** and click ```Next```.
![Create Test Project - Step 2](https://apidocs.io/illustration/objc?step=Test2&workspaceFolder=DOCSMORE%20API-ObjC&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPI&rootNamespace=DOCSMOREAPI)

Provide **Test-Project** as the product name click ```Next```.
![Create Test Project - Step 3](https://apidocs.io/illustration/objc?step=Test3&workspaceFolder=DOCSMORE%20API-ObjC&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPI&rootNamespace=DOCSMOREAPI)

Choose the desired location of your project folder and click ```Create```.
![Create Test Project - Step 4](https://apidocs.io/illustration/objc?step=Test4&workspaceFolder=DOCSMORE%20API-ObjC&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPI&rootNamespace=DOCSMOREAPI)

### 2. Adding the static library dependency
To add this dependency open a terminal and navigate to your project folder. Next, input ```pod init``` and press enter.
![Add dependency - Step 1](https://apidocs.io/illustration/objc?step=Add0&workspaceFolder=DOCSMORE%20API-ObjC&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPI&rootNamespace=DOCSMOREAPI)

Next, open the newly created ```PodFile``` in your favourite text editor. Add the following line : pod 'DOCSMOREAPI', :path => 'Vendor/DOCSMOREAPI'
![Add dependency - Step 2](https://apidocs.io/illustration/objc?step=Add1&workspaceFolder=DOCSMORE%20API-ObjC&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPI&rootNamespace=DOCSMOREAPI)

Execute `pod install` from terminal to install the dependecy in your project. This would add the dependency to the newly created test project.
![Add dependency - Step 3](https://apidocs.io/illustration/objc?step=Add2&workspaceFolder=DOCSMORE%20API-ObjC&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPI&rootNamespace=DOCSMOREAPI)


## How to Test

Unit tests in this SDK can be run using Xcode. 

First build the SDK as shown in the steps above and naivgate to the project directory and open the DOCSMOREAPI.xcworkspace file.

Go to the test explorer in Xcode as shown in the picture below and click on `run tests` from the menu. 
![Run tests](https://apidocs.io/illustration/objc?step=RunTests&workspaceFolder=DOCSMORE%20API-ObjC&workspaceName=DOCSMOREAPI&projectName=DOCSMOREAPI&rootNamespace=DOCSMOREAPI)


## Initialization

### 

Configuration variables can be set as following.
```Objc

```

# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [GetAnAccessTokenController](#get_an_access_token_controller)
* [DOCUMENTFLOWSController](#documentflows_controller)

## <a name="get_an_access_token_controller"></a>![Class: ](https://apidocs.io/img/class.png ".GetAnAccessTokenController") GetAnAccessTokenController

### Get singleton instance
```objc
GetAnAccessToken* getAnAccessToken = [[GetAnAccessToken alloc]init] ;
```

### <a name="create_get_auth_token_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".GetAnAccessTokenController.createGetAuthTOKENAsyncWithBody") createGetAuthTOKENAsyncWithBody

> *Tags:*  ``` Skips Authentication ``` 

> Make sure you call this in server side code. Exposing apiKey and clientSecret is a not a good idea on front end.


```objc
function createGetAuthTOKENAsyncWithBody:(GetAuthTOKENRequest*) body
                completionBlock:(CompletedPostGetAuthTOKEN) onCompleted(body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    GetAuthTOKENRequest* body = (GetAuthTOKENRequest*) [APIHelper jsonDeserialize: @"{    \"apiKey\": \"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX\",    \"clientSecret\": \"XXXXXXXXXXXXX\"}"
                toClass: GetAuthTOKENRequest.class];

    [self.getAnAccessToken createGetAuthTOKENAsyncWithBody: body  completionBlock:^(BOOL success, HttpContext* context, GetAuthTOKENResponse* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="documentflows_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DOCUMENTFLOWSController") DOCUMENTFLOWSController

### Get singleton instance
```objc
DOCUMENTFLOWS* dOCUMENTFLOWS = [[DOCUMENTFLOWS alloc]init] ;
```

### <a name="get_document_flow_collection_with_completion_block"></a>![Method: ](https://apidocs.io/img/method.png ".DOCUMENTFLOWSController.getDocumentFlowCollectionWithCompletionBlock") getDocumentFlowCollectionWithCompletionBlock

> *Tags:*  ``` Skips Authentication ``` 

> Document Flow Collection


```objc
function getDocumentFlowCollectionWithCompletionBlock:(CompletedGetDocumentFlowCollection) onCompleted()
```



#### Example Usage

```objc

    [self.dOCUMENTFLOWS getDocumentFlowCollectionWithCompletionBlock:  ^(BOOL success, HttpContext* context, NSArray<DocumentFlowCollectionResponse> * response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)



