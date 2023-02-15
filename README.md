

# LocationPublicApi
Sections

[1.Base API Url](https://github.com/locationbank/LocationPublicApi/blob/main/README.md#1base-api-url)

[2.List of All Locations](https://github.com/locationbank/LocationPublicApi/blob/main/README.md#2list-of-all-locations)

[3.Create location](https://github.com/locationbank/LocationPublicApi/blob/main/README.md#3create-locations)

[4.Get Single Location](https://github.com/locationbank/LocationPublicApi/blob/main/README.md#4get-single-location)

[5.Update location](https://github.com/locationbank/LocationPublicApi/blob/main/README.md#5update-location)


<details> 
  <summary><strong><h1>1.Base API Url</h1>
</strong>
</summary>

All endpoints described in this document with the exception of Reporting have the following base API url: https://api.places.digital/locations-api-write/
</details> 

---

<h1>2.List of All Locations</h1>

<details> 
  <summary><strong><h2>GET / (Http EndPoint: /locations)</h2>
</strong>
</summary>
  
  ##### Headers Parameters

> | name                             |  type     | data type               | description                                                           |
> |----------------------------------|-----------|-------------------------|-----------------------------------------------------------------------|
> | Ocp-Apim-Subscription-Key        |  required  | string                  | Passed into **header** for Authorization                                 |
> | Content-Type                      |  required  | application/json                                      |

    
  ##### QueryString Parameters

> | name                             |  type     | data type               | description                                                           |
> |----------------------------------|-----------|-------------------------|-----------------------------------------------------------------------|
> | AccountID                         |  required  | uuid                  | The unique identifier for the Account                             |



##### Responses

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `200`         | `text/plain;charset=UTF-8`        | [Response Json Body](https://github.com/locationbank/LocationPublicApi/blob/main/ResponseJsonBodyArray.md)

                      
 
  
[Response Description](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md)

</details> 

---

<h1>3.Create Locations</h1>
<details> 
  <summary><strong><h2>POST / (Http EndPoint:  /location)</h2>
</strong>
</summary>
  
  ##### Headers Parameters

> | name                             |  type     | data type               | description                                                           |
> |----------------------------------|-----------|-------------------------|-----------------------------------------------------------------------|
> | Ocp-Apim-Subscription-Key        |  required  | string                  | Passed into **header** for Authorization                                 |
> | Content-Type                      |  required  | application/json                                      |

    
  ##### FromBody Parameters

> | name                             |  type     | data type               | description                                                           |
> |----------------------------------|-----------|-------------------------|-----------------------------------------------------------------------|
> | LocationBankPublic Object         |Required  | Object                  | [LocationBankPublic Object](https://github.com/locationbank/LocationPublicApi/blob/main/ResponseJsonBody.md)                             |

  [Request Description](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md)



##### Responses

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `200`         | `text/plain;charset=UTF-8`        | [Response Json Body](https://github.com/locationbank/LocationPublicApi/blob/main/ResponseJsonBody.md)
 > | `400`         | 'application/json'                | "Field is Required"
> | `500`         | `'application/json'               | "Error Message"
                      
 
  
[Response Description](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md)

</details> 

---

<h1>4.Get Single Location</h1>
<details> 
  <summary><strong><h2>GET / (Http EndPoint: /location)</h2>
</strong>
</summary>
  
  ##### Headers Parameters

> | name                             |  type     | data type               | description                                                           |
> |----------------------------------|-----------|-------------------------|-----------------------------------------------------------------------|
> | Ocp-Apim-Subscription-Key        |  required  | string                  | Passed into **header** for Authorization                                 |
> | Content-Type                      |  required  | application/json                                      |

    
  ##### QueryString Parameters

> | name                             |  type     | data type               | description                                                           |
> |----------------------------------|-----------|-------------------------|-----------------------------------------------------------------------|
> | AccountID                         |  required  | uuid                  | The unique identifier for the Account                             |
> | LocationID                         |    | uuid                  | The unique identifier for the Location                             |
> | LocationNumber                         |    | string                  | A friendly number used internally to reference the specified Location (for support purposes)                            |
> | ReferenceCode                         |    | uuid                  | An identifier for the Location specified by the user of the API                          |



##### Responses

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `200`         | `text/plain;charset=UTF-8`        | [Response Json Body](https://github.com/locationbank/LocationPublicApi/blob/main/ResponseJsonBody.md)

                      
 
  
[Response Description](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md)

</details> 

---

<h1>5.Update Location</h1>
<details> 
  <summary><strong><h2>PUT / (Http EndPoint:  /location)</h2>
</strong>
</summary>
  
  ##### Headers Parameters

> | name                             |  type     | data type               | description                                                           |
> |----------------------------------|-----------|-------------------------|-----------------------------------------------------------------------|
> | Ocp-Apim-Subscription-Key        |  required  | string                  | Passed into **header** for Authorization                                 |
> | Content-Type                      |  required  | application/json                                      |

    
  ##### FromBody Parameters

> | name                             |  type     | data type               | description                                                           |
> |----------------------------------|-----------|-------------------------|-----------------------------------------------------------------------|
> | LocationBankPublic Object         |Required  | Object                  | [LocationBankPublic Object](https://github.com/locationbank/LocationPublicApi/blob/main/ResponseJsonBody.md)                             |

  [Request Description](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md)


##### Responses

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `200`         | `text/plain;charset=UTF-8`        | [Response Json Body](https://github.com/locationbank/LocationPublicApi/blob/main/ResponseJsonBody.md)
 > | `400`         | 'application/json'                | "Field is Required"
> | `500`         | `'application/json'               | "Error Message"
                      
 
  
[Response Description](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md)

</details> 

---

<h1>6.Publish All Locations</h1>
<details> 
  <summary><strong><h2>GET / (Http EndPoint:  /publish)</h2>
</strong>
</summary>
  
  ##### Headers Parameters

> | name                             |  type     | data type               | description                                                           |
> |----------------------------------|-----------|-------------------------|-----------------------------------------------------------------------|
> | Ocp-Apim-Subscription-Key        |  required  | string                  | Passed into **header** for Authorization                                 |
> | Content-Type                      |  required  | application/json                                      |

  ##### QueryString Parameters

> | name                             |  type     | data type               | description                                                           |
> |----------------------------------|-----------|-------------------------|-----------------------------------------------------------------------|
> | AccountID                         |  required  | uuid                  | The unique identifier for the Account                             |
 
##### Responses

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `200`         | `text/plain;charset=UTF-8`        | [Response Json Body] Boolean 

      

</details> 


