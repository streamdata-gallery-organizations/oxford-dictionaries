{
  "info": {
    "name": "Oxford Dictionaries Lists available lexical categories in a dataset",
    "_postman_id": "7cd459b5-47c3-4cb1-a0a8-7068e1a9215a",
    "description": "Returns a list of available [lexical categories](documentation/glossary?term=lexicalcategory) for a given language dataset.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Lexicalcategories",
      "item": [
        {
          "id": "655a5a5e-61b9-4d44-9852-8e62646b861e",
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
              "id": "de59118b-160b-4d79-b155-b91994f836eb"
            }
          ]
        }
      ]
    }
  ]
}