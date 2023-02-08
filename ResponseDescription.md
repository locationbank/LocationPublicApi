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
| DisplayPoint     | object | DisplayPointObject  
| BusinessStatus | string | 'The Status of the Location (Open, Closed, TemporarilyClosed)'                                                                 |
| Status         | string | Record status                                                                                                                  |
| BusinessName   | Object | BusinessNameObject   
| BusinessDescription | Object | BusinessDescriptionObject                                                                                                             |

<h2>**DisplayPointObject**</h2>
| Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                   
| Type             | enum   | - Calculated -  ManuallyPlaced                                                                       |
| Latitude         | number | '[TO BE REMOVED] Latitude of the Location represented by a high precision decimal number'            |
| Longitude        | number | '[TO BE REMOVED] Longitude of the Location represented by a high precision decimal number'           |
| VerificationType | enum   | - Client - Manually - DAC_PinIt - DAC_Goo


**BusinessNameObject**
| Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                   
| Name           | string | A standard length Business Name for the Location; This field is needed to submit data to Acxiom and Bing (max length 30 chars) |
| LongName       | string | A long Business Name for the Location (max length 80 chars)                                                                    |
| Locale         | string | Primary language 


**BusinessDescriptionObject**
| Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                   
| Description         | string | A description of the Business for the Location; This field is needed to submit data to Yalwa (max length 200 chars)                                  |
| ShortDescription    | string | A short description of the Business for the Location; This field is needed to submit data to Foursquare (max length 160 chars)                       |
| longDescription     | string | A long description of the Business for the Location; This field is needed to submit data to Superpages (min length 250 chars; max length 4000 chars) |
