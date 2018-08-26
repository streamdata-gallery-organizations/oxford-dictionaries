{
  "info": {
    "name": "Oxford Dictionaries Lists available filters",
    "_postman_id": "0d72ebf3-24b6-4459-bd33-21b602d7b979",
    "description": "Returns a list of all the valid filters to construct API calls.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Entries",
      "item": [
        {
          "id": "b553a2e4-0c4f-49cc-9952-897db0eb8e2a",
          "name": "getEntriesSourceLangWordFilters",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "entries/:source_lang/:word_id/:filters"
              ],
              "port": "443",
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "source_lang",
                  "value": "source_lang",
                  "type": "string"
                },
                {
                  "id": "word_id",
                  "value": "word_id",
                  "type": "string"
                },
                {
                  "id": "filters",
                  "value": "filters",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Use filters to limit the [entry](documentation/glossary?term=entry) information that is returned. For example, you may only require definitions and not everything else, or just [pronunciations](documentation/glossary?term=pronunciation). The full list of filters can be retrieved from the filters Utility endpoint. You can also specify values within the filter using '='. For example 'grammaticalFeatures=singular'. Filters can also be combined using a semicolon."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "42e14510-f5a7-4c8d-b20e-9768bfb9f9b3"
            }
          ]
        }
      ]
    },
    {
      "name": "Filters",
      "item": [
        {
          "id": "d3ec3f04-e560-44b1-a09e-32b7f6f9285b",
          "name": "getFilters",
          "request": {
            "url": "http://od-api-demo.oxforddictionaries.com:443/api/v1/filters?No Name=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of all the valid filters to construct API calls."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "aaf97ab0-8297-4e30-bc42-54df41438aa9"
            }
          ]
        }
      ]
    }
  ]
}