# LocationPublicApi
Sections

1.Base API Url

2.List of All Locations

3.Create location

4.Single Location

5.Update location

<h1>1.Base API Url</h1>

All endpoints described in this document with the exception of Reporting have the following base API url: https://api.places.digital/locations-api-write/

<h1>2.List of All Locations</h1>

Http Verb: GET.

Headers: Content-Type: application/json

         Ocp-Apim-Subscription-Key : (Format - string. Passed into header for Authorization)

Http EndPoint: /locations

<strong>QueryString Parameters:</strong>

```{questions}
- AccountID: (Format - uuid. The unique identifier for the Account)
- CreatedDateFrom: Format - date-time (as date-time in RFC3339). Optional filter: Start DateTime to apply filter by date range on the field ''Created''. Expected format is yyyy-MM-dd HH:mm:ss
- CreatedDateTo: 'Format - date-time (as date-time in RFC3339). Optional filter: End DateTime to apply filter by date range on the field ''Created''. Expected format is yyyy-MM-dd HH:mm:ss'
- ModifiedDateFrom: 'Format - date-time (as date-time in RFC3339). Optional filter: Start DateTime to apply filter by date range on the field ''Modified''. Expected format is yyyy-MM-dd HH:mm:ss'
- ModifiedDateTo: 'Format - date-time (as date-time in RFC3339). Optional filter: End DateTime to apply filter by date range on the field ''Modified''. Expected format is yyyy-MM-dd HH:mm:ss'
- PageSize: 'Format - int32. The number of Locations listed on each page of returned data (max value: )'
- ContinuationToken: 'Format - string. Continue your request and get the next page of results by passing in the token from the previous result.'
- statuses : 'Format - string. 'Default is null - returns active locations. Ex: "active,closed"; "0,1"''
```


<strong>Response Json Body</strong>

```{questions}
[{
  "AccountID": "00000000-0000-0000-0000-000000000000",
  "LocationID": "00000000-0000-0000-0000-000000000000",
  "LocationNumber": "string",
  "ReferenceCode": "string",
  "CreatedBy": "string",
  "ModifiedBy": "string",
  "Created": "string",
  "Modified": "string",
  "LocationData": {
    "KeyFields": {},
    "DisplayPoint": {
      "Type": "Calculated",
      "Latitude": 0.0,
      "Longitude": 0.0,
      "VerificationType": "Client"
    },
    "BusinessStatus": "Open",
    "Status": "Active",
    "BusinessName": {
      "Name": "string",
      "LongName": "string",
      "Locale": "Not_set"
    },
    "BusinessDescription": {
      "Description": "string",
      "ShortDescription": "string",
      "LongDescription": "string"
    },
    "PrimaryAddress": {
      "AddressLine1": "string",
      "AddressLine2": "string",
      "AddressLine3": "string",
      "AddressLine4": "string",
      "AddressLine5": "string",
      "Neighborhood": "string",
      "Locality": "string",
      "Region": "string",
      "PostalCode": "string",
      "CountryCode": "string"
    },
    "PhoneNumbers": {
      "PrimaryPhoneNumber": "string",
      "Landline": "string",
      "Mobile": "string",
      "Fax": "string",
      "TollFree": "string"
    },
    "WebsiteURL": "string",
    "AlternateWebsiteURL": "string",
    "MediaURLs": {
      "FacebookURL": "string",
      "TwitterURL": "string",
      "LinkedInURL": "string",
      "InstagramURL": "string",
      "PinterestURL": "string",
      "CouponURL": "string",
      "SocialNetworkURL": "string",
      "VideoURL": "string"
    },
    "HoursOfOperation": "string",
    "HoursOfOperationStructured": {
      "SpecialHours": [
        {
          "Date": "string",
          "Ranges": [
            {
              "StartTime": "string",
              "EndTime": "string"
            }
          ],
          "State": "Open",
          "AdditionalInfo": "string"
        }
      ],
      "Su": {
        "Ranges": [
          {
            "StartTime": "string",
            "EndTime": "string"
          }
        ],
        "State": "Open",
        "AdditionalInfo": "string"
      },
      "Mo": {
        "Ranges": [
          {
            "StartTime": "string",
            "EndTime": "string"
          }
        ],
        "State": "Open",
        "AdditionalInfo": "string"
      },
      "Tu": {
        "Ranges": [
          {
            "StartTime": "string",
            "EndTime": "string"
          }
        ],
        "State": "Open",
        "AdditionalInfo": "string"
      },
      "We": {
        "Ranges": [
          {
            "StartTime": "string",
            "EndTime": "string"
          }
        ],
        "State": "Open",
        "AdditionalInfo": "string"
      },
      "Th": {
        "Ranges": [
          {
            "StartTime": "string",
            "EndTime": "string"
          }
        ],
        "State": "Open",
        "AdditionalInfo": "string"
      },
      "Fr": {
        "Ranges": [
          {
            "StartTime": "string",
            "EndTime": "string"
          }
        ],
        "State": "Open",
        "AdditionalInfo": "string"
      },
      "Sa": {
        "Ranges": [
          {
            "StartTime": "string",
            "EndTime": "string"
          }
        ],
        "State": "Open",
        "AdditionalInfo": "string"
      }
    },
    "BusinessCategories": {
      "Category1": "string",
      "Category2": "string",
      "Category3": "string",
      "Category4": "string",
      "Category5": "string",
      "Category6": "string",
      "Category7": "string",
      "Category8": "string",
      "Category9": "string",
      "Category10": "string"
    },
    "Chain": "string",
    "Amenities": "string",
    "PaymentMethods": "string",
    "PrimaryContact": {
      "FullName": "string",
      "FirstName": "string",
      "MiddleName": "string",
      "LastName": "string",
      "Title": "string",
      "EmailAddress": "string"
    },
    "EmailAddress": "string",
    "PhotoURLs": [
      {
        "Type": "ProfilePhoto",
        "URL": "string",
        "Name": "string",
        "Description": "string"
      }
    ],
    "KeywordsSpecialties": "string",
    "CredentialsCertifications": "string",
    "Products": "string",
    "Services": "string",
    "Brands": "string",
    "YearFounded": "string",
    "ProfessionalAssociations": "string",
    "Tagline": "string",
    "NumberEmployees": "string",
    "AreasServed": "string",
    "Languages": "string",
    "AlternateOrCorporateName": "string"
  },
  "UserData": {}
}]
```

<strong>Response Desciption:</strong>


```{questions}
AccountID:
          type: string
          description: The unique identifier for the Account
          format: uuid
          example: 00000000-0000-0000-0000-000000000000
LocationID:
          type: string
          description: The unique identifier for the Location (auto-generated)
          format: uuid
          example: 00000000-0000-0000-0000-000000000000
LocationNumber:
          type: string
          description: A friendly number used internally to reference the specified Location (for support purposes)
ReferenceCode:
          type: string
          description: An identifier for the Location specified by the user of the APCreatedBy:
          type: string
          description: String indicating who or what created the Locati
ModifiedBy:
          type: string
          description: String indicating who or what last modified the Location
Created:
          type: string
          description: 'Time, location was created'
          format: date-time
 Modified:
          type: string
          description: Time location was modified
          format: date-time
KeyFields:
          type: object
          additionalProperties:
            type: string
          description: Dynamic storage of the key fields for the location or custom data which is used by specific applications
DisplayPoint:
      type: object
      properties:
        Type:
          enum:
            - Calculated
            - ManuallyPlaced
          type: string
          description: 'The method used to determing the geocode for the Location ("ManuallyPlaced": confirmed visually, "Calculated": the typical method)'
        Latitude:
          type: number
          description: '[TO BE REMOVED] Latitude of the Location represented by a high precision decimal number'
          format: double
        Longitude:
          type: number
          description: '[TO BE REMOVED] Longitude of the Location represented by a high precision decimal number'
          format: double
        VerificationType:
          enum:
            - Client
            - Manually
            - DAC_PinIt
            - DAC_Google
            - Other
          type: string
          description: Display point verification type
      description: '[TO BE REMOVED] Structured object containing the geocode of the Location in Latitude and Longitude as a decimal and supplementary information             describing the quality of the geocode'

BusinessStatus:
          enum:
            - Open
            - Closed
            - TemporarilyClosed
            - Duplicate
          type: string
          description: 'The Status of the Location (Open, Closed, TemporarilyClosed)'
Status:
          enum:
            - Active
            - VerificationPending
            - Deleted
            - InActive
          type: string
          description: Record status
```
