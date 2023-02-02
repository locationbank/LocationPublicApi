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

Http EndPoint: /locations

QueryString Parameters:

<textbox>ClientID: (string - Unique client id for every client - required)
ReportType: (string - Supported report types are "Location", "SubLocality", "Locality", "AdministrativeArea", "Country", "MonthlyData", "DailySeries"
              Report types are case sensitive - required)
FromDate: 2020-09-01T17:16:40 (DateTime - required)
ToDate: 2020-09-29T17:16:40 (DateTime - required)</textbox>
