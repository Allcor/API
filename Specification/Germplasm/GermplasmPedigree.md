## Germplasm Pedigree [/brapi/v1/germplasm/{germplasmDbId}/pedigree]
Scope: CORE. Status: ACCEPTED.  
Implementation target date: PAG2016
Implemented by: Germinate, Tripal Brapi Module, Cassavabase (without notation option)

###### Response data types
|Variable|Datatype|Description|Required|  
|------|------|------|:-----:|
|metadata|object|pagination, status|Y|
|pagination|object|pageSize, currentPage, totalCount, totalPages|Y|
|status|list|code, message|Y|
|germplasmDbId|string|Internal db identifier|Y|
|defaultDisplayName|string|A string representing the germplasm that will be meaningful to the user|Y|
|pedigree|string|Cross name with optional selection history.|Y|
|**Deprecated** parent1Id|string|**Use parent1DbId**||
|**Deprecated** parent2Id|string|**Use parent2DbId**||
|parent1DbId|string|germplasmDbId of parent1||
|parent2DbId|string|germplasmDbId of parent2||

(http://wheat.pw.usda.gov/ggpages/gopher/administration/Template%20for%20Germplasm%20records.html) or [Lamacraft] (http://link.springer.com/article/10.1007%2FBF00021556).  

### Germplasm pedigree by id [GET /brapi/v1/germplasm/{germplasmDbId}/pedigree{?notation}]
+ Parameters
   + germplasmDbId (required, string, `382`) ... the internal id of the germplasm
   + notation (optional, string, `purdy`) ... text representation of the pedigree
+ Response 200 (application/json)
    
        { 
            "metadata" : {
                "pagination": {
                    "pageSize":0, 
                    "currentPage":0, 
                    "totalCount":0, 
                    "totalPages":0 
                },
                "status": [],
                "datafiles": []
            }
            "result" : {
                "germplasmDbId": "382",
                "defaultDisplayName": "Pahang",
                "pedigree" : "Cree / Bonanza",
                "parent1DbId" : "166",
                "parent2DbId" : "143"
            }
        }

