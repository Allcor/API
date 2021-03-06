## Germplasm attribute values by germplasmDbId [/brapi/v1/germplasm/{germplasmDbId}/attributes]

Status: ACCEPTED.]

### Germplasm attribute values [GET /brapi/v1/germplasm/{germplasmDbId}/attributes{?attributeList}{?pageSize}{?page}]
Values for all attributes by default.
+ Parameters
    + germplasmDbId (required, string, `993`) ... The germplasm characterized
    + attributeList (optional, array, `123,456,789`) ... Restrict the response to only the listed attributeDbIds.
    + pageSize (optional, integer, `1000`) ... The size of the pages to be returned. Default is `1000`.
    + page (optional, integer, `0`) ... Which result page is requested. The page indexing starts at 0 (the first page is 'page'= 0). Default is `0`.

+ Response 200 (application/json)

        {
            "metadata" : {
                "pagination": {
                    "pageSize": 1000,
                    "currentPage": 0,
                    "totalCount": 1,
                    "totalPages": 1
                },
                "status": [],
                "datafiles": []
            },
            "result" : [
                {
                    "germplasmDbId": "993",
                    "data": [
                        {
                            "attributeDbId": "1",
                            "attributeName": "Rht-B1b",
                            "attributeCode": "RHT",
                            "value": "Present", 
                            "determinedDate": "2007-05-28"
                        }
                    ]
                }
            ]
        }
