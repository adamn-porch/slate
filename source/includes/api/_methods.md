## Methods

### Create Listing

```json
{
   "testEmail":"test.porch@brokerage.com",
   "listingId":"31040547",
   "listingStatus":"Active",
   "listingPrice":548000,
   "listingPriceCurrencyCode":"USD",
   "listingUrl":"http://www.brokerage.com/listing/WA/Shoreline/2301-NW-204th-St-98177/31040547",
   "listingDescription":"This immaculate home is ready for your holiday…",
   "property":{
      "address":{
         "line1":"2301 NW 204th St",
         "line2":"",
         "city":"Shoreline",
         "state":"WA",
         "postalCode":"98177",
         "county":"King",
         "latitude":47.777204,
         "longitude":-122.387488,
         "neighborhood":"Richmond Beach"
      },
      "bedrooms":5,
      "bathrooms":2.5,
      "propertyType":"Single Family Home",
      "sqftLiving":2650,
      "sqftLot":9140,
      "yearBuilt":"1965",
      "units":1
   },
   "provider":{
      "name":"MLS Broker",
      "websiteUrl":"http://www.brokerage.com"
   },
   "mls":{
      "number":555555555,
      "name":"MLS Name"
   },
   "brokerage":{
      "name":"Broker Name",
      "phoneNumber":"5555555555",
      "email":"info@ brokerage.com",
      "websiteUrl":"http://www.brokerage.com",
      "logoUrl":"http://www. brokerage.com/assets/logo.png",
      "addressLine1":"",
      "addressLine2":"",
      "addressCity":"",
      "addressState":"",
      "addressPostalCode":""
   },
   "agents":[
      {
         "name":"Agent Name",
         "title":"Best Broker",
         "email":"agent.name@brokerage.com",
         "websiteUrl":"http://www.agentnamewebsite.com",
         "profileUrl":"http://www.brokerage.com/agents/agent.name",
         "officeName":"",
         "officePhoneNumber":"5555555555",
         "photoUrl":"http://brokerage.com/img/agent.name.png",
         "agentId":"agent.name.id",
         "agentType":"listing",
         "receivePorchEmail":true
      }
   ],
   "photos":[
      {
         "url":"http://brokerage.com/listing-img/31040547?num=1",
         "caption":"",
         "description":""
      },
      {
         "url":" http://brokerage.com/listing-img/31040547?num=2",
         "caption":"",
         "description":""
      },
      {
         "url":" http://brokerage.com/listing-img/31040547?num=3",
         "caption":"",
         "description":""
      },
      {
         "url":" http://brokerage.com/listing-img/31040547?num=4",
         "caption":"",
         "description":""
      }
   ]
}
```

```java
```

```csharp
using System.Net.Http;

using (var client = new HttpClient())
{
    var listing = new Listing();    
    client.DefaultRequestHeaders.Add("api-key", "partnerApiKey");
    var response = await client.PostAsync("https://api.porch.com/v1/partner/utmSource/listings", listing);
    var responseString = await response.Content.ReadAsStringAsync();
}
```

```php
<?php

$Listing = new Listing();
$Listing->testEmail-> = 'email@email.com';

?>
```

> The above command returns JSON structured like this:

```json
{
   "listingId":"5e26f3ba-6501-452f-86d0-a9c3abc5ed32",
   "linkResource":{
      "apiUrl": "http://api.porch.com/v1/partners/utmsource/listings/5e26f3ba-6501-452f-86d0-a9c3abc5ed32/resources/links",
      "links":[
         {
            "label":"See Improvements",
            "url":"https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=See Improvements",
            "linkType":"improvement"
         },
         {
            "label":"See Renovations",
            "url":" https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=See Renovations",
            "linkType":"renovation"
         },
         {
            "label":"Get Renovation Report",
            "url":" https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=Get Renovation Report",
            "linkType":"renovation-report"
         },
         {
            "label":"See Permit History",
            "url":" https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=See Permit History",
            "linkType":"permit"
         },
         {
            "label":"Get Neighborhood Trends",
            "url":" https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=Get Neighborhood Trends",
            "linkType":"neighborhood"
         }
      ]
   }
}
```

```java
```

```csharp
```

```php
array (
  'ListingId' => '5e26f3ba-6501-452f-86d0-a9c3abc5ed32'
)
```

This endpoint creates a new listing then return resources associated with that listing.

#### HTTP Request

`POST https://api.porch.com/v1/partners/{utmSource}/listings`

#### URL Parameters

Parameter | Description
--------- | -----------
utmSource | The utm source created by Porch

### Get Listing

```json
```

```java
```

```csharp
using System.Net.Http;

using (var client = new HttpClient()){
    var listing = new Listing();    
    client.DefaultRequestHeaders.Add("api-key", "partnerApiKey");
    var response = await client.GetAsync("https://api.porch.com/v1/partner/utmSource/listings/listingId");
    var responseString = await response.Content.ReadAsStringAsync();
}
```

> The above command returns JSON structured like this:

```json
{
   "listingId":"5e26f3ba-6501-452f-86d0-a9c3abc5ed32",
   "linkResource":{
      "apiUrl": "http://api.porch.com/v1/partners/utmsource/listings/5e26f3ba-6501-452f-86d0-a9c3abc5ed32/resources/links",
      "links":[
         {
            "label":"See Improvements",
            "url":"https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=See Improvements",
            "linkType":"improvement"
         },
         {
            "label":"See Renovations",
            "url":" https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=See Renovations",
            "linkType":"renovation"
         },
         {
            "label":"Get Renovation Report",
            "url":" https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=Get Renovation Report",
            "linkType":"renovation-report"
         },
         {
            "label":"See Permit History",
            "url":" https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=See Permit History",
            "linkType":"permit"
         },
         {
            "label":"Get Neighborhood Trends",
            "url":" https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=Get Neighborhood Trends",
            "linkType":"neighborhood"
         }
      ]
   }
}
```

```java
```

```csharp
```

#### HTTP Request

`GET https://api.porch.com/v1/partners/{utmSource}/listings/{listingId}`

#### URL Parameters

Parameter | Description
--------- | -----------
utmSource | The utm source created by Porch
listingId | The listing id of the listing to retrieve

### Get Listing Resources

```json
```

```java
```

```csharp
using System.Net.Http;

using (var client = new HttpClient()){
    var listing = new Listing();
    client.DefaultRequestHeaders.Add("api-key", "partnerApiKey");
    var response = await client.GetAsync("https://api.porch.com/v1/partner/utmSource/listings/listingId/resources");
    var responseString = await response.Content.ReadAsStringAsync();
}
```

> The above command returns JSON structured like this:

```json
{
   "listingId":"5e26f3ba-6501-452f-86d0-a9c3abc5ed32",
   "linkResource":{
      "apiUrl": "http://api.porch.com/v1/partners/utmsource/listings/5e26f3ba-6501-452f-86d0-a9c3abc5ed32/resources/links",
      "links":[
         {
            "label":"See Improvements",
            "url":"https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=See Improvements",
            "linkType":"improvement"
         },
         {
            "label":"See Renovations",
            "url":" https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=See Renovations",
            "linkType":"renovation"
         },
         {
            "label":"Get Renovation Report",
            "url":" https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=Get Renovation Report",
            "linkType":"renovation-report"
         },
         {
            "label":"See Permit History",
            "url":" https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=See Permit History",
            "linkType":"permit"
         },
         {
            "label":"Get Neighborhood Trends",
            "url":" https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=Get Neighborhood Trends",
            "linkType":"neighborhood"
         }
      ]
   }
}
```

```java
```

```csharp
```

#### HTTP Request

`GET https://api.porch.com/v1/partners/{utmSource}/listings/{listingId}/resources`

#### URL Parameters

Parameter | Description
--------- | -----------
utmSource | The utm source created by Porch
listingId | The listing id of the listing to retrieve

### Get Listing Resource Links

```json
```

```java
```

```csharp
using System.Net.Http;

using (var client = new HttpClient()){
    var listing = new Listing();
    client.DefaultRequestHeaders.Add("api-key", "partnerApiKey");
    var response = await client.GetAsync("https://api.porch.com/v1/partner/utmSource/listings/listingId/resources/links");
    var responseString = await response.Content.ReadAsStringAsync();
}
```

> The above command returns JSON structured like this:

```json
{
   "links":[
      {
         "label":"See Improvements",
         "url":"https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=See Improvements",
         "linkType":"improvement"
      },
      {
         "label":"See Renovations",
         "url":" https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=See Renovations",
         "linkType":"renovation"
      },
      {
         "label":"Get Renovation Report",
         "url":" https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=Get Renovation Report",
         "linkType":"renovation-report"
      },
      {
         "label":"See Permit History",
         "url":" https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=See Permit History",
         "linkType":"permit"
      },
      {
         "label":"Get Neighborhood Trends",
         "url":" https://porch.com/shorline-wa/homes/2301-nw-204th-st-shorline-wa-98177/1566645?lid=5e26f3ba-6501-452f-86d0-a9c3abc5ed32&utm_source=brokerage&utm_campaign=Get Neighborhood Trends",
         "linkType":"neighborhood"
      }
   ]
}
```

```java
```

```csharp
```

#### HTTP Request

`GET https://api.porch.com/v1/partners/{utmSource}/listings/{listingId}/resources/links`

#### URL Parameters

Parameter | Description
--------- | -----------
utmSource | The utm source created by Porch
listingId | The listing id of the listing to retrieve