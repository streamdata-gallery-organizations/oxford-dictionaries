{
  "info": {
    "name": "Oxford Dictionaries Specify GB or US dictionary for English entry search",
    "_postman_id": "856477b4-3bd4-4672-81eb-0e9e1fa7ebd0",
    "description": "USe this filter to restrict the lookup to either our Oxford Dictionary of English (GB) or New Oxford American Dictionary (US).",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Entries",
      "item": [
        {
          "id": "8cf7a81a-a63e-4ef1-9dfe-2715efe09b4d",
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
              "id": "8daeff41-5cd2-4862-8da0-60642c062ca9"
            }
          ]
        }
      ]
    }
  ]
}