{
  "info": {
    "name": "Oxford Dictionaries Lists available regions in a monolingual dataset",
    "_postman_id": "c1b0b17b-206b-460e-b8ad-14b41f5dbc9b",
    "description": "Returns a list of the available [regions](documentation/glossary?term=regions) for a given monolingual language dataset.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Entries",
      "item": [
        {
          "id": "9eec8dcf-8fa1-45fe-9f0b-9d2c88530bc9",
          "name": "getEntriesSourceLangWordRegionsRegion",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "entries/:source_lang/:word_id/regions=:region"
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
                  "id": "region",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "source_lang",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "word_id",
                  "value": "word_id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "USe this filter to restrict the lookup to either our Oxford Dictionary of English (GB) or New Oxford American Dictionary (US)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "82bf6afc-85b9-4446-885e-3ea9af31047b"
            }
          ]
        }
      ]
    },
    {
      "name": "Regions",
      "item": [
        {
          "id": "f8e884f1-a11d-4b71-909b-f8e5d1b6d383",
          "name": "getRegionsSourceLanguage",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "regions/:source_language"
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
                  "id": "source_language",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of the available [regions](documentation/glossary?term=regions) for a given monolingual language dataset."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "62919a06-8e3e-45d0-a6bd-ae3738c497ff"
            }
          ]
        }
      ]
    }
  ]
}