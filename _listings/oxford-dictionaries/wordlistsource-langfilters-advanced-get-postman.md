{
  "info": {
    "name": "Oxford Dictionaries Retrieve list of words for category with advanced options",
    "_postman_id": "dd279746-abd9-4c4c-a8ea-68eb6e52d047",
    "description": "Use this to apply more complex filters to the [list of words](documentation/glossary?term=wordlist). For example, you may only want to filter out words for which all [senses](documentation/glossary?term=sense) match the filter, or only its 'prime sense'. You can also filter by word length or match by substring (prefix).",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Entries",
      "item": [
        {
          "id": "3f380749-1f97-4fd0-a09f-0c4b92851f14",
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
              "id": "5c7c6329-66bf-404f-be37-772725b9a715"
            }
          ]
        }
      ]
    },
    {
      "name": "Filters",
      "item": [
        {
          "id": "bb2039b1-e0d5-43b3-84a0-ba7a339a44be",
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
              "id": "5731b5c1-c5ea-4688-90f4-60862c86bd1d"
            }
          ]
        },
        {
          "id": "210592dc-97e1-4c26-81ee-3b852de906c7",
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
              "id": "c6a4e6b0-ced3-40b6-8a26-09923358bbb8"
            }
          ]
        }
      ]
    },
    {
      "name": "Inflections",
      "item": [
        {
          "id": "fdf8b124-7105-4d22-9464-e698f1f57830",
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
              "id": "4b9cc802-8e61-47aa-a1f3-57a27de0296b"
            }
          ]
        }
      ]
    },
    {
      "name": "Wordlist",
      "item": [
        {
          "id": "75885803-1eb5-488e-8a2c-e97063722052",
          "name": "getWordlistSourceLangFiltersAdvanced",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "wordlist/:source_lang/:filters_advanced"
              ],
              "port": "443",
              "query": [
                {
                  "key": "exact",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "exclude",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "exclude_prime_senses",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "exclude_senses",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "offset",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "prefix",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "word_length",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "filters_advanced",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "source_lang",
                  "value": "source_lang",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Use this to apply more complex filters to the [list of words](documentation/glossary?term=wordlist). For example, you may only want to filter out words for which all [senses](documentation/glossary?term=sense) match the filter, or only its 'prime sense'. You can also filter by word length or match by substring (prefix)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b78ff374-5c47-430c-bc06-17a1a3754ee6"
            }
          ]
        }
      ]
    }
  ]
}