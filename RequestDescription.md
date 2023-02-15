<h2>Location Bank Public API </h2>
   <h3> Represents a brief location model. Used to return an essensial data when a list of locations is requested </h3>


| Fields         | Type   | Description    | Location Bank Name                                                                                          |
|----------------|--------|----------------|-----------------------------------------------------------------------------------------|
| AccountID      | GUID  | **Required**  <br /> <br /> The unique identifier for the Account             | ClientId                                                       |
| LocationID     | GUID  | The unique identifier for the Location (auto-generated)         |Id                                         |
| LocationNumber | string |**Required** <br /> <br /> A friendly number used internally to reference the specified Location <br /> "A unique ID that you assign to each of your locations to ensure that changes are applied accurately in your account. This value will not be publicly visible anywhere.Generally provided by the client."  | StoreCode               |
| ReferenceCode  | string | An identifier for the Location specified by the user of the API     | PublicAPIReferenceCode                                     |
| CreatedBy      | string | String indicating who or what created the Location                                                       |
| ModifiedBy     | string | String indicating who or what last modified the Location                                                 |
| Created        | string | 'Time, location was created'                                                                             |
| Modified       | string | Time location was modified                                                                               |
| KeyFields      | object |**Required**<br /><br /> Dynamic storage of the key fields for the location or custom data which is used by specific applications.Keywords must be specific to what the business does<br /> e.g. Chicken Restaurant ; Burger Restaurant NOT Menu, Food |
| DisplayPoint     | Object | [DisplayPointObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#displaypointobject) |  
| BusinessStatus | enum |**Required**<br /><br /> [The Status of the Business](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#businessstatus)   | GmbOpenInfoStatus                                                              |
| Status         | enum | [Record status](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#Recordstatus)                                                                                                                  |
| BusinessName   | Object |**Required** <br /><br /> [BusinessNameObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#businessnameobject-) |  
| BusinessDescription | Object | [BusinessDescriptionObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#businessdescriptionobject-)  |
| PrimaryAddress | Object |**Required**<br /><br /> [AddressObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#addressobject-)  |
| phoneNumbers        | Object | [PhoneNumbersObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#phonenumbersobject-)  |
| WebsiteURL          | string |**Required**<br /><br /> The Website for the Location; Must be a valid URL with only sub, main, and top-level domain information (max length 40 char).Business Website |  WebsiteUrl  |
| mediaURLs           | Object | [MediaURLsObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#mediaurlsobject--)      | 
| HoursOfOperationStructured | Object  |**Required**<br /> [HoursOfOperationObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#hoursofoperationobject--) |RegularHours                                                       |
| businessCategories | Object |**Required**<br /> [BusinessCategoriesObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#businesscategoriesobject--)                                                                                                     
| Chain              | string | The name of the franchise or chain the Location belongs to                                                                   |
| Amenities          | string | A comma separated list of Amenities available at the Location <br /> (e.g.Parking, Free Parking, Parking Garage, Wheelchair Access) |
| PaymentMethods     | string | A comma separated list of Payment Methods for the Location                                                                   |
| PrimaryContact     | Object | [ContactPersonObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#contactpersonobject--)                                                                                                          |
| EmailAddress       | string | The primary email address for the Location; Must be a valid email address (max length 60 chars)                              |
| PhotoURLs                 | Array  | [PhotoObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#photourlobject--)                                                                                                           |                                          
| KeywordsSpecialties       | string | A comma separated list of Keywords and/or Specialties used by data providers to refine search listing relevancy for the Location.<br /><br />Keywords must be specific to what the business does <br />e.g. Chicken Restaurant ; Burger Restaurant NOT Menu, Food    | KeyWords                              |
| CredentialsCertifications | string | A comma separated list of Credentials and/or Certifications used by data providers to refine search listing relevancy for the Location (max length 200 chars)     |
| Products                  | string | A comma separated list of Products available at the Location which are used by data providers to refine search listing relevancy for the Location    | Products             |
| Services                  | string |  comma separated list of Services available at the Location which are used by data providers to refine search listing relevancy for the Location                  |
| Brands                    | string |**Required** <br /><br /> A comma separated list of Brands available at the Location which are used by data providers to refine search listing relevancy for the Location                  |
| YearFounded               | string | The year the Location was founded (must be four digits; e.g. 1992) | Founded                                                                                               |
| ProfessionalAssociations  | string | A comma separated list of Professional Associations relevant to the Location which are used by data providers to refine search listing relevancy for the Location |
| Tagline                   | string | A Tagline or slogan for the Location.                                                                                                                             |
| NumberEmployees           | string | The number of employees at the Location (max length 5 chars)                                                                                                      |
| AreasServed               | string | A comma separated list of Areas served by the Location (e.g. Downtown, Uptown, etc.)                                                                              |
| Languages                 | string | A comma separated list of Languages spoken at the Location (see documentation for list of valid Languages and input format)                                       |
| AlternateOrCorporateName  | string | ''                                                                                                                                                                |

<h2>DisplayPointObject</h2>

| Fields         | Type   | Description          | Location Bank Name                                                                                    |
|----------------|--------|----------------------|-----------------------------------------------------------------------------------|                                   
| Type             | enum   | - [DisplayPointType](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#displaypointtype)                                                                   |
| Latitude         | number |**Required** <br /><br /> 'Latitude of the Location represented by a high precision decimal number' <br /> Latitude  coordinate system by means of which the position or location of any place on Earth's surface can be determined and described    |Latitude      |
| Longitude        | number | **Required**<br /><br />  'Longitude of the Location represented by a high precision decimal number' <br />  longitude coordinate system by means of which the position or location of any place on Earth's surface can be determined and described     |Longitude    |
| VerificationType | enum   | -[VerificationType](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#verificationtype)   




<h2>Recordstatus</h2>

| Enum         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                   
| Active     | string   | Record status                                                                   |
| VerificationPending     | string   | Record status                                                                 |
| Deleted     | string   | Record status                                                                   |
| InActive     | string   | Record status                                                         


<h2>BusinessStatus</h2>

| Enum         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                   
| Open     | string   | The Status of the Location                                                                    |
| Closed     | string   | The Status of the Location                                                                  |
| TemporarilyClosed     | string   | The Status of the Location                                                                      |
| Duplicate     | string   | The Status of the Location                                                             


<h2>DisplayPointType</h2>

| Enum         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                   
| Calculated     | string   | The method used to determing the geocode for the Location ("Calculated": the typical method)                                                                       |
| ManuallyPlaced         | string | The method used to determing the geocode for the Location ("ManuallyPlaced": confirmed visually)            

<h2>VerificationType</h2>

| Enum         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                   
| Client     | string   | Display point verification type                                                                      |
| Manually         | string | Display point verification type       |    
| DAC_PinIt     | string   | Display point verification type                                                                 |
| DAC_Google     | string   |Display point verification type                                                                      |
| Other     | string   | Display point verification type                                                                       


<h2>BusinessNameObject </h2>

| Fields         | Type   | Description                | Location Bank Name                                                                              |
|----------------|--------|----------------------------|-----------------------------------------------------------------------------|                                   
| Name           | string |**Required** <br /><br /> A standard length Business Name for the Location. This field is needed to submit data to Acxiom and Bing (max length 30 chars)."A business name is required for each location.<br /><br />The name of your business that will appear on your listing. Represent your business exactly as it appears in the offline world. Your business name must be no longer than 80 characters." . | LocationName|
| LongName       | string | A long Business Name for the Location (max length 80 chars).                                                                    |
| Locale         | Enum | [Primary language](https://github.com/locationbank/LocationPublicApi/blob/main/BusinessNameLocale.md) 


  <h2>BusinessDescriptionObject </h2>
  
| Fields         | Type   | Description           | Location Bank Name                                                                                   |
|----------------|--------|-----------------------|-----------------------------------------------------------------------------------|                                   
| Description         | string |**Required** <br /><br /> A description of the Business for the Location       |Description                          |
| ShortDescription    | string |**Required**<br /><br />  A short description of the Business for the Location; This field is needed to submit data to Foursquare (max length 160 chars).<br /> "Enter a short description (max 160. characters) of the location or comapnay.Content: The description could be about your company history uniquness and products or services so that customers can get to know you better.<br /><br /> Do not input any contact data like Email, Phone or Website."                     |ShortDescription  |
| longDescription     | string | A long description of the Business for the Location; This field is needed to submit data to Superpages (min length 250 chars; max length 4000 chars).<br /><br />This field is needed to submit data to Yalwa (max length 200 chars).<br /><br />"Enter a Long description (max 750. characters) of the location or comapnay.Content: The description could be about your company history uniquness and products or services so that customers can get to know you better. <br /><br />Do not input any contact data like Email, Phone or Website."   |

<h2>AddressObject </h2>
  
| Fields         | Type   | Description      | Location Bank Name                                                                                        |
|----------------|--------|------------------|---------------------------------------------------------------------------------------|                                   
| AddressVisibility   | enum | [AddressVisibility](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#addressvisibility-)                                                                                                                                       |
| AddressLine1   | string |**Required** <br /><br /> First line of an address (max length 80 chars).      | AddressLine1                                                                                                                                     |
| AddressLine2   | string | econd line of an address (max length 80 chars).          | AddressLine2                                                                                                                                 |
| AddressLine3   | string | Third line of an address (max length 80 chars)                | AddressLine3                                                                                                                            |
| AddressLine4   | string | Fourth line of an address (max length 80 chars)        | AddressLine4                                                                                                                                    |
| AddressLine5   | string | Fifth line of an address (max length 80 chars)       |  | AddressLine5                                                                                                                                     |
| Neighborhood   | string |  Neighborhood represents an official sub-locality - typically an area within a town or city (max length 200 chars)  | SubLocality                                                                      |
| Locality       | string | **Required** <br /><br /> Locality generally represents a City or Town (max length 28 chars)        | Locality                                                                                                               |
| Region         | string | 'A Region represents the State or Province; depending on the specified CountryCode, this field may be required and the input format validated' |  AdministrativeArea |
| PostalCode     | string | **Required** <br /><br />  Postal Code or Zip Code; depending on the specified CountryCode, this field may be required and the input format validated (see documentation for validation details)' | PostalCode                 |
| CountryCode    | string | **Required** <br /><br />   'Two letter ISO 3166-1 alpha-2 country code representing the Country of a Location <br /> (e.g. US, CA, FR, DE, etc.)       | Country                                                                     |

                                 

  <h2>AddressVisibility </h2>

| Enum         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                                                                            
| LOCATION                  | string  |       Location Address: A business that serves customers only at their business address.               |
| LOCATION_SERVICE          | string  |     Location Address & Service Area:A business that serves customers at their business address, but also directly visits or delivers to customers. If your business doesn’t have permanent on-site signage, it's not eligible as a storefront and should be listed as a service-area business.For example, a dine-in restaurant that also delivers food.  |      
| SERVICE                    | string  | Service Area Only:Service-area business: A business that visits or delivers to customers directly, but doesn’t serve customers at their business address. <br/>For example, businesses like cleaning services or plumbers. <br/>Service-area businesses can only create one profile for the metropolitan area that they serve.                                            


  <h2>PhoneNumbersObject </h2>
  
  | Fields         | Type   | Description  | Location Bank Name                                                                                            |
|----------------|--------|----------------|-----------------------------------------------------------------------------------------|    
|  PrimaryPhoneNumber | string |**Required** <br /><br /> The Primary Phone Number for the Location. "The best number for customers to use to reach your business. <br /><br /> This phone number may be for a mobile device or landline (no fax numbers). Provide a phone number that connects to your location as directly as possible."          | PrimaryPhone                                                                            |
| Landline            | string | The Landline Phone Number for the Location | AdditionalPhone1                                                                                    |
| Mobile              | string | The Mobile Phone Number for the Location     | AdditionalPhone2                                                                                  |
| Fax                 | string | The Fax Number for the Location        | AdditionalPhone3                                                                                        |
| TollFree            | string | The Toll-Free Phone Number for the Location       | AdditionalPhone4                                                                             |


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



  <h2>HoursOfOperationObject  </h2>
  
 | Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|    
| HoursOfOperationObject     | string  | [Su](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#day-) <br /><br /> These are the trading hours of the business                                                                           |
| HoursOfOperationObject     | string  | [Mo](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#day-) <br /><br />   These are the trading hours of the business                                                                          |
| HoursOfOperationObject     | string  | [Tu](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#day-)  <br /><br /> These are the trading hours of the business                                                                          |
| HoursOfOperationObject     | string  | [We](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#day-) <br /><br /> These are the trading hours of the business                                                                           |
| HoursOfOperationObject     | string  | [Th](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#day-) <br /> <br />These are the trading hours of the business                                                                           |
| HoursOfOperationObject     | string  | [Fr](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#day-) <br /><br /> These are the trading hours of the business                                                                           |
| HoursOfOperationObject     | string  | [Sa](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#day-) <br /><br /> These are the trading hours of the business                                                                           |


  <h2>Day </h2>
  
 | Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                                                                             
| Ranges                     | Array   | [TimeRange](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#day-)             |
| state                      | Enum  | [State](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#state--)   |
| additionalInfo             | string  | Any additional comments - open by appointment, short hours during holidays etc                        |
|                            |         |        


  <h2>TimeRange  </h2>
  
 | Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                                                                            
| StartTime                  | string  | Start time                                                                                            |
| EndTime                    | string  | End time                                                                                              |      


  <h2>state  </h2>
  
 | Enum         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                                                                            
| Open                  | string  | Represent open/close state on the specific date  [Open=0]                                                       |
| Closed                    | string  | Represent open/close state on the specific date  [Closed=1]                                                |      
| Open24Hrs                    | string  | Represent open/close state on the specific date  [Open24Hrs=2]                                           |     
| OpenByAppointment                    | string  | Represent open/close state on the specific date OpenByAppointment=3                                                                                               


 <h2>BusinessCategoriesObject  </h2>
  
 | Fields         | Type   | Description   | Location Bank Name                                                                                          |
|----------------|--------|----------------|-----------------------------------------------------------------------------------------|                                                                                            
| Category1          | string |**Required** <br /><br />  Business Category 1 You can select 1 primary category (the most weight in the Google algorithm) and 9 secondary categories for your Google My Business listing. | GmbPrimaryCategoryName                                                                                   |
| Category2          | string | Business Category 2   |  GmbAdditionalCategoryName1                                                                                                       |
| Category3          | string | Business Category 3  |  GmbAdditionalCategoryName2                                                                                                        |
| Category4          | string | Business Category 4     | GmbAdditionalCategoryName3                                                                                                     |
| Category5          | string | Business Category 5       | GmbAdditionalCategoryName4                                                                                                   |
| Category6          | string | Business Category 6     | GmbAdditionalCategoryName5                                                                                                     |
| Category7          | string | Business Category 7     |  GmbAdditionalCategoryName6                                                                                                     |
| Category8          | string | Business Category 8      | GmbAdditionalCategoryName7                                                                                                    |
| Category9          | string | Business Category 9      | GmbAdditionalCategoryName8                                                                                                    |


 <h2>ContactPersonObject  </h2>
  
 | Fields         | Type   | Description  | Location Bank  Name                                                                                             |
|----------------|--------|---------------|------------------------------------------------------------------------------------------|                                                                                            
| FullName     | string | The full name of the Contact Person                                                           |
| FirstName    | string | The First Name of the Contact Person (max length 15 chars)                                    |
| MiddleName   | string | The Middle Name of the Contact Person                                                         |
| LastName     | string | The Last Name of the Contact Person (max length 20 chars)                                     |
| Title        | string | Title (e.g. Regional Sales Manager, Customer Support Technician, etc.) (max length 256 chars) |
| EmailAddress | string | Contact Email address (must be a valid email address) | Email                                         |


 <h2>PhotoURLObject  </h2>
  
 | Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                                                                            
| Type                      | Enum | [Type of photo](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#phototype--)                        |
| URL                       | string | The URL for the Photo                                                                                                                                             |
| Name                      | string | The name of the Photo                                                                                                                                             |
| Description               | string | A description of the Photo  |



 <h2>PhotoType  </h2>
  
 | Enum         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                                                                            
| ProfilePhoto                      | string | "ProfilePhoto": often displayed as a series                                |
| CoverPhoto                       | string | "CoverPhoto": usually only 1                                                 |
| Logo                      | string | usually only 1                                                                      |
| Other               | string | ''  |


