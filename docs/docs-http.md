# 

**`API Version:`** `1.0`

TODO: Add a description



## Base URL

The base URL for this API is `https://api.docsmore.com/`









# <a name="api_reference"></a>API Reference

* [Get an Access Token](#get_an_access_token)
* [DOCUMENT FLOWS](#document_flows)

## <a name="get_an_access_token"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Get an Access Token") Get an Access Token


### <a name="get_auth_token"></a>![Endpoint: ](https://apidocs.io/img/method.png "Get Auth TOKEN") Get Auth TOKEN


**`POST`** `/auth/authtoken`

> *Tags:*  ``` Skips Authentication ``` 

> Make sure you call this in server side code. Exposing apiKey and clientSecret is a not a good idea on front end.




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [Get Auth TOKEN request](#get_auth_token_request) |  ``` Required ```  | - | 

 *Example Request Body* 
``` 
{
  "apiKey": "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX",
  "clientSecret": "XXXXXXXXXXXXX"
}
``` 

#### Responses
**200** 


 *Example Body* (**[Get Auth TOKEN response](#get_auth_token_response)**) 

```
{
  "access_token": "eyXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
}
```


[Back to API Reference](#api_reference)

## <a name="document_flows"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "DOCUMENT FLOWS") DOCUMENT FLOWS


### <a name="document_flow_collection"></a>![Endpoint: ](https://apidocs.io/img/method.png "Document Flow Collection") Document Flow Collection


**`GET`** `/api/docflow/getdocflows`

> *Tags:*  ``` Skips Authentication ``` 

> Document Flow Collection




#### Responses
**200** 


 *Example Body* (**[[Document Flow Collection response](#document_flow_collection_response)]**) 

```
[
  {
    "_id": "58fa4b45b3611e0d28000020",
    "flowName": "Bathroom remodeling project",
    "userid": {
      "_id": "58fa0ab6b3611e0d2800000c",
      "userEmail": "ethitrans@docsmore.com"
    },
    "primaryKey": "_id",
    "firstNameKey": "null",
    "lastNameKey": "null",
    "apikey": "{Document Flow API Key}",
    "createdOn": "\"2017-04-21T18:11:17.126Z\""
  },
  {
    "_id": "58fa4bb9b3611e0d28000021",
    "flowName": "Kitchen remodeling project",
    "userid": {
      "_id": "58fa0ab6b3611e0d2800000c",
      "userEmail": "ethitrans@docsmore.com"
    },
    "primaryKey": "_id",
    "firstNameKey": "null",
    "lastNameKey": "null",
    "apikey": "{Document Flow API Key}",
    "createdOn": "\"2017-04-21T18:13:13.527Z\""
  },
  {
    "_id": "58fa6cd0b3611e0d2800006f",
    "flowName": "Office Paper works",
    "userid": {
      "_id": "58fa0ab6b3611e0d2800000c",
      "userEmail": "ethitrans@docsmore.com"
    },
    "primaryKey": "_id",
    "firstNameKey": "null",
    "lastNameKey": "null",
    "apikey": "{ Document Flow API Key }",
    "createdOn": "\"2017-04-21T20:34:24.471Z\""
  }
]
```


[Back to API Reference](#api_reference)

# <a name="models"></a> Models

### List of Models

* [Get Auth TOKEN response](#get_auth_token_response)
* [Get Auth TOKEN request](#get_auth_token_request)
* [Document Flow Collection response](#document_flow_collection_response)
## <a name="get_auth_token_response"></a>![Type: ](https://apidocs.io/img/method.png "Get Auth TOKEN response") Get Auth TOKEN response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| access_token | string |  ``` Required ```  | - | 



#### Example
```
{
  "access_token": "eyXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
}
```



## <a name="get_auth_token_request"></a>![Type: ](https://apidocs.io/img/method.png "Get Auth TOKEN request") Get Auth TOKEN request








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| apiKey | string |  ``` Required ```  | - | 
| clientSecret | string |  ``` Required ```  | - | 



#### Example
```
{
  "apiKey": "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX",
  "clientSecret": "XXXXXXXXXXXXX"
}
```



## <a name="document_flow_collection_response"></a>![Type: ](https://apidocs.io/img/method.png "Document Flow Collection response") Document Flow Collection response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| _id | string |  ``` Required ```  | - | 
| flowName | string |  ``` Required ```  | - | 
| userid | object |  ``` Required ```  | - | 
| primaryKey | string |  ``` Required ```  | - | 
| firstNameKey | string |  ``` Required ```  | - | 
| lastNameKey | string |  ``` Required ```  | - | 
| apikey | string |  ``` Required ```  | - | 
| createdOn | string |  ``` Required ```  | - | 



#### Example
```
{
  "_id": "58fa4b45b3611e0d28000020",
  "flowName": "Bathroom remodeling project",
  "userid": {
    "_id": "58fa0ab6b3611e0d2800000c",
    "userEmail": "ethitrans@docsmore.com"
  },
  "primaryKey": "_id",
  "firstNameKey": "null",
  "lastNameKey": "null",
  "apikey": "{Document Flow API Key}",
  "createdOn": "\"2017-04-21T18:11:17.126Z\""
}
```




