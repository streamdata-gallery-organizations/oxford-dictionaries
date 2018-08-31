{
  "info": {
    "name": "Oxford Dictionaries Retrieve only example sentences in entry search.",
    "_postman_id": "9aa119a3-a3c4-4605-adec-a9fc214c6b27",
    "description": "Find available [dictionary entries](/glossary?tag=#entry&expand) for given word and language. Filter results by categories.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Domains",
      "item": [
        {
          "id": "ae1ff28d-82f8-47e7-8bda-bf7032fdd84c",
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
              "id": "bbbe6935-089a-4a82-a389-918375b789f1"
            }
          ]
        },
        {
          "id": "cf27b2f5-e04e-4df0-a833-363028148529",
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
              "id": "0694e1f7-461f-4025-af0b-bd41494699eb"
            }
          ]
        },
        {
          "id": "761318c0-0bc1-4968-80c4-e546bddf03c9",
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
              "id": "8ac7e174-aaa2-46a0-80dc-4a6ec0dbe093"
            }
          ]
        }
      ]
    },
    {
      "name": "Entries",
      "item": [
        {
          "id": "ee0a798d-4245-4ddb-9f4b-ec2ac0a6d481",
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
              "id": "584d45ab-fc23-4fe8-bc1c-8e8d21508cac"
            }
          ]
        },
        {
          "id": "b31e72cb-72d2-496c-9e86-bf832c084bc9",
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
              "id": "d1c6c3b4-49ae-4e3c-a795-bc449b8171f4"
            }
          ]
        },
        {
          "id": "996f99b2-ae56-4306-a617-e795c6d76de4",
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
              "id": "e7912df3-61d3-458a-9069-df78ad9e5fd7"
            }
          ]
        },
        {
          "id": "5292d6c9-ecae-44d2-8321-d9e3f05bb690",
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
              "id": "1f40bb5d-72d2-4e24-9703-e66e37fa0c41"
            }
          ]
        },
        {
          "id": "064fbd8d-d737-44e5-a0fe-f94e78bbdf64",
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
              "id": "7cbada5d-f834-408b-9674-74a759205bd0"
            }
          ]
        },
        {
          "id": "627e1274-59ae-419f-8013-3efea992ea22",
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
              "id": "6fc3d94c-9210-4157-8965-aaf4d1b866c6"
            }
          ]
        },
        {
          "id": "83a80b94-950f-471b-b008-cd5eeba7f358",
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
              "id": "fd62b9d8-030c-4a9a-91bd-3b8806654629"
            }
          ]
        },
        {
          "id": "fa7e1435-7f55-4272-84b3-2533c84459cf",
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
              "id": "bf37bb9e-bdc3-44f9-9bfd-c9afd01c50d1"
            }
          ]
        },
        {
          "id": "df6a5da5-a325-4df9-95d9-c1e76cb412ee",
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
              "id": "4c52a258-ad24-4587-9f5b-a072bc6aded0"
            }
          ]
        },
        {
          "id": "06d6cb1d-5ad3-4aae-9206-440ed82ed62b",
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
              "id": "5899559a-eac0-47fa-9cc5-e024d85c515d"
            }
          ]
        }
      ]
    },
    {
      "name": "Filters",
      "item": [
        {
          "id": "2c7afd24-83f3-49c3-b685-7a3412bdd758",
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
              "id": "dbfb0c0b-3cd6-4dbb-8ec4-11d6053a0652"
            }
          ]
        },
        {
          "id": "78a82788-0abf-4e6a-830a-3d95e114040b",
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
              "id": "8754086a-e2ba-43d0-a1d8-e1682775a04a"
            }
          ]
        }
      ]
    },
    {
      "name": "GrammaticalFeatures",
      "item": [
        {
          "id": "e2ddb66e-3f52-4879-88d0-1398a080b3c5",
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
              "id": "1dfe857b-011d-4205-91c4-2c0e79997f2c"
            }
          ]
        }
      ]
    },
    {
      "name": "Inflections",
      "item": [
        {
          "id": "633268bb-ff68-45b7-a672-d718be64af58",
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
              "id": "bbf8b174-1154-4751-8910-0feca55f8c1c"
            }
          ]
        },
        {
          "id": "984ce459-17eb-4a5d-a926-c1b13e462ff7",
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
              "id": "7898ad35-bb21-41ae-8794-153c4d271896"
            }
          ]
        }
      ]
    },
    {
      "name": "Languages",
      "item": [
        {
          "id": "7edfe5cb-243f-4301-920b-222663a1a933",
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
              "id": "01c2d9f4-01d0-4824-8c61-ac9783916c50"
            }
          ]
        }
      ]
    },
    {
      "name": "Lexicalcategories",
      "item": [
        {
          "id": "7753da72-0460-40bc-9715-adcd96658788",
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
              "id": "60f247ba-6dd2-4aaa-98f4-fbdbc831da41"
            }
          ]
        }
      ]
    },
    {
      "name": "Regions",
      "item": [
        {
          "id": "dfff9328-dc77-4389-acc8-c15de414e7ab",
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
              "id": "0347a825-ef96-47d8-aee9-70beec778963"
            }
          ]
        }
      ]
    },
    {
      "name": "Registers",
      "item": [
        {
          "id": "d05ad830-2631-414d-92a0-873e51855325",
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
              "id": "06dcd7b2-fcd9-45dc-993f-0ac7f3707b21"
            }
          ]
        },
        {
          "id": "52311d2d-9898-4968-b65d-0f2a44690ba2",
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
              "id": "cd4f0f5d-7c24-41b5-a618-dc7a3bd12c02"
            }
          ]
        }
      ]
    },
    {
      "name": "Search",
      "item": [
        {
          "id": "124a6ab0-0ac3-4acc-b2be-1454bd4dd05f",
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
              "id": "ad09773c-cd04-4411-a6cc-c9258990190f"
            }
          ]
        },
        {
          "id": "1b0244da-20e9-4008-a3a2-17f3c5d724a6",
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
              "id": "e7b489f7-93e4-435c-b94f-e8e43dd38f38"
            }
          ]
        }
      ]
    },
    {
      "name": "Stats",
      "item": [
        {
          "id": "3d8ba8f8-0c49-4fe9-8fcc-3aa64c26fc03",
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
              "id": "bb1fa526-7bd8-4f0d-aef9-eef2e577f089"
            }
          ]
        },
        {
          "id": "2ca5dfe0-4c3c-4b06-805d-e212930ee82d",
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
              "id": "94501594-91e4-4cfe-868f-1a813f651a81"
            }
          ]
        },
        {
          "id": "9b14d024-f2c6-4c6a-bb63-8349f3f42b7e",
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
              "id": "5a60b146-a576-4700-85dd-ec3291cde46b"
            }
          ]
        }
      ]
    },
    {
      "name": "Wordlist",
      "item": [
        {
          "id": "afa30c04-dc75-4fbb-a6ea-9606f62694ad",
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
              "id": "3744c5bd-4cf5-4106-a9ef-facafc5e3288"
            }
          ]
        },
        {
          "id": "b9635e10-157d-4129-9e0b-26bec8d96365",
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
              "id": "2005e502-b912-409f-bc63-b2575be536c3"
            }
          ]
        }
      ]
    }
  ]
}