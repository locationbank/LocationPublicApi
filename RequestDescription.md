
| Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|
| AccountID      | GUID  | The unique identifier for the Account                                                                    |
| LocationID     | GUID  | The unique identifier for the Location (auto-generated)                                                  |
| LocationNumber | string |**Required** A friendly number used internally to reference the specified Location & "A unique ID that you assign to each of your locations to ensure that changes are applied accurately in your account. This value will not be publicly visible anywhere.Generally provided by the client."                 |
| ReferenceCode  | string | An identifier for the Location specified by the user of the API                                          |
| CreatedBy      | string | String indicating who or what created the Location                                                       |
| ModifiedBy     | string | String indicating who or what last modified the Location                                                 |
| Created        | string | 'Time, location was created'                                                                             |
| Modified       | string | Time location was modified                                                                               |
| KeyFields      | object |**Required** Dynamic storage of the key fields for the location or custom data which is used by specific applications |
| DisplayPoint     | Object | [DisplayPointObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#displaypointobject) |  
| BusinessStatus | enum |**Required** [The Status of the Business](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#businessstatus)                                                                 |
| Status         | enum | [Record status](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#Recordstatus)                                                                                                                  |
| BusinessName   | Object |**Required** [BusinessNameObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#businessnameobject-) "A business name is required for each location.
 
The name of your business that will appear on your listing. Represent your business exactly as it appears in the offline world. Your business name must be no longer than 80 characters."|  
| BusinessDescription | Object | [BusinessDescriptionObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#businessdescriptionobject-)  |
| PrimaryAddress | Object |**Required** [AddressObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#addressobject-)  |
| phoneNumbers        | Object | [PhoneNumbersObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#phonenumbersobject-)  |
| WebsiteURL          | string |**Required** The Website for the Location; Must be a valid URL with only sub, main, and top-level domain information (max length 40 char)  |
| mediaURLs           | Object | [MediaURLsObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#mediaurlsobject-)      | 
| HoursOfOperationStructured | Object  |**Required** [HoursOfOperationObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#hoursofoperationobject--)                                                        |
| businessCategories | Object |**Required** [BusinessCategoriesObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#businesscategoriesobject--)                                                                                                     
| Chain              | string | The name of the franchise or chain the Location belongs to                                                                   |
| Amenities          | string | A comma separated list of Amenities available at the Location (e.g.Parking, Free Parking, Parking Garage, Wheelchair Access) |
| PaymentMethods     | string | A comma separated list of Payment Methods for the Location                                                                   |
| PrimaryContact     | Object | [ContactPersonObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#contactpersonobject--)                                                                                                          |
| EmailAddress       | string | The primary email address for the Location; Must be a valid email address (max length 60 chars)                              |
| PhotoURLs                 | Array  | [PhotoObject](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#photourlobject--)                                                                                                           |                                          
| KeywordsSpecialties       | string | A comma separated list of Keywords and/or Specialties used by data providers to refine search listing relevancy for the Location                                  |
| CredentialsCertifications | string | A comma separated list of Credentials and/or Certifications used by data providers to refine search listing relevancy for the Location (max length 200 chars)     |
| Products                  | string | A comma separated list of Products available at the Location which are used by data providers to refine search listing relevancy for the Location                 |
| Services                  | string |  comma separated list of Services available at the Location which are used by data providers to refine search listing relevancy for the Location                  |
| Brands                    | string |**Required**  A comma separated list of Brands available at the Location which are used by data providers to refine search listing relevancy for the Location                  |
| YearFounded               | string | The year the Location was founded (must be four digits; e.g. 1992)                                                                                                |
| ProfessionalAssociations  | string | A comma separated list of Professional Associations relevant to the Location which are used by data providers to refine search listing relevancy for the Location |
| Tagline                   | string | A Tagline or slogan for the Location.                                                                                                                             |
| NumberEmployees           | string | The number of employees at the Location (max length 5 chars)                                                                                                      |
| AreasServed               | string | A comma separated list of Areas served by the Location (e.g. Downtown, Uptown, etc.)                                                                              |
| Languages                 | string | A comma separated list of Languages spoken at the Location (see documentation for list of valid Languages and input format)                                       |
| AlternateOrCorporateName  | string | ''                                                                                                                                                                |

<h2>DisplayPointObject</h2>

| Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                   
| Type             | enum   | - [DisplayPointType](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#type)                                                                   |
| Latitude         | number |**Required** 'Latitude of the Location represented by a high precision decimal number'            |
| Longitude        | number | **Required** 'Longitude of the Location represented by a high precision decimal number'           |
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


<h2>Type</h2>

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

| Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                   
| Name           | string |**Required** A standard length Business Name for the Location; This field is needed to submit data to Acxiom and Bing (max length 30 chars) |
| LongName       | string | A long Business Name for the Location (max length 80 chars)                                                                    |
| Locale         | Enum | [Primary language](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#businessnamelocale--) 


  <h2>BusinessDescriptionObject </h2>
  
| Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                   
| Description         | string |**Required** A description of the Business for the Location; This field is needed to submit data to Yalwa (max length 200 chars)                                  |
| ShortDescription    | string |**Required** A short description of the Business for the Location; This field is needed to submit data to Foursquare (max length 160 chars)                       |
| longDescription     | string | A long description of the Business for the Location; This field is needed to submit data to Superpages (min length 250 chars; max length 4000 chars) |


  <h2>AddressObject </h2>
  
| Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                   
| AddressLine1   | string |**Required** First line of an address (max length 80 chars).                                                                                                                                           |
| AddressLine2   | string | econd line of an address (max length 80 chars).                                                                                                                                           |
| AddressLine3   | string | Third line of an address (max length 80 chars)                                                                                                                                            |
| AddressLine4   | string | Fourth line of an address (max length 80 chars)                                                                                                                                           |
| AddressLine5   | string | Fifth line of an address (max length 80 chars)                                                                                                                                            |
| Neighborhood   | string |  Neighborhood represents an official sub-locality - typically an area within a town or city (max length 200 chars)                                                                        |
| Locality       | string | **Required** Locality generally represents a City or Town (max length 28 chars)                                                                                                                       |
| Region         | string | 'A Region represents the State or Province; depending on the specified CountryCode, this field may be required and the input format validated (see documentation for validation details)' |
| PostalCode     | string | **Required** Postal Code or Zip Code; depending on the specified CountryCode, this field may be required and the input format validated (see documentation for validation details)'                   |
| CountryCode    | string | **Required** 'Two letter ISO 3166-1 alpha-2 country code representing the Country of a Location (e.g. US, CA, FR, DE, etc.)                                                                            |


  <h2>PhoneNumbersObject </h2>
  
  | Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|    
|  PrimaryPhoneNumber | string |**Required** The Primary Phone Number for the Location                                                                                      |
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



  <h2>HoursOfOperationObject  </h2>
  
 | Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|    
| HoursOfOperationObject     | string  | [Su](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#day-)                                                                            |
| HoursOfOperationObject     | string  | [Mo](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#day-)                                                                            |
| HoursOfOperationObject     | string  | [Tu](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#day-)                                                                            |
| HoursOfOperationObject     | string  | [We](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#day-)                                                                            |
| HoursOfOperationObject     | string  | [Th](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#day-)                                                                            |
| HoursOfOperationObject     | string  | [Fr](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#day-)                                                                            |
| HoursOfOperationObject     | string  | [Sa](https://github.com/locationbank/LocationPublicApi/blob/main/RequestDescription.md#day-)                                                                            |


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
  
 | Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                                                                            
| Category1          | string |**Required** Business Category 1                                                                                                          |
| Category2          | string | Business Category 2                                                                                                          |
| Category3          | string | Business Category 3                                                                                                          |
| Category4          | string | Business Category 4                                                                                                          |
| Category5          | string | Business Category 5                                                                                                          |
| Category6          | string | Business Category 6                                                                                                          |
| Category7          | string | Business Category 7                                                                                                          |
| Category8          | string | Business Category 8                                                                                                          |
| Category9          | string | Business Category 9                                                                                                          |


 <h2>ContactPersonObject  </h2>
  
 | Fields         | Type   | Description                                                                                              |
|----------------|--------|----------------------------------------------------------------------------------------------------------|                                                                                            
| FullName     | string | The full name of the Contact Person                                                           |
| FirstName    | string | The First Name of the Contact Person (max length 15 chars)                                    |
| MiddleName   | string | The Middle Name of the Contact Person                                                         |
| LastName     | string | The Last Name of the Contact Person (max length 20 chars)                                     |
| Title        | string | Title (e.g. Regional Sales Manager, Customer Support Technician, etc.) (max length 256 chars) |
| EmailAddress | string | Contact Email address (must be a valid email address)                                         |


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

 <h2>BusinessNameLocale  </h2>


|                  Enum |
|-------------------------:|
|                    Not_set |
|                    af_ZA |
|                    am_ET |
|                    ar_AE |
|                    ar_BH |
|                    ar_DZ |
|                    ar_EG |
|                    ar_IQ |
|                    ar_JO |
|                    ar_KW |
|                    ar_LB |
|                    ar_LY |
|                    ar_MA |
|                   arn_CL |
|                    ar_OM |
|                    ar_QA |
|                    ar_SA |
|                    ar_SY |
|                    ar_TN |
|                    ar_YE |
|                    as_IN |
|               az_Cyrl_AZ |
|               az_Latn_AZ |
|                    ba_RU |
|                    be_BY |
|                    bg_BG |
|                    bn_BD |
|                    bn_IN |
|                    bo_CN |
|                    br_FR |
|               bs_Cyrl_BA |
|               bs_Latn_BA |
|                    ca_ES |
|                    co_FR |
|                    cs_CZ |
|                    cy_GB |
|                    da_DK |
|                    de_AT |
|                    de_CH |
|                    de_DE |
|                    de_LI |
|                    de_LU |
|                   dsb_DE |
|                    dv_MV |
|                    el_GR |
|                   en_029 |
|                    en_AU |
|                    en_BZ |
|                    en_CA |
|                    en_GB |
|                    en_IE |
|                    en_IN |
|                    en_JM |
|                    en_MY |
|                    en_NZ |
|                    en_PH |
|                    en_SG |
|                    en_TT |
|                    en_US |
|                    en_ZA |
|                    en_ZW |
|                    es_AR |
|                    es_BO |
|                    es_CL |
|                    es_CO |
|                    es_CR |
|                    es_DO |
|                    es_EC |
|                    es_ES |
|                    es_GT |
|                    es_HN |
|                    es_MX |
|                    es_NI |
|                    es_PA |
|                    es_PE |
|                    es_PR |
|                    es_PY |
|                    es_SV |
|                    es_US |
|                    es_UY |
|                    es_VE |
|                    et_EE |
|                    eu_ES |
|                    fa_IR |
|                    fi_FI |
|                   fil_PH |
|                    fo_FO |
|                    fr_BE |
|                    fr_CA |
|                    fr_CH |
|                    fr_FR |
|                    fr_LU |
|                    fr_MC |
|                    fy_NL |
|                    ga_IE |
|                    gd_GB |
|                    gl_ES |
|                   gsw_FR |
|                    gu_IN |
|               ha_Latn_NG |
|                    he_IL |
|                    hi_IN |
|                    hr_BA |
|                    hr_HR |
|                   hsb_DE |
|                    hu_HU |
|                    hy_AM |
|                    id_ID |
|                    ig_NG |
|                    ii_CN |
|                    is_IS |
|                    it_CH |
|                    it_IT |
|               iu_Cans_CA |
|               iu_Latn_CA |
|                    ja_JP |
|                    ka_GE |
|                    kk_KZ |
|                    kl_GL |
|                    km_KH |
|                    kn_IN |
|                   kok_IN |
|                    ko_KR |
|                    ky_KG |
|                    lb_LU |
|                    lo_LA |
|                    lt_LT |
|                    lv_LV |
|                    mi_NZ |
|                    mk_MK |
|                    ml_IN |
|                    mn_MN |
|               mn_Mong_CN |
|                   moh_CA |
|                    mr_IN |
|                    ms_BN |
|                    ms_MY |
|                    mt_MT |
|                    nb_NO |
|                    ne_NP |
|                    nl_BE |
|                    nl_NL |
|                    nn_NO |
|                   nso_ZA |
|                    oc_FR |
|                    or_IN |
|                    pa_IN |
|                    pl_PL |
|                   prs_AF |
|                    ps_AF |
|                    pt_BR |
|                    pt_PT |
|                   qut_GT |
|                   quz_BO |
|                   quz_EC |
|                   quz_PE |
|                    rm_CH |
|                    ro_RO |
|                    ru_RU |
|                    rw_RW |
|                   sah_RU |
|                    sa_IN |
|                    se_FI |
|                    se_NO |
|                    se_SE |
|                    si_LK |
|                    sk_SK |
|                    sl_SI |
|                   sma_NO |
|                   sma_SE |
|                   smj_NO |
|                   smj_SE |
|                   smn_FI |
|                   sms_FI |
|                    sq_AL |
|               sr_Cyrl_BA |
|               sr_Cyrl_CS |
|               sr_Cyrl_ME |
|               sr_Cyrl_RS |
|               sr_Latn_BA |
|               sr_Latn_CS |
|               sr_Latn_ME |
|               sr_Latn_RS |
|                    sv_FI |
|                    sv_SE |
|                    sw_KE |
|                   syr_SY |
|                    ta_IN |
|                    te_IN |
|               tg_Cyrl_TJ |
|                    th_TH |
|                    tk_TM |
|                    tn_ZA |
|                    tr_TR |
|                    tt_RU |
|              tzm_Latn_DZ |
|                    ug_CN |
|                    uk_UA |
|                    ur_PK |
|               uz_Cyrl_UZ |
|               uz_Latn_UZ |
|                    vi_VN |
|                    wo_SN |
|                    xh_ZA |
|                    yo_NG |
|                    zh_CN |
|                    zh_HK |
|                    zh_MO |
|                    zh_SG |
|                    zh_TW |
|                    zu_ZA |