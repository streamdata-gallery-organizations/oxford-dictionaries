---
swagger: "2.0"
x-collection-name: Oxford Dictionaries
x-complete: 0
info:
  title: Oxford Dictionaries Check a word exists in the dictionary and retrieve its
    root form
  description: Use this to check if a word exists in the dictionary, or what 'root'
    form it links to (e.g., swimming > swim). The response tells you the possible
    [lemmas](documentation/glossary?term=lemma) for a given [inflected](documentation/glossary?term=inflection)
    word. This can then be combined with other endpoints to retrieve more information.
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
  /entries/{source_lang}/{word_id}/synonyms;antonyms:
    get:
      summary: Retrieve synonyms and antonyms for a given word
      description: Retrieve available [synonyms](documentation/glossary?term=thesaurus)
        and [antonyms](documentation/glossary?term=thesaurus) for a given word and
        language.
      operationId: getEntriesSourceLangWordSynonyms;antonyms
      x-api-path-slug: entriessource-langword-idsynonymsantonyms-get
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
      - Synonyms;antonyms
  /entries/{source_lang}/{word_id}/{filters}:
    get:
      summary: Apply filters to response
      description: Use filters to limit the [entry](documentation/glossary?term=entry)
        information that is returned. For example, you may only require definitions
        and not everything else, or just [pronunciations](documentation/glossary?term=pronunciation).
        The full list of filters can be retrieved from the filters Utility endpoint.
        You can also specify values within the filter using '='. For example 'grammaticalFeatures=singular'.
        Filters can also be combined using a semicolon.
      operationId: getEntriesSourceLangWordFilters
      x-api-path-slug: entriessource-langword-idfilters-get
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
      - Filters
  /entries/{source_translation_language}/{word_id}/translations={target_translation_language}:
    get:
      summary: Retrieve translation for a given word
      description: Use this to return translations for a given word. In the event
        that a word in the dataset does not have a direct translation, the response
        will be a [definition](documentation/glossary?term=entry) in the target language.
      operationId: getEntriesSourceTranslationLanguageWordTranslationsTargetTranslationLanguage
      x-api-path-slug: entriessource-translation-languageword-idtranslationstarget-translation-language-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: source_translation_language
        description: IANA language code
      - in: path
        name: target_translation_language
        description: IANA language code
      - in: path
        name: word_id
        description: The source word
      responses:
        200:
          description: OK
      tags:
      - Entries
      - Source
      - Translation
      - Language
      - Word
      - Id
      - Translations=target
      - Translation
      - Language
  /filters:
    get:
      summary: Lists available filters
      description: Returns a list of all the valid filters to construct API calls.
      operationId: getFilters
      x-api-path-slug: filters-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Filters
  /filters/{endpoint}:
    get:
      summary: Lists available filters for specific endpoint
      description: Returns a list of all the valid filters for a given endpoint to
        construct API calls.
      operationId: getFiltersEndpoint
      x-api-path-slug: filtersendpoint-get
      parameters:
      - in: path
        name: endpoint
        description: Name of the endpoint
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Filters
      - Endpoint
  /grammaticalFeatures/{source_language}:
    get:
      summary: Lists available grammatical features in a dataset
      description: Returns a list of the available [grammatical features](documentation/glossary?term=grammaticalfeatures)
        for a given language dataset.
      operationId: getGrammaticalfeaturesSourceLanguage
      x-api-path-slug: grammaticalfeaturessource-language-get
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
      - GrammaticalFeatures
      - Source
      - Language
  /inflections/{source_lang}/{word_id}:
    get:
      summary: Check a word exists in the dictionary and retrieve its root form
      description: Use this to check if a word exists in the dictionary, or what 'root'
        form it links to (e.g., swimming > swim). The response tells you the possible
        [lemmas](documentation/glossary?term=lemma) for a given [inflected](documentation/glossary?term=inflection)
        word. This can then be combined with other endpoints to retrieve more information.
      operationId: getInflectionsSourceLangWord
      x-api-path-slug: inflectionssource-langword-id-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: word_id
        description: The input word
      responses:
        200:
          description: OK
      tags:
      - Inflections
      - Source
      - Lang
      - Word
      - Id
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