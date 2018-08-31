{
  "info": {
    "name": "Oxford Dictionaries Retrieve only pronunciations in entry search.",
    "_postman_id": "aba6172f-8e17-42df-ac4d-e673dd449d0d",
    "description": "Find available [dictionary entries](/glossary?tag=#entry&expand) for given word and language. Filter results by categories.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Domains",
      "item": [
        {
          "id": "0a3b82a0-36c8-450e-89c7-f515eee4fcc2",
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
              "id": "58908408-42bd-492c-b476-ad430cccfde2"
            }
          ]
        },
        {
          "id": "d01cd608-556c-4aed-85d6-06eccabebb43",
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
              "id": "73959644-0164-4e1c-a6c2-d8934749ebe0"
            }
          ]
        },
        {
          "id": "d84ec978-37f6-4b68-b6e2-6c51d24a3928",
          "name": "getDomainsSourceLanguageTargetLanguage",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "domains/:source_language/:target_language"
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
                  "value": "source_language",
                  "type": "string"
                },
                {
                  "id": "target_language",
                  "value": "target_language",
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
            "description": "Returns a list of the available [domains](/glossary?tag=#domains&expand) for a given bilingual language dataset."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1527c359-5bd0-4abb-8448-f39dd7b49987"
            }
          ]
        }
      ]
    },
    {
      "name": "Entries",
      "item": [
        {
          "id": "4fc956c0-6542-448d-aa59-50473de223dd",
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
              "id": "8043cf1b-f891-4e2f-8a60-3885504fe3aa"
            }
          ]
        },
        {
          "id": "6aef4de0-96db-4dae-acb9-eaa06716d416",
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
              "id": "46febe55-fd9c-49cf-82ef-eaf293ea8a35"
            }
          ]
        },
        {
          "id": "5ee7eea2-2aa2-49d9-be56-55835e5ed3e1",
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
              "id": "407f3b26-55fd-4c56-bce4-b09bc5d3b4da"
            }
          ]
        },
        {
          "id": "366b0d16-331e-493d-935a-0637ac03ebcf",
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
              "id": "be17d7ec-394e-41df-ada0-646be8d3255d"
            }
          ]
        },
        {
          "id": "99bad1f4-86b7-4c69-8408-0bfe9732ea3d",
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
              "id": "6eef3fb0-e5b1-435b-8c2f-20f12d1d0497"
            }
          ]
        },
        {
          "id": "401e35ed-7421-4c36-b250-6585811d27b1",
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
              "id": "405dc315-27aa-4fed-85c0-50d968be9947"
            }
          ]
        },
        {
          "id": "4e7f06ee-32d3-4ea3-9691-ef064a76fba8",
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
              "id": "f7ea7478-64a5-481f-b8a1-1567dcd62c44"
            }
          ]
        },
        {
          "id": "9cf7413a-6b7e-4c9e-aa39-7a061ccfa7bf",
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
              "id": "13243d02-87f0-420e-889f-05681c3db5f3"
            }
          ]
        },
        {
          "id": "5550a6e1-f1f2-447f-9c28-4b36a219190e",
          "name": "getEntriesSourceLangWordDefinitions",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "entries/:source_lang/:word_id/definitions"
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
            "description": "Find available [dictionary entries](/glossary?tag=#entry&expand) for given word and language. Filter results by categories."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5f0f70cf-3418-4792-8748-9d66b6580e8a"
            }
          ]
        },
        {
          "id": "c19d463b-0c41-4fe9-ac40-cae0b4d8aaa9",
          "name": "getEntriesSourceLangWordExamples",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "entries/:source_lang/:word_id/examples"
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
            "description": "Find available [dictionary entries](/glossary?tag=#entry&expand) for given word and language. Filter results by categories."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d93802e7-5910-4eec-bdd6-fc42516eb392"
            }
          ]
        },
        {
          "id": "c08aa1ef-7e0f-41da-9805-2248aa31dcce",
          "name": "getEntriesSourceLangWordPronunciations",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "entries/:source_lang/:word_id/pronunciations"
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
            "description": "Find available [dictionary entries](/glossary?tag=#entry&expand) for given word and language. Filter results by categories."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1148aba5-5118-4e41-a078-0cbafc7744f0"
            }
          ]
        }
      ]
    },
    {
      "name": "Filters",
      "item": [
        {
          "id": "5abbc172-5550-4d92-a707-91313fa563b9",
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
              "id": "9c5d60c9-c636-44f3-8d84-456a4049c773"
            }
          ]
        },
        {
          "id": "b017cc71-5ced-429f-b41b-a358aa452412",
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
              "id": "c280ec99-cf73-4a6c-90eb-d05a70850dab"
            }
          ]
        }
      ]
    },
    {
      "name": "GrammaticalFeatures",
      "item": [
        {
          "id": "e7f1047f-31a9-4d61-a091-e21fedbfbf86",
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
              "id": "fa35fe1e-0c77-4d6b-81e8-93e97989ddc7"
            }
          ]
        }
      ]
    },
    {
      "name": "Inflections",
      "item": [
        {
          "id": "962cf503-2417-404f-b9e5-08119a12a30e",
          "name": "getInflectionsSourceLangWord",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "inflections/:source_lang/:word_id"
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
            "description": "Use this to check if a word exists in the dictionary, or what 'root' form it links to (e.g., swimming > swim). The response tells you the possible [lemmas](documentation/glossary?term=lemma) for a given [inflected](documentation/glossary?term=inflection) word. This can then be combined with other endpoints to retrieve more information."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ec83bcfd-f7da-40da-8ba1-6457d2a96c12"
            }
          ]
        },
        {
          "id": "c6ade95d-66fb-4c24-864e-4da698aad6d5",
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
            "description": "Retrieve available [lemmas](documentation/glossary?term=lemma) for a given [inflected](documentation/glossary?term=inflection) wordform. Filter results by categories."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a731897e-7d22-4783-abd7-fdd1d5d1da3d"
            }
          ]
        }
      ]
    },
    {
      "name": "Languages",
      "item": [
        {
          "id": "e26b6746-9595-49ac-89f1-44d823ac3b5f",
          "name": "getLanguages",
          "request": {
            "url": "http://od-api-demo.oxforddictionaries.com:443/api/v1/languages?No Name=%7B%7D&sourceLanguage=%7B%7D&targetLanguage=%7B%7D",
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
            "description": "Returns a list of monolingual and bilingual language datasets available in the API"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7c3bf3b9-eb81-4efc-ad64-cff76d2d6a94"
            }
          ]
        }
      ]
    },
    {
      "name": "Lexicalcategories",
      "item": [
        {
          "id": "33247e8f-380c-4e9f-bbbd-14cb950fc0d3",
          "name": "getLexicalcategoriesLanguage",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "lexicalcategories/:language"
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
                  "id": "language",
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
            "description": "Returns a list of available [lexical categories](documentation/glossary?term=lexicalcategory) for a given language dataset."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "50f00dd3-01e8-4295-b750-3ce7f43043cb"
            }
          ]
        }
      ]
    },
    {
      "name": "Regions",
      "item": [
        {
          "id": "5f197903-a222-46b9-aff5-a6a86084d62c",
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
            "description": "Returns a list of the available [regions](documentation/glossary?term=regions) for a given monolingual language dataset."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e3a0262a-75c1-4ccf-9a68-55129f54dae7"
            }
          ]
        }
      ]
    },
    {
      "name": "Registers",
      "item": [
        {
          "id": "17e0589b-0ac5-42aa-a86b-23bc2364ac39",
          "name": "getRegistersSourceLanguage",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "registers/:source_language"
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
            "description": "Returns a list of the available [registers](documentation/glossary?term=registers) for a given monolingual language dataset."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7c5f181b-29e9-48f6-a696-cf1fbbb408fc"
            }
          ]
        },
        {
          "id": "2b431ccd-f029-40ce-b7e2-119714d4f7c6",
          "name": "getRegistersSourceRegisterLanguageTargetRegisterLanguage",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "registers/:source_register_language/:target_register_language"
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
                  "id": "source_register_language",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "target_register_language",
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
            "description": "Returns a list of the available [registers](documentation/glossary?term=registers) for a given bilingual language dataset."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7cd527d5-b9c3-4a9e-859c-e5eb6315bb39"
            }
          ]
        }
      ]
    },
    {
      "name": "Search",
      "item": [
        {
          "id": "98617c3a-64cf-4bd9-813b-b6ef88baa7ba",
          "name": "getSearchSourceLang",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "search/:source_lang"
              ],
              "port": "443",
              "query": [
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
                  "key": "q",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "regions",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "source_lang",
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
            "description": "Use this to retrieve possible [headword](documentation/glossary?term=headword) matches for a given string of text. The results are culculated using headword matching, fuzzy matching, and [lemmatization](documentation/glossary?term=lemma)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "858415c5-91ce-4ac2-8f3c-5f50e15f69d9"
            }
          ]
        },
        {
          "id": "9e59da76-bed5-4de2-955d-046617a4f0ca",
          "name": "getSearchSourceSearchLanguageTranslationsTargetSearchLanguage",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "search/:source_search_language/translations=:target_search_language"
              ],
              "port": "443",
              "query": [
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
                  "key": "q",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "regions",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "source_search_language",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "target_search_language",
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
            "description": "Use this to find matches in our translation dictionaries."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "55448df3-47af-4948-bd84-a4071721122e"
            }
          ]
        }
      ]
    },
    {
      "name": "Stats",
      "item": [
        {
          "id": "44502369-c37b-40c3-a3d2-8d07ddd0d6bf",
          "name": "getStatsFrequencyNgramsSourceLangCorpusNgramSize",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "stats/frequency/ngrams/:source_lang/:corpus/:ngram-size/"
              ],
              "port": "443",
              "query": [
                {
                  "key": "contains",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "format",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "maxDocumentFrequency",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "maxFrequency",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "minDocumentFrequency",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "minFrequency",
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
                  "key": "punctuation",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "tokens",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "corpus",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "ngram-size",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "source_lang",
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
            "description": "This endpoint returns frequencies of ngrams of size 1-4. That is the number of times a word (ngram size = 1) or words (ngram size > 1) appear in the corpus. Ngrams are case sensitive (\"I AM\" and \"I am\" will have different frequency) and frequencies are calculated per word (true case) so \"the book\" and \"the books\" are two different ngrams. The results can be filtered based on query parameters.   Parameters can be provided in PATH, GET or POST (form or json). The parameters in PATH are overriden by parameters in GET, POST and json (in that order). In PATH, individual options are separated by semicolon and values are separated by commas (where multiple values can be used).   Example for bigrams (ngram of size 2):\n* PATH: /tokens=a word,another word\n* GET: /?tokens=a word&tokens=another word\n* POST (json):\n\n  ```javascript\n    {\n        \"tokens\": [\"a word\", \"another word\"]\n    }\n  ```"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5005cf10-fa2a-48ae-a16e-cbb31f64a7bb"
            }
          ]
        },
        {
          "id": "d56a23b2-5750-4d5e-a8df-8f24e34e4e7d",
          "name": "getStatsFrequencyWordSourceLang",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "stats/frequency/word/:source_lang/"
              ],
              "port": "443",
              "query": [
                {
                  "key": "corpus",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "lemma",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "lexicalCategory",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "trueCase",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "wordform",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "source_lang",
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
            "description": "This endpoint provides the frequency of a given word. When multiple database records match the query parameters, the returned frequency is the sum of the individual frequencies. For example, if the query parameters are lemma=test, the returned frequency will include the verb \"test\", the noun \"test\" and the adjective \"test\" in all forms (Test, tested, testing, etc.)   If you are interested in the frequency of the word \"test\" but want to exclude other forms (e.g., tested) use the option trueCase=test. Normally, the word \"test\" will be spelt with a capital letter at the beginning of a sentence. The option trueCase will ignore this and it will count \"Test\" and \"test\" as the same token. If you are interested in frequencies of \"Test\" and \"test\", use the option wordform=test or wordform=Test. Note that trueCase is not just a lower case of the word as some words are genuinely spelt with a capital letter such as the word \"press\" in Oxford University Press.   Parameters can be provided in PATH, GET or POST (form or json). The parameters in PATH are overriden by parameters in GET, POST and json (in that order). In PATH, individual options are separated by semicolon and values are separated by commas (where multiple values can be used). Examples:\n* PATH: /lemma=test;lexicalCategory=noun\n* GET: /?lemma=test&lexicalCategory=noun\n* POST (json):\n\n  ```javascript\n    {\n      \"lemma\": \"test\",\n      \"lexicalCategory\": \"noun\"\n    }\n  ```\n\n One of the options wordform/trueCase/lemma/lexicalCategory has to be provided."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "de255d84-bdde-44b2-a869-b2f90ef99cfa"
            }
          ]
        },
        {
          "id": "1644dedd-ac93-4929-9800-facba5d3aeba",
          "name": "getStatsFrequencyWordsSourceLang",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "stats/frequency/words/:source_lang/"
              ],
              "port": "443",
              "query": [
                {
                  "key": "corpus",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "grammaticalFeatures",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "lemma",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "lexicalCategory",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "maxFrequency",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "maxNormalizedFrequency",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "minFrequency",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "minNormalizedFrequency",
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
                  "key": "sort",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "trueCase",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "wordform",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "source_lang",
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
            "description": "This endpoint provides a list of frequencies for a given word or words. Unlike the /word/ endpoint, the results are split into the smallest units.   To exclude a specific value, prepend it with the minus sign ('-'). For example, to get frequencies of the lemma 'happy' but exclude superlative forms (i.e., happiest) you could use options 'lemma=happy;grammaticalFeatures=-degreeType:superlative'.   Parameters can be provided in PATH, GET or POST (form or json). The parameters in PATH are overriden by parameters in GET, POST and json (in that order). In PATH, individual options are separated by semicolon and values are separated by commas (where multiple values can be used).   The parameters wordform/trueCase/lemma/lexicalCategory also exist in a plural form, taking a lists of items. Examples:\n* PATH: /wordforms=happy,happier,happiest\n* GET: /?wordforms=happy&wordforms=happier&wordforms=happiest\n* POST (json):\n```javascript\n  {\n    \"wordforms\": [\"happy\", \"happier\", \"happiest\"]\n  }\n```\n Aside from individual frequency requests, users can also post a list of items for which they would like to get frequencies. The list has to be uploaded in json and the required fields are \"items\" and \"collate\".   The field \"items\" is a list of items for which you want the frequencies. The content of the items depends on the option for \"collate\". The value of \"collate\" should be a list of \"columns\" that the items contain. The list is limited to combinations of \"wordform\", \"lemma\", \"trueCase\" and \"lexicalCategory\". The fields that are listed in the \"collate\" options have to be present in each item. Here are some examples of queries:\n* ### Get frequencies of provided wordforms:\n```javascript\n  {\n      \"collate\": [\"wordform\"],\n      \"items\": [{\"wordform\": \"test\"}, {\"wordform\": \"Test\"}]\n  }\n```\n* ### Get frequencies of provided lemmas:\n```javascript\n  {\n      \"collate\": [\"lemma\"],\n      \"items\": [{\"lemma\": \"test\"}, {\"lemma\": \"Test\"}]\n  }\n```\n* ### Get frequencies of provided lemmas per lexical category:\n```javascript\n  {\n      \"collate\": [\"lemma\", \"lexicalCategory\"],\n      \"items\": [\n          {\"lemma\": \"test\", \"lexicalCategory\": \"verb\"},\n          {\"lemma\": \"test\", \"lexicalCategory\": \"noun\"}\n      ]\n  }\n```"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "05c6ac3a-6233-4841-bb28-8b9d9a7b0a0b"
            }
          ]
        }
      ]
    },
    {
      "name": "Wordlist",
      "item": [
        {
          "id": "3e7ab2c4-7321-4e02-bc76-423585c343ea",
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
            "description": "Use this to apply more complex filters to the [list of words](documentation/glossary?term=wordlist). For example, you may only want to filter out words for which all [senses](documentation/glossary?term=sense) match the filter, or only its 'prime sense'. You can also filter by word length or match by substring (prefix)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1d2d9263-597b-48f7-a1db-464fc3cdcda1"
            }
          ]
        },
        {
          "id": "f8c8149a-335c-4a04-a395-e9f20dd5ba01",
          "name": "getWordlistSourceLangFiltersBasic",
          "request": {
            "url": {
              "protocol": "http",
              "host": "od-api-demo.oxforddictionaries.com",
              "path": [
                "api",
                "v1",
                "wordlist/:source_lang/:filters_basic"
              ],
              "port": "443",
              "query": [
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
                }
              ],
              "variable": [
                {
                  "id": "filters_basic",
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
            "description": "Use this to retrieve a [list of words](documentation/glossary?term=wordlist) for particular [domain](documentation/glossary?term=domain), [lexical category](documentation/glossary?term=lexicalcategory), [register](documentation/glossary?term=registers) and/or [region](documentation/glossary?term=regions). View the full list of possible filters using the filters Utility endpoint.  The response only includes [headwords](documentation/glossary?term=headword), not all their possible [inflections](documentation/glossary?term=inflection). If you require a full [wordlist](documentation/glossary?term=wordlist) including [inflected forms](documentation/glossary?term=inflection), contact us and we can help."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8d8aa5f8-99c3-415d-bf51-6c3f1b3711a7"
