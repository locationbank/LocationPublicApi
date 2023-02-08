<h1>Response Description</h1>

| Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|
| AccountID      | string | The unique identifier for the Account                                                                    |
| LocationID     | string | The unique identifier for the Location (auto-generated)                                                  |
| LocationNumber | string | A friendly number used internally to reference the specified Location                                    |
| ReferenceCode  | string | An identifier for the Location specified by the user of the API                                          |
| CreatedBy      | string | String indicating who or what created the Location                                                       |
| ModifiedBy     | string | String indicating who or what last modified the Location                                                 |
| Created        | string | 'Time, location was created'                                                                             |
| Modified       | string | Time location was modified                                                                               |
| KeyFields      | object | Dynamic storage of the key fields for the location or custom data which is used by specific applications |
| DisplayPoint     | Object | [DisplayPointObject](https://github.com/locationbank/LocationPublicApi/blob/main/ResponseDescription.md#displaypointobject) |  
| BusinessStatus | string | 'The Status of the Location (Open, Closed, TemporarilyClosed)'                                                                 |
| Status         | string | Record status                                                                                                                  |
| BusinessName   | Object | [BusinessNameObject](https://github.com/locationbank/LocationPublicApi/blob/main/ResponseDescription.md#businessnameobject) |   
| BusinessDescription | Object | [BusinessDescriptionObject](https://github.com/locationbank/LocationPublicApi/blob/main/ResponseDescription.md#businessdescriptionobject-)                                                       |
| PrimaryAddress | Object | [AddressObject](https://github.com/locationbank/LocationPublicApi/blob/main/ResponseDescription.md#addressobject-)  
| phoneNumbers        | Object | [PhoneNumbersObject] (https://github.com/locationbank/LocationPublicApi/blob/main/ResponseDescription.md#PhoneNumbersObject-)  |                                                                                                           
| WebsiteURL          | string | 'The Website for the Location; Must be a valid URL with only sub, main, and top-level domain information (max length 40 char)' |
| mediaURLs           | Object | [MediaURLsObject](https://github.com/locationbank/LocationPublicApi/blob/main/ResponseDescription.md#MediaURLsObject-)                                                                                                                |

<h2>DisplayPointObject</h2>

| Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                   
| Type             | enum   | - Calculated -  ManuallyPlaced                                                                       |
| Latitude         | number | '[TO BE REMOVED] Latitude of the Location represented by a high precision decimal number'            |
| Longitude        | number | '[TO BE REMOVED] Longitude of the Location represented by a high precision decimal number'           |
| VerificationType | enum   | - Client - Manually - DAC_PinIt - DAC_Goo


<h2>BusinessNameObject </h2>

| Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                   
| Name           | string | A standard length Business Name for the Location; This field is needed to submit data to Acxiom and Bing (max length 30 chars) |
| LongName       | string | A long Business Name for the Location (max length 80 chars)                                                                    |
| Locale         | string | Primary language 


  <h2>BusinessDescriptionObject </h2>
  
| Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                   
| Description         | string | A description of the Business for the Location; This field is needed to submit data to Yalwa (max length 200 chars)                                  |
| ShortDescription    | string | A short description of the Business for the Location; This field is needed to submit data to Foursquare (max length 160 chars)                       |
| longDescription     | string | A long description of the Business for the Location; This field is needed to submit data to Superpages (min length 250 chars; max length 4000 chars) |


  <h2>AddressObject </h2>
  
| Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                   
| AddressLine1   | string | First line of an address (max length 80 chars).                                                                                                                                           |
| AddressLine2   | string | econd line of an address (max length 80 chars).                                                                                                                                           |
| AddressLine3   | string | Third line of an address (max length 80 chars)                                                                                                                                            |
| AddressLine4   | string | Fourth line of an address (max length 80 chars)                                                                                                                                           |
| AddressLine5   | string | Fifth line of an address (max length 80 chars)                                                                                                                                            |
| Neighborhood   | string |  Neighborhood represents an official sub-locality - typically an area within a town or city (max length 200 chars)                                                                        |
| Locality       | string |  Locality generally represents a City or Town (max length 28 chars)                                                                                                                       |
| Region         | string | 'A Region represents the State or Province; depending on the specified CountryCode, this field may be required and the input format validated (see documentation for validation details)' |
| PostalCode     | string |  Postal Code or Zip Code; depending on the specified CountryCode, this field may be required and the input format validated (see documentation for validation details)'                   |
| CountryCode    | string | 'Two letter ISO 3166-1 alpha-2 country code representing the Country of a Location (e.g. US, CA, FR, DE, etc.)                                                                            |


  <h2>PhoneNumbersObject </h2>
  
  | Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|    
|  PrimaryPhoneNumber | string | The Primary Phone Number for the Location                                                                                      |
| Landline            | string | The Landline Phone Number for the Location                                                                                     |
| Mobile              | string | The Mobile Phone Number for the Location                                                                                       |
| Fax                 | string | The Fax Number for the Location                                                                                                |
| TollFree            | string | The Toll-Free Phone Number for the Location                                                                                    |


  <h2>MediaURLsObject  </h2>
  
  | Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|    
| FacebookURL         | string | The Facebook URL for the Location (must be a valid URL)                                                                        |
| TwitterURL          | string | The Twitter URL for the Location (must be a valid URL)                                                                         |
| LinkedInURL         | string | The LinkedIn URL for the Location (must be a valid URL)                                                                        |
| InstagramURL        | string | The Instagram URL for the Location (must be a valid URL)                                                                       |
| PinterestURL        | string | The Pinterest URL for the Location (must be a valid URL)                                                                       |
| CouponURL           | string | The Coupon URL for the Location (must be a valid URL)                                                                          |
| SocialNetworkURL    | string | The Social Network URL for the Location (must be a valid URL)                                                                  |
| VideoURL            | string | The Video URL for the Location (must be a valid URL)                                                                           |
