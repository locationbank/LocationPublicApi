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
[    
       
    {
        "accountID": "00000000-0000-0000-0000-000000000000",
        "locationID": "e2f30897-bd1b-40e2-b1b6-98e446dc8ced",
        "locationNumber": "test",
        "referenceCode": null,
        "createdBy": "LocationBankAPI",
        "modifiedBy": "LocationBankAPI",
        "created": null,
        "modified": null,
        "locationBankPublicLocationData": {
            "keyFields": {
                "pinMarker": "true",
                "referenceCode2": "test",
                "chainName": null,
                "primarylanguage": "en-"
            },
            "displayPoint": {
                "type": "Calculated",
                "latitude": -25.73134,
                "longitude": 28.21837,
                "verificationType": "Other"
            },
            "businessStatus": "Open",
            "status": "Active",
            "businessName": {
                "name": "test",
                "longName": "test"
            },
            "businessDescription": {
                "description": null,
                "shortDescription": null,
                "longDescription": null
            },
            "primaryAddress": {
                "addressLine1": "",
                "addressLine2": "",
                "addressLine3": "",
                "addressLine4": "",
                "addressLine5": "",
                "neighborhood": "",
                "locality": "",
                "region": "",
                "postalCode": "",
                "countryCode": ""
            },
            "phoneNumbers": {
                "primaryPhoneNumber": "",
                "landline": null,
                "mobile": null,
                "fax": null,
                "tollFree": null
            },
            "websiteURL": "",
            "alternateWebsiteURL": null,
            "mediaURLs": {
                "facebookUrl": "",
                "twitterUrl": "",
                "linkedInUrl": "",
                "instagramUrl": "",
                "pinterestUrl": "",
                "couponUrl": "",
                "socialNetworkUrl": "",
                "videoUrl": ""
            },
            "hoursOfOperation": null,
            "hoursOfOperationStructured": {
                "su": {
                    "ranges": [
                        {
                            "startTime": "08:00AM",
                            "endTime": "05:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "mo": {
                    "ranges": [
                        {
                            "startTime": "08:00AM",
                            "endTime": "05:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "tu": {
                    "ranges": [
                        {
                            "startTime": "08:00AM",
                            "endTime": "05:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "we": {
                    "ranges": [
                        {
                            "startTime": "08:00AM",
                            "endTime": "05:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "th": {
                    "ranges": [
                        {
                            "startTime": "08:00AM",
                            "endTime": "05:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "fr": {
                    "ranges": [
                        {
                            "startTime": "08:00AM",
                            "endTime": "05:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "sa": {
                    "ranges": [
                        {
                            "startTime": "08:00AM",
                            "endTime": "05:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "specialHours": []
            },
            "businessCategories": {
                "category1": "",
                "category2": "",
                "category3": "",
                "category4": "",
                "category5": "",
                "category6": "",
                "category7": "",
                "category8": "",
                "category9": "",
                "category10": ""
            },
            "chain": null,
            "amenities": "",
            "paymentMethods": "",
            "primaryContact": {
                "fullName": null,
                "firstName": null,
                "middleName": null,
                "lastName": null,
                "title": null,
                "emailAddress": null
            },
            "emailAddress": "",
            "photoURLs": [],
            "keywordsSpecialties": "",
            "credentialsCertifications": "",
            "products": "",
            "services": null,
            "brands": null,
            "yearFounded": "",
            "professionalAssociations": "",
            "tagline": null,
            "numberEmployees": "",
            "areasServed": null,
            "languages": "en",
            "alternateOrCorporateName": null
        },
        "userData": null
    },
    {
        "accountID": "00000000-0000-0000-0000-000000000000",
        "locationID": "fdbddbf7-e73e-4bbe-b9f6-b49f0675ebff",
        "locationNumber": "SC103",
        "referenceCode": null,
        "createdBy": "LocationBankAPI",
        "modifiedBy": "LocationBankAPI",
        "created": null,
        "modified": null,
        "locationBankPublicLocationData": {
            "keyFields": {
                "pinMarker": "true",
                "referenceCode2": "SC103",
                "chainName": "Brand Name - Location number 5",
                "primarylanguage": "en-ZA"
            },
            "displayPoint": {
                "type": "Calculated",
                "latitude": -33.7291942,
                "longitude": 18.4386631,
                "verificationType": "Other"
            },
            "businessStatus": "Open",
            "status": "Active",
            "businessName": {
                "name": "Location 5",
                "longName": "Brand Name Example Location 5"
            },
            "businessDescription": {
                "description": "",
                "shortDescription": "Test 20:17 2021/01/31",
                "longDescription": ""
            },
            "primaryAddress": {
                "addressLine1": "Cnr 6th Ave & Beach Rd",
                "addressLine2": "Shop 103",
                "addressLine3": "",
                "addressLine4": "",
                "addressLine5": "",
                "neighborhood": "Melkbosstrand",
                "locality": "Cape Town",
                "region": "Some place",
                "postalCode": "7441",
                "countryCode": "ZA"
            },
            "phoneNumbers": {
                "primaryPhoneNumber": "0107861031",
                "landline": null,
                "mobile": null,
                "fax": null,
                "tollFree": null
            },
            "websiteURL": "http://www.yowzit.com/",
            "alternateWebsiteURL": "http://www.yowzit.com/",
            "mediaURLs": {
                "facebookUrl": "",
                "twitterUrl": "",
                "linkedInUrl": "",
                "instagramUrl": "",
                "pinterestUrl": "",
                "couponUrl": "",
                "socialNetworkUrl": "",
                "videoUrl": ""
            },
            "hoursOfOperation": null,
            "hoursOfOperationStructured": {
                "su": {
                    "ranges": [
                        {
                            "startTime": "09:00AM",
                            "endTime": "01:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "mo": {
                    "ranges": [
                        {
                            "startTime": "09:00AM",
                            "endTime": "01:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "tu": {
                    "ranges": [
                        {
                            "startTime": "09:00AM",
                            "endTime": "01:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "we": {
                    "ranges": [
                        {
                            "startTime": "09:00AM",
                            "endTime": "01:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "th": {
                    "ranges": [
                        {
                            "startTime": "09:00AM",
                            "endTime": "01:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "fr": {
                    "ranges": [
                        {
                            "startTime": "09:00AM",
                            "endTime": "01:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "sa": {
                    "ranges": [
                        {
                            "startTime": "11:00AM",
                            "endTime": "06:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "specialHours": []
            },
            "businessCategories": {
                "category1": "Pool Cleaning Service",
                "category2": "Swimming Pool Supply Store",
                "category3": "Swimming",
                "category4": "Swimming Instructor",
                "category5": "",
                "category6": "",
                "category7": "",
                "category8": "",
                "category9": "",
                "category10": ""
            },
            "chain": null,
            "amenities": "",
            "paymentMethods": "",
            "primaryContact": {
                "fullName": null,
                "firstName": null,
                "middleName": null,
                "lastName": null,
                "title": null,
                "emailAddress": null
            },
            "emailAddress": "",
            "photoURLs": [],
            "keywordsSpecialties": "test",
            "credentialsCertifications": "",
            "products": "",
            "services": null,
            "brands": null,
            "yearFounded": "20190310",
            "professionalAssociations": "",
            "tagline": null,
            "numberEmployees": "",
            "areasServed": null,
            "languages": "en",
            "alternateOrCorporateName": null
        },
        "userData": null
    }
]
```

<strong>Response Description:</strong>


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
 BusinessName:
        BusinessNameObject:
      type: object
      properties:
        Name:
          type: string
          description: A standard length Business Name for the Location; This field is needed to submit data to Acxiom and Bing (max length 30 chars)
        LongName:
          type: string
          description: A long Business Name for the Location (max length 80 chars)
        Locale:
          enum:
            - Not_set
            - af_ZA
            - am_ET
            - ar_AE
            - ar_BH
            - ar_DZ
            - ar_EG
            - ar_IQ
            - ar_JO
            - ar_KW
            - ar_LB
            - ar_LY
            - ar_MA
            - arn_CL
            - ar_OM
            - ar_QA
            - ar_SA
            - ar_SY
            - ar_TN
            - ar_YE
            - as_IN
            - az_Cyrl_AZ
            - az_Latn_AZ
            - ba_RU
            - be_BY
            - bg_BG
            - bn_BD
            - bn_IN
            - bo_CN
            - br_FR
            - bs_Cyrl_BA
            - bs_Latn_BA
            - ca_ES
            - co_FR
            - cs_CZ
            - cy_GB
            - da_DK
            - de_AT
            - de_CH
            - de_DE
            - de_LI
            - de_LU
            - dsb_DE
            - dv_MV
            - el_GR
            - en_029
            - en_AU
            - en_BZ
            - en_CA
            - en_GB
            - en_IE
            - en_IN
            - en_JM
            - en_MY
            - en_NZ
            - en_PH
            - en_SG
            - en_TT
            - en_US
            - en_ZA
            - en_ZW
            - es_AR
            - es_BO
            - es_CL
            - es_CO
            - es_CR
            - es_DO
            - es_EC
            - es_ES
            - es_GT
            - es_HN
            - es_MX
            - es_NI
            - es_PA
            - es_PE
            - es_PR
            - es_PY
            - es_SV
            - es_US
            - es_UY
            - es_VE
            - et_EE
            - eu_ES
            - fa_IR
            - fi_FI
            - fil_PH
            - fo_FO
            - fr_BE
            - fr_CA
            - fr_CH
            - fr_FR
            - fr_LU
            - fr_MC
            - fy_NL
            - ga_IE
            - gd_GB
            - gl_ES
            - gsw_FR
            - gu_IN
            - ha_Latn_NG
            - he_IL
            - hi_IN
            - hr_BA
            - hr_HR
            - hsb_DE
            - hu_HU
            - hy_AM
            - id_ID
            - ig_NG
            - ii_CN
            - is_IS
            - it_CH
            - it_IT
            - iu_Cans_CA
            - iu_Latn_CA
            - ja_JP
            - ka_GE
            - kk_KZ
            - kl_GL
            - km_KH
            - kn_IN
            - kok_IN
            - ko_KR
            - ky_KG
            - lb_LU
            - lo_LA
            - lt_LT
            - lv_LV
            - mi_NZ
            - mk_MK
            - ml_IN
            - mn_MN
            - mn_Mong_CN
            - moh_CA
            - mr_IN
            - ms_BN
            - ms_MY
            - mt_MT
            - nb_NO
            - ne_NP
            - nl_BE
            - nl_NL
            - nn_NO
            - nso_ZA
            - oc_FR
            - or_IN
            - pa_IN
            - pl_PL
            - prs_AF
            - ps_AF
            - pt_BR
            - pt_PT
            - qut_GT
            - quz_BO
            - quz_EC
            - quz_PE
            - rm_CH
            - ro_RO
            - ru_RU
            - rw_RW
            - sah_RU
            - sa_IN
            - se_FI
            - se_NO
            - se_SE
            - si_LK
            - sk_SK
            - sl_SI
            - sma_NO
            - sma_SE
            - smj_NO
            - smj_SE
            - smn_FI
            - sms_FI
            - sq_AL
            - sr_Cyrl_BA
            - sr_Cyrl_CS
            - sr_Cyrl_ME
            - sr_Cyrl_RS
            - sr_Latn_BA
            - sr_Latn_CS
            - sr_Latn_ME
            - sr_Latn_RS
            - sv_FI
            - sv_SE
            - sw_KE
            - syr_SY
            - ta_IN
            - te_IN
            - tg_Cyrl_TJ
            - th_TH
            - tk_TM
            - tn_ZA
            - tr_TR
            - tt_RU
            - tzm_Latn_DZ
            - ug_CN
            - uk_UA
            - ur_PK
            - uz_Cyrl_UZ
            - uz_Latn_UZ
            - vi_VN
            - wo_SN
            - xh_ZA
            - yo_NG
            - zh_CN
            - zh_HK
            - zh_MO
            - zh_SG
            - zh_TW
            - zu_ZA
          type: string
          description: Primary language
      description: Structured object containing different length Business Names for the Location to enable data submission to different services
BusinessDescription
                  type: object
      properties:
        Description:
          type: string
          description: A description of the Business for the Location; This field is needed to submit data to Yalwa (max length 200 chars)
        ShortDescription:
          type: string
          description: A short description of the Business for the Location; This field is needed to submit data to Foursquare (max length 160 chars)
        LongDescription:
          type: string
          description: A long description of the Business for the Location; This field is needed to submit data to Superpages (min length 250 chars; max length 4000 chars)
      description: Structured object containing different length descriptions of the Business for the Location to enable data submission to different services
PhoneNumbers:
         PhoneNumbersObject:
      type: object
      properties:
        PrimaryPhoneNumber:
          type: string
          description: The Primary Phone Number for the Location (see documentation for input format) (Infogroup does not allow toll-free numbers; Location data can only be submitted to Infogroup when the PrimaryPhoneNumber is a local number)
        Landline:
          type: string
          description: The Landline Phone Number for the Location (if different from Primary number) (see documentation for input format)
        Mobile:
          type: string
          description: The Mobile Phone Number for the Location (if different from Primary number) (see documentation for input format)
        Fax:
          type: string
          description: The Fax Number for the Location (see documentation for input format)
        TollFree:
          type: string
          description: The Toll-Free Phone Number for the Location (see documentation for input format)
      description: The list of Phone Numbers for the Location (see documentation for input format)
      
         WebsiteURL:
          type: string
          description: 'The Website for the Location; Must be a valid URL with only sub, main, and top-level domain information (max length 40 char)'
        AlternateWebsiteURL:
          type: string
          description: An Alternate Website for the Location; potentially a corporate website for the location (no max length)
        MediaURLs:
                   MediaURLsObject:
                              MediaURLsObject:
                                 type: object
                                 properties:
                                   FacebookURL:
                                     type: string
                                     description: The Facebook URL for the Location (must be a valid URL)
                                   TwitterURL:
                                     type: string
                                     description: The Twitter URL for the Location (must be a valid URL)
                                   LinkedInURL:
                                     type: string
                                     description: The LinkedIn URL for the Location (must be a valid URL)
                                   InstagramURL:
                                     type: string
                                     description: The Instagram URL for the Location (must be a valid URL)
                                   PinterestURL:
                                     type: string
                                     description: The Pinterest URL for the Location (must be a valid URL)
                                   CouponURL:
                                     type: string
                                     description: The Coupon URL for the Location (must be a valid URL)
                                   SocialNetworkURL:
                                     type: string
                                     description: The Social Network URL for the Location (must be a valid URL)
                                   VideoURL:
                                     type: string
                                     description: The Video URL for the Location (must be a valid URL)
                                 description: The list of Social Media URLs for the Location                 
          
 HoursOfOperation:
          type: string
          description: String representation of Hours of Operation structured object for the Location
          readOnly: true
          
  HoursOfOperationStructured:
     HoursOfOperationObject:
            type: object
               properties:
                     SpecialHours:
                       type: array
                      items:
                      HoursOfOperationItemEx:
                             required:
                                 - Date
                                       type: object
                                          properties:
                                            Date:
                                              type: string
                                              description: Optional. Set the specific date
                                            Ranges:
                                              type: array
                                              items:
                                               TimeRange:
                                                   type: object
                                                   properties:
                                                     StartTime:
                                                       type: string
                                                       description: Start time
                                                     EndTime:
                                                       type: string
                                                       description: End time
                                                   description: 'Time period, less than 24 hours'
                                                      description: A list of time periods
                          State:
                            enum:
                              - Open
                              - Closed
                              - Open24Hrs
                              - OpenByAppointment
                            type: string
                            description: " Represent open/close state on the specific date.\r\n[Open=0|Closed=1|Open24Hrs=2|OpenByAppointment=3]"
                          AdditionalInfo:
                            type: string
                            description: 'Any additional comments - open by appointment, short hours during holidays etc.'
                        description: Hours of Operations information for a single day.
                                     description: Identify hours of operation on special dates   
                                   Su:
                                     HoursOfOperationItem:
                                          type: object
                                          properties:
                                            Ranges:
                                              type: array
                                              items:
                                              TimeRange:
                                                 type: object
                                                  properties:
                                                    StartTime:
                                                      type: string
                                                      description: Start time
                                                    EndTime:
                                                      type: string
                                                      description: End time
                                                 description: 'Time period, less than 24 hours'
                                              description: A list of time periods
                                            State:
                                              enum:
                                                - Open
                                                - Closed
                                                - Open24Hrs
                                                - OpenByAppointment
                                              type: string
                                              description: " Represent open/close state on the specific date.\r\n[Open=0|Closed=1|Open24Hrs=2|OpenByAppointment=3]"
                                            AdditionalInfo:
                                              type: string
                                              description: 'Any additional comments - open by appointment, short hours during holidays etc.'
                                          description: Hours of operation
                                   Mo:
                                        HoursOfOperationItem:
                                          type: object
                                          properties:
                                            Ranges:
                                              type: array
                                              items:
                                              TimeRange:
                                                 type: object
                                                  properties:
                                                    StartTime:
                                                      type: string
                                                      description: Start time
                                                    EndTime:
                                                      type: string
                                                      description: End time
                                                 description: 'Time period, less than 24 hours'
                                              description: A list of time periods
                                            State:
                                              enum:
                                                - Open
                                                - Closed
                                                - Open24Hrs
                                                - OpenByAppointment
                                              type: string
                                              description: " Represent open/close state on the specific date.\r\n[Open=0|Closed=1|Open24Hrs=2|OpenByAppointment=3]"
                                            AdditionalInfo:
                                              type: string
                                              description: 'Any additional comments - open by appointment, short hours during holidays etc.'
                                          description: Hours of operation
                                   Tu:
                                         HoursOfOperationItem:
                                          type: object
                                          properties:
                                            Ranges:
                                              type: array
                                              items:
                                              TimeRange:
                                                 type: object
                                                  properties:
                                                    StartTime:
                                                      type: string
                                                      description: Start time
                                                    EndTime:
                                                      type: string
                                                      description: End time
                                                 description: 'Time period, less than 24 hours'
                                              description: A list of time periods
                                            State:
                                              enum:
                                                - Open
                                                - Closed
                                                - Open24Hrs
                                                - OpenByAppointment
                                              type: string
                                              description: " Represent open/close state on the specific date.\r\n[Open=0|Closed=1|Open24Hrs=2|OpenByAppointment=3]"
                                            AdditionalInfo:
                                              type: string
                                              description: 'Any additional comments - open by appointment, short hours during holidays etc.'
                                          description: Hours of operation
                                   We:
                                      HoursOfOperationItem:
                                          type: object
                                          properties:
                                            Ranges:
                                              type: array
                                              items:
                                              TimeRange:
                                                 type: object
                                                  properties:
                                                    StartTime:
                                                      type: string
                                                      description: Start time
                                                    EndTime:
                                                      type: string
                                                      description: End time
                                                 description: 'Time period, less than 24 hours'
                                              description: A list of time periods
                                            State:
                                              enum:
                                                - Open
                                                - Closed
                                                - Open24Hrs
                                                - OpenByAppointment
                                              type: string
                                              description: " Represent open/close state on the specific date.\r\n[Open=0|Closed=1|Open24Hrs=2|OpenByAppointment=3]"
                                            AdditionalInfo:
                                              type: string
                                              description: 'Any additional comments - open by appointment, short hours during holidays etc.'
                                          description: Hours of operation
                                   Th:
                                       HoursOfOperationItem:
                                          type: object
                                          properties:
                                            Ranges:
                                              type: array
                                              items:
                                              TimeRange:
                                                 type: object
                                                  properties:
                                                    StartTime:
                                                      type: string
                                                      description: Start time
                                                    EndTime:
                                                      type: string
                                                      description: End time
                                                 description: 'Time period, less than 24 hours'
                                              description: A list of time periods
                                            State:
                                              enum:
                                                - Open
                                                - Closed
                                                - Open24Hrs
                                                - OpenByAppointment
                                              type: string
                                              description: " Represent open/close state on the specific date.\r\n[Open=0|Closed=1|Open24Hrs=2|OpenByAppointment=3]"
                                            AdditionalInfo:
                                              type: string
                                              description: 'Any additional comments - open by appointment, short hours during holidays etc.'
                                          description: Hours of operation
                                   Fr:
                                       HoursOfOperationItem:
                                          type: object
                                          properties:
                                            Ranges:
                                              type: array
                                              items:
                                              TimeRange:
                                                 type: object
                                                  properties:
                                                    StartTime:
                                                      type: string
                                                      description: Start time
                                                    EndTime:
                                                      type: string
                                                      description: End time
                                                 description: 'Time period, less than 24 hours'
                                              description: A list of time periods
                                            State:
                                              enum:
                                                - Open
                                                - Closed
                                                - Open24Hrs
                                                - OpenByAppointment
                                              type: string
                                              description: " Represent open/close state on the specific date.\r\n[Open=0|Closed=1|Open24Hrs=2|OpenByAppointment=3]"
                                            AdditionalInfo:
                                              type: string
                                              description: 'Any additional comments - open by appointment, short hours during holidays etc.'
                                          description: Hours of operation
                                   Sa:
                                       HoursOfOperationItem:
                                          type: object
                                          properties:
                                            Ranges:
                                              type: array
                                              items:
                                              TimeRange:
                                                 type: object
                                                  properties:
                                                    StartTime:
                                                      type: string
                                                      description: Start time
                                                    EndTime:
                                                      type: string
                                                      description: End time
                                                 description: 'Time period, less than 24 hours'
                                              description: A list of time periods
                                            State:
                                              enum:
                                                - Open
                                                - Closed
                                                - Open24Hrs
                                                - OpenByAppointment
                                              type: string
                                              description: " Represent open/close state on the specific date.\r\n[Open=0|Closed=1|Open24Hrs=2|OpenByAppointment=3]"
                                            AdditionalInfo:
                                              type: string
                                              description: 'Any additional comments - open by appointment, short hours during holidays etc.'
                                          description: Hours of operation                  

 SpecialHours:
          type: array
          items:
            HoursOfOperationItemEx:
                      required:
                          - Date
                      type: object
                      properties:
                       Date:
                          type: string
                          description: Optional. Set the specific date
                              Ranges:
                                 type: array
                                 items:
                                       TimeRange:
                                          type: object
                                          properties:
                                            StartTime:
                                              type: string
                                              description: Start time
                                            EndTime:
                                              type: string
                                              description: End time
                                          description: 'Time period, less than 24 hours'
                                     description: A list of time periods
                                   State:
                                     enum:
                                       - Open
                                       - Closed
                                       - Open24Hrs
                                       - OpenByAppointment
                                     type: string
                                     description: " Represent open/close state on the specific date.\r\n[Open=0|Closed=1|Open24Hrs=2|OpenByAppointment=3]"
                                   AdditionalInfo:
                                     type: string
                                     description: 'Any additional comments - open by appointment, short hours during holidays etc.'
                                 description: Hours of Operations information for a single day.
          description: Identify hours of operation on special dates                            
          
 BusinessCategories :
                  BusinessCategoriesObject:
                                 type: object
                                 properties:
                                   Category1:
                                     type: string
                                     description: Business Category 1 (see documentation for list of valid Categories)
                                   Category2:
                                     type: string
                                     description: Business Category 2 (see documentation for list of valid Categories)
                                   Category3:
                                     type: string
                                     description: Business Category 3 (see documentation for list of valid Categories)
                                   Category4:
                                     type: string
                                     description: Business Category 4 (see documentation for list of valid Categories)
                                   Category5:
                                     type: string
                                     description: Business Category 5 (see documentation for list of valid Categories)
                                   Category6:
                                     type: string
                                     description: Business Category 6 (see documentation for list of valid Categories)
                                   Category7:
                                     type: string
                                     description: Business Category 7 (see documentation for list of valid Categories)
                                   Category8:
                                     type: string
                                     description: Business Category 8 (see documentation for list of valid Categories)
                                   Category9:
                                     type: string
                                     description: Business Category 9 (see documentation for list of valid Categories)
                                   Category10:
                                     type: string
                                     description: Business Category 10 (see documentation for list of valid Categories)
                                 description: The list of Business Categories for the Location (see documentation for list of valid Categories)
Chain:
          type: string
          description: The name of the franchise or chain the Location belongs to
Amenities:
          type: string
          description: 'A comma separated list of Amenities available at the Location (e.g.Parking, Free Parking, Parking Garage, Wheelchair Access)'
PaymentMethods:
          type: string
          description: A comma separated list of Payment Methods for the Location (see documentation for list of valid Payment Methods and input format)
 PrimaryContact:
          ContactPersonObject:
                        type: object
                        properties:
                          FullName:
                            type: string
                            description: The full name of the Contact Person
                          FirstName:
                            type: string
                            description: The First Name of the Contact Person (max length 15 chars)
                          MiddleName:
                            type: string
                            description: The Middle Name of the Contact Person
                          LastName:
                            type: string
                            description: The Last Name of the Contact Person (max length 20 chars)
                          Title:
                            type: string
                            description: 'Title (e.g. Regional Sales Manager, Customer Support Technician, etc.) (max length 256 chars)'
                          EmailAddress:
                            type: string
                            description: Contact Email address (must be a valid email address)
                        description: Structured object containing contact information for a Contact Person 
          
  EmailAddress:
          type: string
          description: Contact Email address (must be a valid email address)
      description: Structured object containing contact information for a Contact Person

PhotoURLs :
                  PhotoObject:
                        required:
                          - URL
                        type: object
                        properties:
                          Type:
                            enum:
                              - ProfilePhoto
                              - CoverPhoto
                              - Logo
                              - Other
                            type: string
                            description: 'Type of photo ("ProfilePhoto": often displayed as a series, "CoverPhoto": usually only 1, "Logo": usually only 1, "Other")'
                          URL:
                            type: string
                            description: The URL for the Photo (must be a valid URL)
                          Name:
                            type: string
                            description: The name of the Photo
                          Description:
                            type: string
                            description: A description of the Photo
                        description: Structured object containing a Photo URL and supplementary information about the Photo
 KeywordsSpecialties:
          type: string
          description: A comma separated list of Keywords and/or Specialties used by data providers to refine search listing relevancy for the Location
  CredentialsCertifications:
          type: string
          description: A comma separated list of Credentials and/or Certifications used by data providers to refine search listing relevancy for the Location (max length 200 chars)
  Products:
          type: string
          description: A comma separated list of Products available at the Location which are used by data providers to refine search listing relevancy for the Location
        Services:
          type: string
          description: A comma separated list of Services available at the Location which are used by data providers to refine search listing relevancy for the Location
 Brands:
          type: string
          description: A comma separated list of Brands available at the Location which are used by data providers to refine search listing relevancy for the Location
   YearFounded:
          type: string
          description: The year the Location was founded (must be four digits; e.g. 1992)
   ProfessionalAssociations:
          type: string
          description: A comma separated list of Professional Associations relevant to the Location which are used by data providers to refine search listing relevancy for the Location
 Tagline:
          type: string
          description: A Tagline or slogan for the Location.
  NumberEmployees:
          type: string
          description: The number of employees at the Location (max length 5 chars)
 AreasServed:
          type: string
          description: 'A comma separated list of Areas served by the Location (e.g. Downtown, Uptown, etc.)'
Languages:
          type: string
          description: A comma separated list of Languages spoken at the Location (see documentation for list of valid Languages and input format)
AlternateOrCorporateName:
          type: string
          description: ''
      description: Location Data Model
UserData:
          type: object
          additionalProperties:
            type: string
          description: User defined data dictionary (array of key-value pairs) that can be used to store any additional information about a location
      description: The object contains partial uniModel data. It simplifies the data structure for presentation to the end user
          
          
          
          
          
          
          
```
<h1>3.Create Locations</h1>

Http Verb: POST.

Headers: Content-Type: application/json

         Ocp-Apim-Subscription-Key : (Format - string. Passed into header for Authorization)

Http EndPoint: /location

<strong>FromBody Parameters:</strong>

```{questions}
- ClientId: (Format - uuid. The unique identifier for the Client)

- Name : 'Format - string. 'Location Name'
```


<strong>Response Json Body</strong>

```{questions}
[    
       
    {
        "accountID": "00000000-0000-0000-0000-000000000000",
        "locationID": "e2f30897-bd1b-40e2-b1b6-98e446dc8ced",
        "locationNumber": "test",
        "referenceCode": null,
        "createdBy": "LocationBankAPI",
        "modifiedBy": "LocationBankAPI",
        "created": null,
        "modified": null,
        "locationBankPublicLocationData": {
            "keyFields": {
                "pinMarker": "true",
                "referenceCode2": "test",
                "chainName": null,
                "primarylanguage": "en-"
            },
            "displayPoint": {
                "type": "Calculated",
                "latitude": -25.73134,
                "longitude": 28.21837,
                "verificationType": "Other"
            },
            "businessStatus": "Open",
            "status": "Active",
            "businessName": {
                "name": "test",
                "longName": "test"
            },
            "businessDescription": {
                "description": null,
                "shortDescription": null,
                "longDescription": null
            },
            "primaryAddress": {
                "addressLine1": "",
                "addressLine2": "",
                "addressLine3": "",
                "addressLine4": "",
                "addressLine5": "",
                "neighborhood": "",
                "locality": "",
                "region": "",
                "postalCode": "",
                "countryCode": ""
            },
            "phoneNumbers": {
                "primaryPhoneNumber": "",
                "landline": null,
                "mobile": null,
                "fax": null,
                "tollFree": null
            },
            "websiteURL": "",
            "alternateWebsiteURL": null,
            "mediaURLs": {
                "facebookUrl": "",
                "twitterUrl": "",
                "linkedInUrl": "",
                "instagramUrl": "",
                "pinterestUrl": "",
                "couponUrl": "",
                "socialNetworkUrl": "",
                "videoUrl": ""
            },
            "hoursOfOperation": null,
            "hoursOfOperationStructured": {
                "su": {
                    "ranges": [
                        {
                            "startTime": "08:00AM",
                            "endTime": "05:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "mo": {
                    "ranges": [
                        {
                            "startTime": "08:00AM",
                            "endTime": "05:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "tu": {
                    "ranges": [
                        {
                            "startTime": "08:00AM",
                            "endTime": "05:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "we": {
                    "ranges": [
                        {
                            "startTime": "08:00AM",
                            "endTime": "05:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "th": {
                    "ranges": [
                        {
                            "startTime": "08:00AM",
                            "endTime": "05:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "fr": {
                    "ranges": [
                        {
                            "startTime": "08:00AM",
                            "endTime": "05:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "sa": {
                    "ranges": [
                        {
                            "startTime": "08:00AM",
                            "endTime": "05:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "specialHours": []
            },
            "businessCategories": {
                "category1": "",
                "category2": "",
                "category3": "",
                "category4": "",
                "category5": "",
                "category6": "",
                "category7": "",
                "category8": "",
                "category9": "",
                "category10": ""
            },
            "chain": null,
            "amenities": "",
            "paymentMethods": "",
            "primaryContact": {
                "fullName": null,
                "firstName": null,
                "middleName": null,
                "lastName": null,
                "title": null,
                "emailAddress": null
            },
            "emailAddress": "",
            "photoURLs": [],
            "keywordsSpecialties": "",
            "credentialsCertifications": "",
            "products": "",
            "services": null,
            "brands": null,
            "yearFounded": "",
            "professionalAssociations": "",
            "tagline": null,
            "numberEmployees": "",
            "areasServed": null,
            "languages": "en",
            "alternateOrCorporateName": null
        },
        "userData": null
    },
    {
        "accountID": "00000000-0000-0000-0000-000000000000",
        "locationID": "fdbddbf7-e73e-4bbe-b9f6-b49f0675ebff",
        "locationNumber": "SC103",
        "referenceCode": null,
        "createdBy": "LocationBankAPI",
        "modifiedBy": "LocationBankAPI",
        "created": null,
        "modified": null,
        "locationBankPublicLocationData": {
            "keyFields": {
                "pinMarker": "true",
                "referenceCode2": "SC103",
                "chainName": "Brand Name - Location number 5",
                "primarylanguage": "en-ZA"
            },
            "displayPoint": {
                "type": "Calculated",
                "latitude": -33.7291942,
                "longitude": 18.4386631,
                "verificationType": "Other"
            },
            "businessStatus": "Open",
            "status": "Active",
            "businessName": {
                "name": "Location 5",
                "longName": "Brand Name Example Location 5"
            },
            "businessDescription": {
                "description": "",
                "shortDescription": "Test 20:17 2021/01/31",
                "longDescription": ""
            },
            "primaryAddress": {
                "addressLine1": "Cnr 6th Ave & Beach Rd",
                "addressLine2": "Shop 103",
                "addressLine3": "",
                "addressLine4": "",
                "addressLine5": "",
                "neighborhood": "Melkbosstrand",
                "locality": "Cape Town",
                "region": "Some place",
                "postalCode": "7441",
                "countryCode": "ZA"
            },
            "phoneNumbers": {
                "primaryPhoneNumber": "0107861031",
                "landline": null,
                "mobile": null,
                "fax": null,
                "tollFree": null
            },
            "websiteURL": "http://www.yowzit.com/",
            "alternateWebsiteURL": "http://www.yowzit.com/",
            "mediaURLs": {
                "facebookUrl": "",
                "twitterUrl": "",
                "linkedInUrl": "",
                "instagramUrl": "",
                "pinterestUrl": "",
                "couponUrl": "",
                "socialNetworkUrl": "",
                "videoUrl": ""
            },
            "hoursOfOperation": null,
            "hoursOfOperationStructured": {
                "su": {
                    "ranges": [
                        {
                            "startTime": "09:00AM",
                            "endTime": "01:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "mo": {
                    "ranges": [
                        {
                            "startTime": "09:00AM",
                            "endTime": "01:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "tu": {
                    "ranges": [
                        {
                            "startTime": "09:00AM",
                            "endTime": "01:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "we": {
                    "ranges": [
                        {
                            "startTime": "09:00AM",
                            "endTime": "01:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "th": {
                    "ranges": [
                        {
                            "startTime": "09:00AM",
                            "endTime": "01:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "fr": {
                    "ranges": [
                        {
                            "startTime": "09:00AM",
                            "endTime": "01:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "sa": {
                    "ranges": [
                        {
                            "startTime": "11:00AM",
                            "endTime": "06:00PM"
                        }
                    ],
                    "state": "Open",
                    "additionalInfo": ""
                },
                "specialHours": []
            },
            "businessCategories": {
                "category1": "Pool Cleaning Service",
                "category2": "Swimming Pool Supply Store",
                "category3": "Swimming",
                "category4": "Swimming Instructor",
                "category5": "",
                "category6": "",
                "category7": "",
                "category8": "",
                "category9": "",
                "category10": ""
            },
            "chain": null,
            "amenities": "",
            "paymentMethods": "",
            "primaryContact": {
                "fullName": null,
                "firstName": null,
                "middleName": null,
                "lastName": null,
                "title": null,
                "emailAddress": null
            },
            "emailAddress": "",
            "photoURLs": [],
            "keywordsSpecialties": "test",
            "credentialsCertifications": "",
            "products": "",
            "services": null,
            "brands": null,
            "yearFounded": "20190310",
            "professionalAssociations": "",
            "tagline": null,
            "numberEmployees": "",
            "areasServed": null,
            "languages": "en",
            "alternateOrCorporateName": null
        },
        "userData": null
    }
]
```

<strong>Response Description:</strong>


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
 BusinessName:
        BusinessNameObject:
      type: object
      properties:
        Name:
          type: string
          description: A standard length Business Name for the Location; This field is needed to submit data to Acxiom and Bing (max length 30 chars)
        LongName:
          type: string
          description: A long Business Name for the Location (max length 80 chars)
        Locale:
          enum:
            - Not_set
            - af_ZA
            - am_ET
            - ar_AE
            - ar_BH
            - ar_DZ
            - ar_EG
            - ar_IQ
            - ar_JO
            - ar_KW
            - ar_LB
            - ar_LY
            - ar_MA
            - arn_CL
            - ar_OM
            - ar_QA
            - ar_SA
            - ar_SY
            - ar_TN
            - ar_YE
            - as_IN
            - az_Cyrl_AZ
            - az_Latn_AZ
            - ba_RU
            - be_BY
            - bg_BG
            - bn_BD
            - bn_IN
            - bo_CN
            - br_FR
            - bs_Cyrl_BA
            - bs_Latn_BA
            - ca_ES
            - co_FR
            - cs_CZ
            - cy_GB
            - da_DK
            - de_AT
            - de_CH
            - de_DE
            - de_LI
            - de_LU
            - dsb_DE
            - dv_MV
            - el_GR
            - en_029
            - en_AU
            - en_BZ
            - en_CA
            - en_GB
            - en_IE
            - en_IN
            - en_JM
            - en_MY
            - en_NZ
            - en_PH
            - en_SG
            - en_TT
            - en_US
            - en_ZA
            - en_ZW
            - es_AR
            - es_BO
            - es_CL
            - es_CO
            - es_CR
            - es_DO
            - es_EC
            - es_ES
            - es_GT
            - es_HN
            - es_MX
            - es_NI
            - es_PA
            - es_PE
            - es_PR
            - es_PY
            - es_SV
            - es_US
            - es_UY
            - es_VE
            - et_EE
            - eu_ES
            - fa_IR
            - fi_FI
            - fil_PH
            - fo_FO
            - fr_BE
            - fr_CA
            - fr_CH
            - fr_FR
            - fr_LU
            - fr_MC
            - fy_NL
            - ga_IE
            - gd_GB
            - gl_ES
            - gsw_FR
            - gu_IN
            - ha_Latn_NG
            - he_IL
            - hi_IN
            - hr_BA
            - hr_HR
            - hsb_DE
            - hu_HU
            - hy_AM
            - id_ID
            - ig_NG
            - ii_CN
            - is_IS
            - it_CH
            - it_IT
            - iu_Cans_CA
            - iu_Latn_CA
            - ja_JP
            - ka_GE
            - kk_KZ
            - kl_GL
            - km_KH
            - kn_IN
            - kok_IN
            - ko_KR
            - ky_KG
            - lb_LU
            - lo_LA
            - lt_LT
            - lv_LV
            - mi_NZ
            - mk_MK
            - ml_IN
            - mn_MN
            - mn_Mong_CN
            - moh_CA
            - mr_IN
            - ms_BN
            - ms_MY
            - mt_MT
            - nb_NO
            - ne_NP
            - nl_BE
            - nl_NL
            - nn_NO
            - nso_ZA
            - oc_FR
            - or_IN
            - pa_IN
            - pl_PL
            - prs_AF
            - ps_AF
            - pt_BR
            - pt_PT
            - qut_GT
            - quz_BO
            - quz_EC
            - quz_PE
            - rm_CH
            - ro_RO
            - ru_RU
            - rw_RW
            - sah_RU
            - sa_IN
            - se_FI
            - se_NO
            - se_SE
            - si_LK
            - sk_SK
            - sl_SI
            - sma_NO
            - sma_SE
            - smj_NO
            - smj_SE
            - smn_FI
            - sms_FI
            - sq_AL
            - sr_Cyrl_BA
            - sr_Cyrl_CS
            - sr_Cyrl_ME
            - sr_Cyrl_RS
            - sr_Latn_BA
            - sr_Latn_CS
            - sr_Latn_ME
            - sr_Latn_RS
            - sv_FI
            - sv_SE
            - sw_KE
            - syr_SY
            - ta_IN
            - te_IN
            - tg_Cyrl_TJ
            - th_TH
            - tk_TM
            - tn_ZA
            - tr_TR
            - tt_RU
            - tzm_Latn_DZ
            - ug_CN
            - uk_UA
            - ur_PK
            - uz_Cyrl_UZ
            - uz_Latn_UZ
            - vi_VN
            - wo_SN
            - xh_ZA
            - yo_NG
            - zh_CN
            - zh_HK
            - zh_MO
            - zh_SG
            - zh_TW
            - zu_ZA
          type: string
          description: Primary language
      description: Structured object containing different length Business Names for the Location to enable data submission to different services
BusinessDescription
                  type: object
      properties:
        Description:
          type: string
          description: A description of the Business for the Location; This field is needed to submit data to Yalwa (max length 200 chars)
        ShortDescription:
          type: string
          description: A short description of the Business for the Location; This field is needed to submit data to Foursquare (max length 160 chars)
        LongDescription:
          type: string
          description: A long description of the Business for the Location; This field is needed to submit data to Superpages (min length 250 chars; max length 4000 chars)
      description: Structured object containing different length descriptions of the Business for the Location to enable data submission to different services
PhoneNumbers:
         PhoneNumbersObject:
      type: object
      properties:
        PrimaryPhoneNumber:
          type: string
          description: The Primary Phone Number for the Location (see documentation for input format) (Infogroup does not allow toll-free numbers; Location data can only be submitted to Infogroup when the PrimaryPhoneNumber is a local number)
        Landline:
          type: string
          description: The Landline Phone Number for the Location (if different from Primary number) (see documentation for input format)
        Mobile:
          type: string
          description: The Mobile Phone Number for the Location (if different from Primary number) (see documentation for input format)
        Fax:
          type: string
          description: The Fax Number for the Location (see documentation for input format)
        TollFree:
          type: string
          description: The Toll-Free Phone Number for the Location (see documentation for input format)
      description: The list of Phone Numbers for the Location (see documentation for input format)
      
         WebsiteURL:
          type: string
          description: 'The Website for the Location; Must be a valid URL with only sub, main, and top-level domain information (max length 40 char)'
        AlternateWebsiteURL:
          type: string
          description: An Alternate Website for the Location; potentially a corporate website for the location (no max length)
        MediaURLs:
                   MediaURLsObject:
                              MediaURLsObject:
                                 type: object
                                 properties:
                                   FacebookURL:
                                     type: string
                                     description: The Facebook URL for the Location (must be a valid URL)
                                   TwitterURL:
                                     type: string
                                     description: The Twitter URL for the Location (must be a valid URL)
                                   LinkedInURL:
                                     type: string
                                     description: The LinkedIn URL for the Location (must be a valid URL)
                                   InstagramURL:
                                     type: string
                                     description: The Instagram URL for the Location (must be a valid URL)
                                   PinterestURL:
                                     type: string
                                     description: The Pinterest URL for the Location (must be a valid URL)
                                   CouponURL:
                                     type: string
                                     description: The Coupon URL for the Location (must be a valid URL)
                                   SocialNetworkURL:
                                     type: string
                                     description: The Social Network URL for the Location (must be a valid URL)
                                   VideoURL:
                                     type: string
                                     description: The Video URL for the Location (must be a valid URL)
                                 description: The list of Social Media URLs for the Location                 
          
 HoursOfOperation:
          type: string
          description: String representation of Hours of Operation structured object for the Location
          readOnly: true
          
  HoursOfOperationStructured:
     HoursOfOperationObject:
            type: object
               properties:
                     SpecialHours:
                       type: array
                      items:
                      HoursOfOperationItemEx:
                             required:
                                 - Date
                                       type: object
                                          properties:
                                            Date:
                                              type: string
                                              description: Optional. Set the specific date
                                            Ranges:
                                              type: array
                                              items:
                                               TimeRange:
                                                   type: object
                                                   properties:
                                                     StartTime:
                                                       type: string
                                                       description: Start time
                                                     EndTime:
                                                       type: string
                                                       description: End time
                                                   description: 'Time period, less than 24 hours'
                                                      description: A list of time periods
                          State:
                            enum:
                              - Open
                              - Closed
                              - Open24Hrs
                              - OpenByAppointment
                            type: string
                            description: " Represent open/close state on the specific date.\r\n[Open=0|Closed=1|Open24Hrs=2|OpenByAppointment=3]"
                          AdditionalInfo:
                            type: string
                            description: 'Any additional comments - open by appointment, short hours during holidays etc.'
                        description: Hours of Operations information for a single day.
                                     description: Identify hours of operation on special dates   
                                   Su:
                                     HoursOfOperationItem:
                                          type: object
                                          properties:
                                            Ranges:
                                              type: array
                                              items:
                                              TimeRange:
                                                 type: object
                                                  properties:
                                                    StartTime:
                                                      type: string
                                                      description: Start time
                                                    EndTime:
                                                      type: string
                                                      description: End time
                                                 description: 'Time period, less than 24 hours'
                                              description: A list of time periods
                                            State:
                                              enum:
                                                - Open
                                                - Closed
                                                - Open24Hrs
                                                - OpenByAppointment
                                              type: string
                                              description: " Represent open/close state on the specific date.\r\n[Open=0|Closed=1|Open24Hrs=2|OpenByAppointment=3]"
                                            AdditionalInfo:
                                              type: string
                                              description: 'Any additional comments - open by appointment, short hours during holidays etc.'
                                          description: Hours of operation
                                   Mo:
                                        HoursOfOperationItem:
                                          type: object
                                          properties:
                                            Ranges:
                                              type: array
                                              items:
                                              TimeRange:
                                                 type: object
                                                  properties:
                                                    StartTime:
                                                      type: string
                                                      description: Start time
                                                    EndTime:
                                                      type: string
                                                      description: End time
                                                 description: 'Time period, less than 24 hours'
                                              description: A list of time periods
                                            State:
                                              enum:
                                                - Open
                                                - Closed
                                                - Open24Hrs
                                                - OpenByAppointment
                                              type: string
                                              description: " Represent open/close state on the specific date.\r\n[Open=0|Closed=1|Open24Hrs=2|OpenByAppointment=3]"
                                            AdditionalInfo:
                                              type: string
                                              description: 'Any additional comments - open by appointment, short hours during holidays etc.'
                                          description: Hours of operation
                                   Tu:
                                         HoursOfOperationItem:
                                          type: object
                                          properties:
                                            Ranges:
                                              type: array
                                              items:
                                              TimeRange:
                                                 type: object
                                                  properties:
                                                    StartTime:
                                                      type: string
                                                      description: Start time
                                                    EndTime:
                                                      type: string
                                                      description: End time
                                                 description: 'Time period, less than 24 hours'
                                              description: A list of time periods
                                            State:
                                              enum:
                                                - Open
                                                - Closed
                                                - Open24Hrs
                                                - OpenByAppointment
                                              type: string
                                              description: " Represent open/close state on the specific date.\r\n[Open=0|Closed=1|Open24Hrs=2|OpenByAppointment=3]"
                                            AdditionalInfo:
                                              type: string
                                              description: 'Any additional comments - open by appointment, short hours during holidays etc.'
                                          description: Hours of operation
                                   We:
                                      HoursOfOperationItem:
                                          type: object
                                          properties:
                                            Ranges:
                                              type: array
                                              items:
                                              TimeRange:
                                                 type: object
                                                  properties:
                                                    StartTime:
                                                      type: string
                                                      description: Start time
                                                    EndTime:
                                                      type: string
                                                      description: End time
                                                 description: 'Time period, less than 24 hours'
                                              description: A list of time periods
                                            State:
                                              enum:
                                                - Open
                                                - Closed
                                                - Open24Hrs
                                                - OpenByAppointment
                                              type: string
                                              description: " Represent open/close state on the specific date.\r\n[Open=0|Closed=1|Open24Hrs=2|OpenByAppointment=3]"
                                            AdditionalInfo:
                                              type: string
                                              description: 'Any additional comments - open by appointment, short hours during holidays etc.'
                                          description: Hours of operation
                                   Th:
                                       HoursOfOperationItem:
                                          type: object
                                          properties:
                                            Ranges:
                                              type: array
                                              items:
                                              TimeRange:
                                                 type: object
                                                  properties:
                                                    StartTime:
                                                      type: string
                                                      description: Start time
                                                    EndTime:
                                                      type: string
                                                      description: End time
                                                 description: 'Time period, less than 24 hours'
                                              description: A list of time periods
                                            State:
                                              enum:
                                                - Open
                                                - Closed
                                                - Open24Hrs
                                                - OpenByAppointment
                                              type: string
                                              description: " Represent open/close state on the specific date.\r\n[Open=0|Closed=1|Open24Hrs=2|OpenByAppointment=3]"
                                            AdditionalInfo:
                                              type: string
                                              description: 'Any additional comments - open by appointment, short hours during holidays etc.'
                                          description: Hours of operation
                                   Fr:
                                       HoursOfOperationItem:
                                          type: object
                                          properties:
                                            Ranges:
                                              type: array
                                              items:
                                              TimeRange:
                                                 type: object
                                                  properties:
                                                    StartTime:
                                                      type: string
                                                      description: Start time
                                                    EndTime:
                                                      type: string
                                                      description: End time
                                                 description: 'Time period, less than 24 hours'
                                              description: A list of time periods
                                            State:
                                              enum:
                                                - Open
                                                - Closed
                                                - Open24Hrs
                                                - OpenByAppointment
                                              type: string
                                              description: " Represent open/close state on the specific date.\r\n[Open=0|Closed=1|Open24Hrs=2|OpenByAppointment=3]"
                                            AdditionalInfo:
                                              type: string
                                              description: 'Any additional comments - open by appointment, short hours during holidays etc.'
                                          description: Hours of operation
                                   Sa:
                                       HoursOfOperationItem:
                                          type: object
                                          properties:
                                            Ranges:
                                              type: array
                                              items:
                                              TimeRange:
                                                 type: object
                                                  properties:
                                                    StartTime:
                                                      type: string
                                                      description: Start time
                                                    EndTime:
                                                      type: string
                                                      description: End time
                                                 description: 'Time period, less than 24 hours'
                                              description: A list of time periods
                                            State:
                                              enum:
                                                - Open
                                                - Closed
                                                - Open24Hrs
                                                - OpenByAppointment
                                              type: string
                                              description: " Represent open/close state on the specific date.\r\n[Open=0|Closed=1|Open24Hrs=2|OpenByAppointment=3]"
                                            AdditionalInfo:
                                              type: string
                                              description: 'Any additional comments - open by appointment, short hours during holidays etc.'
                                          description: Hours of operation                  

 SpecialHours:
          type: array
          items:
            HoursOfOperationItemEx:
                      required:
                          - Date
                      type: object
                      properties:
                       Date:
                          type: string
                          description: Optional. Set the specific date
                              Ranges:
                                 type: array
                                 items:
                                       TimeRange:
                                          type: object
                                          properties:
                                            StartTime:
                                              type: string
                                              description: Start time
                                            EndTime:
                                              type: string
                                              description: End time
                                          description: 'Time period, less than 24 hours'
                                     description: A list of time periods
                                   State:
                                     enum:
                                       - Open
                                       - Closed
                                       - Open24Hrs
                                       - OpenByAppointment
                                     type: string
                                     description: " Represent open/close state on the specific date.\r\n[Open=0|Closed=1|Open24Hrs=2|OpenByAppointment=3]"
                                   AdditionalInfo:
                                     type: string
                                     description: 'Any additional comments - open by appointment, short hours during holidays etc.'
                                 description: Hours of Operations information for a single day.
          description: Identify hours of operation on special dates                            
          
 BusinessCategories :
                  BusinessCategoriesObject:
                                 type: object
                                 properties:
                                   Category1:
                                     type: string
                                     description: Business Category 1 (see documentation for list of valid Categories)
                                   Category2:
                                     type: string
                                     description: Business Category 2 (see documentation for list of valid Categories)
                                   Category3:
                                     type: string
                                     description: Business Category 3 (see documentation for list of valid Categories)
                                   Category4:
                                     type: string
                                     description: Business Category 4 (see documentation for list of valid Categories)
                                   Category5:
                                     type: string
                                     description: Business Category 5 (see documentation for list of valid Categories)
                                   Category6:
                                     type: string
                                     description: Business Category 6 (see documentation for list of valid Categories)
                                   Category7:
                                     type: string
                                     description: Business Category 7 (see documentation for list of valid Categories)
                                   Category8:
                                     type: string
                                     description: Business Category 8 (see documentation for list of valid Categories)
                                   Category9:
                                     type: string
                                     description: Business Category 9 (see documentation for list of valid Categories)
                                   Category10:
                                     type: string
                                     description: Business Category 10 (see documentation for list of valid Categories)
                                 description: The list of Business Categories for the Location (see documentation for list of valid Categories)
Chain:
          type: string
          description: The name of the franchise or chain the Location belongs to
Amenities:
          type: string
          description: 'A comma separated list of Amenities available at the Location (e.g.Parking, Free Parking, Parking Garage, Wheelchair Access)'
PaymentMethods:
          type: string
          description: A comma separated list of Payment Methods for the Location (see documentation for list of valid Payment Methods and input format)
 PrimaryContact:
          ContactPersonObject:
                        type: object
                        properties:
                          FullName:
                            type: string
                            description: The full name of the Contact Person
                          FirstName:
                            type: string
                            description: The First Name of the Contact Person (max length 15 chars)
                          MiddleName:
                            type: string
                            description: The Middle Name of the Contact Person
                          LastName:
                            type: string
                            description: The Last Name of the Contact Person (max length 20 chars)
                          Title:
                            type: string
                            description: 'Title (e.g. Regional Sales Manager, Customer Support Technician, etc.) (max length 256 chars)'
                          EmailAddress:
                            type: string
                            description: Contact Email address (must be a valid email address)
                        description: Structured object containing contact information for a Contact Person 
          
  EmailAddress:
          type: string
          description: Contact Email address (must be a valid email address)
      description: Structured object containing contact information for a Contact Person

PhotoURLs :
                  PhotoObject:
                        required:
                          - URL
                        type: object
                        properties:
                          Type:
                            enum:
                              - ProfilePhoto
                              - CoverPhoto
                              - Logo
                              - Other
                            type: string
                            description: 'Type of photo ("ProfilePhoto": often displayed as a series, "CoverPhoto": usually only 1, "Logo": usually only 1, "Other")'
                          URL:
                            type: string
                            description: The URL for the Photo (must be a valid URL)
                          Name:
                            type: string
                            description: The name of the Photo
                          Description:
                            type: string
                            description: A description of the Photo
                        description: Structured object containing a Photo URL and supplementary information about the Photo
 KeywordsSpecialties:
          type: string
          description: A comma separated list of Keywords and/or Specialties used by data providers to refine search listing relevancy for the Location
  CredentialsCertifications:
          type: string
          description: A comma separated list of Credentials and/or Certifications used by data providers to refine search listing relevancy for the Location (max length 200 chars)
  Products:
          type: string
          description: A comma separated list of Products available at the Location which are used by data providers to refine search listing relevancy for the Location
        Services:
          type: string
          description: A comma separated list of Services available at the Location which are used by data providers to refine search listing relevancy for the Location
 Brands:
          type: string
          description: A comma separated list of Brands available at the Location which are used by data providers to refine search listing relevancy for the Location
   YearFounded:
          type: string
          description: The year the Location was founded (must be four digits; e.g. 1992)
   ProfessionalAssociations:
          type: string
          description: A comma separated list of Professional Associations relevant to the Location which are used by data providers to refine search listing relevancy for the Location
 Tagline:
          type: string
          description: A Tagline or slogan for the Location.
  NumberEmployees:
          type: string
          description: The number of employees at the Location (max length 5 chars)
 AreasServed:
          type: string
          description: 'A comma separated list of Areas served by the Location (e.g. Downtown, Uptown, etc.)'
Languages:
          type: string
          description: A comma separated list of Languages spoken at the Location (see documentation for list of valid Languages and input format)
AlternateOrCorporateName:
          type: string
          description: ''
      description: Location Data Model
UserData:
          type: object
          additionalProperties:
            type: string
          description: User defined data dictionary (array of key-value pairs) that can be used to store any additional information about a location
      description: The object contains partial uniModel data. It simplifies the data structure for presentation to the end user
          
          
          
          
          
          
          
```
