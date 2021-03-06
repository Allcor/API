## Sample Search [/brapi/v1/samples-search]

Used to retrieve list of Samples from a Sample Tracking system based on some search criteria.

### Get Sample Search [GET /brapi/v1/samples-search{?sampleDbId}{?observationUnitDbId}{?plateDbId}{?germplasmDbId}]
+ Parameters
    + sampleDbId (optional, string, `Unique-Plant-SampleID-1`) ... the internal DB id for a sample
    + observationUnitDbId (optional, string, `abc123`) ... the internal DB id for an observation unit where a sample was taken from
    + plateDbId (optional, string, `PlateID-123`) ... the internal DB id for a plate of samples 
    + germplasmDbId (optional, string, `def456`) ... the internal DB id for a germplasm
    
+ Response 200 (application/json)

        {
            "metadata": {
                "pagination" : { 
                    "pageSize":1000, 
                    "currentPage":0, 
                    "totalCount":2, 
                    "totalPages":1 
                },
                "status" : [],
                "datafiles": []
            },
            "result": {
                "data": [
                    {
                          "sampleDbId": "Unique-Plant-SampleID-1",
                          "observationUnitDbId": "abc123",
                          "germplasmDbId": "def456",
                          "studyDbId": "StudyId-123",
                          "plotDbId": "PlotId-123",
                          "plantDbId" : "PlantID-123",
                          "plateDbId": "PlateID-123",
                          "plateIndex": 0,
                          "takenBy": "Mr. Technician",
                          "sampleTimestamp": "2016-07-27T14:43:22+0100",
                          "sampleType" : "TypeOfSample",
                          "tissueType" : "TypeOfTissue",
                          "notes": "Cut from infected leaf"
                      },{
                          "sampleDbId": "Unique-Plant-SampleID-2",
                          "observationUnitDbId": "a1b2c3",
                          "germplasmDbId": "def456",
                          "studyDbId": "StudyId-123",
                          "plotDbId": "PlotId-123",
                          "plantDbId" : "PlantID-123",
                          "plateDbId": "PlateID-123",
                          "plateIndex": 0,
                          "takenBy": "Mr. Technician",
                          "sampleTimestamp": "2016-07-27T14:43:22+0100",
                          "sampleType" : "TypeOfSample",
                          "tissueType" : "TypeOfTissue",
                          "notes": "Cut from infected leaf"
                      }
                  ]
            }
        }
        
