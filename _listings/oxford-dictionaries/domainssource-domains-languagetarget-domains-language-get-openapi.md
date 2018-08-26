---
swagger: "2.0"
x-collection-name: Oxford Dictionaries
x-complete: 0
info:
  title: Oxford Dictionaries Lists available domains in a bilingual dataset
  description: Returns a list of the available [domains](documentation/glossary?term=domain)
    for a given bilingual language dataset.
  termsOfService: http://helloreverb.com/terms/
  version: 1.8.0
host: od-api-demo.oxforddictionaries.com:443
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /domains/{source_domains_language}/{target_domains_language}:
    get:
      summary: Lists available domains in a bilingual dataset
      description: Returns a list of the available [domains](documentation/glossary?term=domain)
        for a given bilingual language dataset.
      operationId: getDomainsSourceDomainsLanguageTargetDomainsLanguage
      x-api-path-slug: domainssource-domains-languagetarget-domains-language-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: source_domains_language
        description: IANA language code
      - in: path
        name: target_domains_language
        description: IANA language code
      responses:
        200:
          description: OK
      tags:
      - Domains
      - Source
      - Domains
      - Language
      - Target
      - Domains
      - Language
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---