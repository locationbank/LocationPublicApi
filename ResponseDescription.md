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


| Type             | enum   | - Calculated -  ManuallyPlaced                                                                       |
| Latitude         | number | '[TO BE REMOVED] Latitude of the Location represented by a high precision decimal number'            |
| Longitude        | number | '[TO BE REMOVED] Longitude of the Location represented by a high precision decimal number'           |
| VerificationType | enum   | - Client
            - Manually
            - DAC_PinIt
            - DAC_Goo
