{
  "info": {
    "name": "Oxford Dictionaries Apply optional filters to Lemmatron response",
    "_postman_id": "072a2896-466f-467a-af0a-ec6c79a7fedf",
    "description": "Retrieve available [lemmas](documentation/glossary?term=lemma) for a given [inflected](documentation/glossary?term=inflection) wordform. Filter results by categories.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Entries",
      "item": [
        {
          "id": "d12acebb-244a-484f-a88b-88baf77deb0b",
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
              "id": "88978653-4f1a-4e92-a829-0c7a0f54b2c5"
            }
          ]
        }
      ]
    },
    {
      "name": "Filters",
      "item": [
        {
          "id": "7c90ac2e-5c24-45e3-9cb4-842ad8bb8c63",
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
              "id": "966f9ecb-8649-4e29-8a6f-68d9d3c61570"
            }
          ]
        },
        {
          "id": "a2930d0b-ab09-4493-9399-724d2eb9250e",
          "name": "getFiltersEndpoint",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "filters/:endpoint"
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
                  "id": "endpoint",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of all the valid filters for a given endpoint to construct API calls."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "211ea55e-9140-427b-a59f-44847bf4cd5e"
            }
          ]
        }
      ]
    },
    {
      "name": "Inflections",
      "item": [
        {
          "id": "7be66ecb-e4cf-46d4-9491-513d4567cfdb",
          "name": "getInflectionsSourceLangWordFilters",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "inflections/:source_lang/:word_id/:filters"
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
                  "id": "word_id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "source_lang",
                  "value": "source_lang",
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
            "description": "Retrieve available [lemmas](documentation/glossary?term=lemma) for a given [inflected](documentation/glossary?term=inflection) wordform. Filter results by categories."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9bf30d46-4ff5-4dac-a349-6302de9c3937"
            }
          ]
        }
      ]
    }
  ]
}