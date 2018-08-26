{
  "info": {
    "name": "Oxford Dictionaries Lists available grammatical features in a dataset",
    "_postman_id": "a45da7f1-3509-4e05-a153-4d5b98fd50c7",
    "description": "Returns a list of the available [grammatical features](documentation/glossary?term=grammaticalfeatures) for a given language dataset.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Domains",
      "item": [
        {
          "id": "73da22aa-af7c-432d-9c07-d45252e9d302",
          "name": "getDomainsSourceDomainsLanguageTargetDomainsLanguage",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "domains/:source_domains_language/:target_domains_language"
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
                  "id": "source_domains_language",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "target_domains_language",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of the available [domains](documentation/glossary?term=domain) for a given bilingual language dataset."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7a997f67-1b76-4ee0-b5ad-e39ce11a64c3"
            }
          ]
        },
        {
          "id": "bd7a902d-b614-4eb9-8dd0-fdb08b8852b4",
          "name": "getDomainsSourceLanguage",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "domains/:source_language"
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
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of the available [domains](documentation/glossary?term=domain) for a given monolingual language dataset."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a7b98c79-5607-4308-8124-fdb4798d4a38"
            }
          ]
        }
      ]
    },
    {
      "name": "Entries",
      "item": [
        {
          "id": "ac3d691d-7714-4873-a3b8-f3edee404a16",
          "name": "getEntriesSourceLanguageWordSentences",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "entries/:source_language/:word_id/sentences"
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
                },
                {
                  "id": "word_id",
                  "value": "word_id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Use this to retrieve sentences extracted from  corpora which show how a word is used in the language. This is available for English and Spanish. For English, the sentences are linked to the correct [sense](documentation/glossary?term=sense) of the word in the dictionary. In Spanish, they are linked at the [headword](documentation/glossary?term=headword) level."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ca363c37-0f2f-43c9-8d67-34ecf2081ca6"
            }
          ]
        },
        {
          "id": "62541c6b-52fd-48be-9763-53ab2847b394",
          "name": "getEntriesSourceLangWord",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "entries/:source_lang/:word_id"
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
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Use this to retrieve definitions, [pronunciations](documentation/glossary?term=pronunciation), example sentences, [grammatical information](documentation/glossary?term=grammaticalfeatures) and [word origins](documentation/glossary?term=etymology). It only works for dictionary [headwords](documentation/glossary?term=headword), so you may need to use the [Lemmatron](documentation/glossary?term=lemma) first if your input is likely to be an [inflected](documentation/glossary?term=inflection) form (e.g., 'swimming'). This would return the linked [headword](documentation/glossary?term=headword) (e.g., 'swim') which you can then use in the Entries endpoint. Unless specified using a region filter, the default lookup will be the Oxford Dictionary of English (GB)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ce01ec96-7a81-42a4-8bd8-926fc2a6f41f"
            }
          ]
        },
        {
          "id": "5793462e-f3f3-470d-8c67-405ba585c0d1",
          "name": "getEntriesSourceLangWordAntonyms",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "entries/:source_lang/:word_id/antonyms"
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
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve words that are opposite in meaning to the input word ([antonym](documentation/glossary?term=thesaurus))."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "32bf2694-6d7f-43e4-b9ee-bce2a1018a4a"
            }
          ]
        },
        {
          "id": "df4fa582-10ce-490b-886e-748f465e4b27",
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
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
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
              "id": "cb0d0c73-631b-442b-85ce-c54df296bae4"
            }
          ]
        },
        {
          "id": "2e4d3afb-a15a-4da0-a78f-0c4617395896",
          "name": "getEntriesSourceLangWordSynonyms",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "entries/:source_lang/:word_id/synonyms"
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
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Use this to retrieve words that are similar in meaning to the input word ([synonym](documentation/glossary?term=synonym))."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5980a6f5-53ba-4b94-b57e-0c3aa61872d3"
            }
          ]
        },
        {
          "id": "144d67ba-75ab-4784-94fc-636007181880",
          "name": "getEntriesSourceLangWordSynonyms;antonyms",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "entries/:source_lang/:word_id/synonyms;antonyms"
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
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve available [synonyms](documentation/glossary?term=thesaurus) and [antonyms](documentation/glossary?term=thesaurus) for a given word and language."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "55bdfa3a-6e6f-4e56-b8be-741dbb68ed8b"
            }
          ]
        },
        {
          "id": "90baea51-90ee-4d46-8a8a-d3f063a85591",
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
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
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
              "id": "9a2f4658-ce68-440f-8382-dbfcd21140c1"
            }
          ]
        },
        {
          "id": "24e11843-48e1-4bfe-946d-9141be5129d3",
          "name": "getEntriesSourceTranslationLanguageWordTranslationsTargetTranslationLanguage",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "entries/:source_translation_language/:word_id/translations=:target_translation_language"
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
                  "id": "source_translation_language",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "target_translation_language",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "word_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Use this to return translations for a given word. In the event that a word in the dataset does not have a direct translation, the response will be a [definition](documentation/glossary?term=entry) in the target language."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "206660af-05ca-4bc3-baa0-a20ff3e6a47e"
            }
          ]
        }
      ]
    },
    {
      "name": "Filters",
      "item": [
        {
          "id": "9140f2c4-685a-4b8a-a5d5-036121cb6698",
          "name": "getFilters",
          "request": {
            "url": "http://od-api-demo.oxforddictionaries.com:443/api/v1/filters?No Name=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
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
              "id": "3bff4899-f937-4334-8bb8-2669d92b61f2"
            }
          ]
        },
        {
          "id": "1bff7767-ecba-41ec-81b6-3c0b022d48e1",
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
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
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
              "id": "dc1804fc-6ba1-44db-bfc5-53d0f445fa11"
            }
          ]
        }
      ]
    },
    {
      "name": "GrammaticalFeatures",
      "item": [
        {
          "id": "c5f93e4a-ceac-4a03-becf-aa2d8b9aadb6",
          "name": "getGrammaticalfeaturesSourceLanguage",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "grammaticalFeatures/:source_language"
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
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of the available [grammatical features](documentation/glossary?term=grammaticalfeatures) for a given language dataset."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2da3b308-7246-41bf-a384-e1be8d6bb84e"
            }
          ]
        }
      ]
    }
  ]
}