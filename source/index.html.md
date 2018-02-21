---
title: APIDocs

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:
  - <a target="_blank" href='http://gb2-st-trackingservice-001.io.thehut.local'>Sign Up for a Developer Key</a>

includes:
  - errors

search: true
---

# Glossybox Violet Supertool!!!

Welcome to the VIOLET API! You can use our API to access VIOLET API endpoints, which can get information on various cats, kittens, and breeds in our database.

We have language bindings in Shell, PHP, and Javascript! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.


# Authentication

> To authorize, use this code:

```shell
curl "http://gb2-st-trackingservice-001.io.thehut.local"
    -H "Authorization: yourapikey"
```

> Make sure to replace `yourapikey` with your API key.

<aside class="notice">
VIOLET uses API keys to allow access to the API. Check our portal for your own API key.
VIOLET expects the API key to be included in all API requests to the server in a header that looks like the following:
</aside>

# Trackings

## Get All Trackings

```shell
curl http://gb2-st-trackingservice-001.io.thehut.local/violet/api/trackings
    -H "Content-type: application/json"
    -H "Accept: application/json"
```

> The above command returns JSON structured like this:

```json
{  
   "trackings":[  
      {  
         "tracking_number":"52060900714668551970",
         "createdAt":"2018-02-21T11:27:30+00:00",
         "updatedAt":"2018-02-21T11:27:30+00:00",
         "historyCount":2,
         "history":{  
            "data":[  
               {  
                  "id":1,
                  "createdAt":"2018-02-21T11:27:30+00:00",
                  "updatedAt":"2018-02-21T11:27:30+00:00",
                  "status":"528"
               },
               {  
                  "id":2,
                  "createdAt":"2018-02-21T11:27:30+00:00",
                  "updatedAt":"2018-02-21T11:27:30+00:00",
                  "status":"528"
               }
            ]
         }
      }
  ]
}
```

This endpoint retrieves all trackings.

## Get a Specific tracking

```shell
curl http://gb2-st-trackingservice-001.io.thehut.local/violet/api/trackings/52060900714668551970
    -H "Content-type: application/json"
    -H "Accept: application/json"
```

> The above command returns JSON structured like this:

```json
{
  "tracking": {
    "tracking_number": "52060900714668551970",
    "createdAt": "2018-02-21T11:27:30+00:00",
    "updatedAt": "2018-02-21T11:27:30+00:00",
    "historyCount": 2,
    "history": {
      "data": [
        {
          "id": 1,
          "createdAt": "2018-02-21T11:27:30+00:00",
          "updatedAt": "2018-02-21T11:27:30+00:00",
          "status": "528"
        },
        {
          "id": 2,
          "createdAt": "2018-02-21T11:27:30+00:00",
          "updatedAt": "2018-02-21T11:27:30+00:00",
          "status": "528"
        }
      ]
    }
  }
}
```

This endpoint retrieves a specific tracking.

### Parameters

Parameter | Description
--------- | -----------
Number | The Number of the tracking to retrieve








## Add a tracking

```shell
curl http://gb2-st-trackingservice-001.io.thehut.local/violet/api/trackings
    -H "Content-type: application/json"
    -H "Accept: application/json"
    -d '{"shipment_number":"10000028", "order_number":"100000028,"tracking_number":"52060900714668551970", "internal_service_id":"1"}' 
    -X POST
```

> The above command returns JSON structured like this:  

```json
{
  "success": true
}
```

This endpoint adds a tracking.








## Update a tracking

```shell
curl http://gb2-st-trackingservice-001.io.thehut.local/violet/api/trackings/52060900714668551970
    -H "Content-type: application/json"
    -H "Accept: application/json"
    -d '{"shipment_number":"10000028", "order_number":"100000028,"tracking_number":"52060900714668551970", "internal_service_id":"1"}' 
    -X PUT 
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint updates a tracking.

### Parameters

Parameter | Description
--------- | -----------
Number | The Number of the tracking to update




## Delete a tracking

```shell
curl http://gb2-st-trackingservice-001.io.thehut.local/violet/api/trackings/52060900714668551970x
    -H "Content-type: application/json"
    -H "Accept: application/json"
    -X DELETE
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint deletes a tracking.

### Parameters

Parameter | Description
--------- | -----------
Number | The Number of the tracking to delete