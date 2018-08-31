---
swagger: "2.0"
x-collection-name: Oxford Dictionaries
x-complete: 0
info:
  title: Oxford Dictionaries Retrieve words that are similar
  description: Use this to retrieve words that are similar in meaning to the input
    word ([synonym](documentation/glossary?term=synonym)).
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
  /domains/{source_language}:
    get:
      summary: Lists available domains in a monolingual dataset
      description: Returns a list of the available [domains](documentation/glossary?term=domain)
        for a given monolingual language dataset.
      operationId: getDomainsSourceLanguage
      x-api-path-slug: domainssource-language-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: source_language
        description: IANA language code
      responses:
        200:
          description: OK
      tags:
      - Domains
      - Source
      - Language
  /entries/{source_language}/{word_id}/sentences:
    get:
      summary: Retrieve corpus sentences for a given word
      description: Use this to retrieve sentences extracted from  corpora which show
        how a word is used in the language. This is available for English and Spanish.
        For English, the sentences are linked to the correct [sense](documentation/glossary?term=sense)
        of the word in the dictionary. In Spanish, they are linked at the [headword](documentation/glossary?term=headword)
        level.
      operationId: getEntriesSourceLanguageWordSentences
      x-api-path-slug: entriessource-languageword-idsentences-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: source_language
        description: IANA language code
      responses:
        200:
          description: OK
      tags:
      - Entries
      - Source
      - Language
      - Word
      - Id
      - Sentences
  /entries/{source_lang}/{word_id}:
    get:
      summary: Retrieve dictionary information for a given word
      description: Use this to retrieve definitions, [pronunciations](documentation/glossary?term=pronunciation),
        example sentences, [grammatical information](documentation/glossary?term=grammaticalfeatures)
        and [word origins](documentation/glossary?term=etymology). It only works for
        dictionary [headwords](documentation/glossary?term=headword), so you may need
        to use the [Lemmatron](documentation/glossary?term=lemma) first if your input
        is likely to be an [inflected](documentation/glossary?term=inflection) form
        (e.g., 'swimming'). This would return the linked [headword](documentation/glossary?term=headword)
        (e.g., 'swim') which you can then use in the Entries endpoint. Unless specified
        using a region filter, the default lookup will be the Oxford Dictionary of
        English (GB).
      operationId: getEntriesSourceLangWord
      x-api-path-slug: entriessource-langword-id-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Entries
      - Source
      - Lang
      - Word
      - Id
  /entries/{source_lang}/{word_id}/antonyms:
    get:
      summary: Retrieve words that mean the opposite
      description: Retrieve words that are opposite in meaning to the input word ([antonym](documentation/glossary?term=thesaurus)).
      operationId: getEntriesSourceLangWordAntonyms
      x-api-path-slug: entriessource-langword-idantonyms-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Entries
      - Source
      - Lang
      - Word
      - Id
      - Antonyms
  /entries/{source_lang}/{word_id}/regions={region}:
    get:
      summary: Specify GB or US dictionary for English entry search
      description: USe this filter to restrict the lookup to either our Oxford Dictionary
        of English (GB) or New Oxford American Dictionary (US).
      operationId: getEntriesSourceLangWordRegionsRegion
      x-api-path-slug: entriessource-langword-idregionsregion-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: region
        description: Region filter parameter
      - in: path
        name: source_lang
        description: IANA language code
      responses:
        200:
          description: OK
      tags:
      - Entries
      - Source
      - Lang
      - Word
      - Id
      - Regions=region
  /entries/{source_lang}/{word_id}/synonyms:
    get:
      summary: Retrieve words that are similar
      description: Use this to retrieve words that are similar in meaning to the input
        word ([synonym](documentation/glossary?term=synonym)).
      operationId: getEntriesSourceLangWordSynonyms
      x-api-path-slug: entriessource-langword-idsynonyms-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Entries
      - Source
      - Lang
      - Word
      - Id
      - Synonyms
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