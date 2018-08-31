---
swagger: "2.0"
x-collection-name: Oxford Dictionaries
x-complete: 0
info:
  title: Oxford Dictionaries Retrieve only example sentences in entry search.
  description: Find available [dictionary entries](/glossary?tag=#entry&expand) for
    given word and language. Filter results by categories.
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
  /inflections/{source_lang}/{word_id}/{filters}:
    get:
      summary: Apply optional filters to Lemmatron response
      description: Retrieve available [lemmas](documentation/glossary?term=lemma)
        for a given [inflected](documentation/glossary?term=inflection) wordform.
        Filter results by categories.
      operationId: getInflectionsSourceLangWordFilters
      x-api-path-slug: inflectionssource-langword-idfilters-get
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
      - Filters
  /languages:
    get:
      summary: Lists available dictionaries
      description: Returns a list of monolingual and bilingual language datasets available
        in the API
      operationId: getLanguages
      x-api-path-slug: languages-get
      parameters:
      - in: query
        name: No Name
      - in: query
        name: sourceLanguage
        description: IANA language code
      - in: query
        name: targetLanguage
        description: IANA language code
      responses:
        200:
          description: OK
      tags:
      - Languages
  /lexicalcategories/{language}:
    get:
      summary: Lists available lexical categories in a dataset
      description: Returns a list of available [lexical categories](documentation/glossary?term=lexicalcategory)
        for a given language dataset.
      operationId: getLexicalcategoriesLanguage
      x-api-path-slug: lexicalcategorieslanguage-get
      parameters:
      - in: path
        name: language
        description: IANA language code
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Lexicalcategories
      - Language
  /regions/{source_language}:
    get:
      summary: Lists available regions in a monolingual dataset
      description: Returns a list of the available [regions](documentation/glossary?term=regions)
        for a given monolingual language dataset.
      operationId: getRegionsSourceLanguage
      x-api-path-slug: regionssource-language-get
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
      - Regions
      - Source
      - Language
  /registers/{source_language}:
    get:
      summary: Lists available registers in a  monolingual dataset
      description: Returns a list of the available [registers](documentation/glossary?term=registers)
        for a given monolingual language dataset.
      operationId: getRegistersSourceLanguage
      x-api-path-slug: registerssource-language-get
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
      - Registers
      - Source
      - Language
  /registers/{source_register_language}/{target_register_language}:
    get:
      summary: Lists available registers in a bilingual dataset
      description: Returns a list of the available [registers](documentation/glossary?term=registers)
        for a given bilingual language dataset.
      operationId: getRegistersSourceRegisterLanguageTargetRegisterLanguage
      x-api-path-slug: registerssource-register-languagetarget-register-language-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: source_register_language
        description: IANA language code
      - in: path
        name: target_register_language
        description: IANA language code
      responses:
        200:
          description: OK
      tags:
      - Registers
      - Source
      - Register
      - Language
      - Target
      - Register
      - Language
  /search/{source_lang}:
    get:
      summary: Retrieve possible matches to input
      description: Use this to retrieve possible [headword](documentation/glossary?term=headword)
        matches for a given string of text. The results are culculated using headword
        matching, fuzzy matching, and [lemmatization](documentation/glossary?term=lemma)
      operationId: getSearchSourceLang
      x-api-path-slug: searchsource-lang-get
      parameters:
      - in: query
        name: limit
        description: Limit the number of results per response
      - in: query
        name: No Name
      - in: query
        name: offset
        description: Offset the start number of the result
      - in: query
        name: prefix
        description: Set prefix to true if youd like to get results only starting
          with search string
      - in: query
        name: q
        description: Search string
      - in: query
        name: regions
        description: If searching in English, filter words with specific region(s)
          either us or gb
      - in: path
        name: source_lang
        description: IANA language code
      responses:
        200:
          description: OK
      tags:
      - Search
      - Source
      - Lang
  /search/{source_search_language}/translations={target_search_language}:
    get:
      summary: Retrieve possible translation matches to input
      description: Use this to find matches in our translation dictionaries.
      operationId: getSearchSourceSearchLanguageTranslationsTargetSearchLanguage
      x-api-path-slug: searchsource-search-languagetranslationstarget-search-language-get
      parameters:
      - in: query
        name: limit
        description: Limit the number of results per response
      - in: query
        name: No Name
      - in: query
        name: offset
        description: Offset the start number of the result
      - in: query
        name: prefix
        description: Set prefix to true if youd like to get results only starting
          with search string
      - in: query
        name: q
        description: Search string
      - in: query
        name: regions
        description: Filter words with specific region(s) E
      - in: path
        name: source_search_language
        description: IANA language code
      - in: path
        name: target_search_language
        description: IANA language code
      responses:
        200:
          description: OK
      tags:
      - Search
      - Source
      - Search
      - Language
      - Translations=target
      - Search
      - Language
  /stats/frequency/ngrams/{source_lang}/{corpus}/{ngram-size}/:
    get:
      summary: Retrieve the frequency of ngrams (1-4) derived from a corpus
      description: |-
        This endpoint returns frequencies of ngrams of size 1-4. That is the number of times a word (ngram size = 1) or words (ngram size > 1) appear in the corpus. Ngrams are case sensitive ("I AM" and "I am" will have different frequency) and frequencies are calculated per word (true case) so "the book" and "the books" are two different ngrams. The results can be filtered based on query parameters.   Parameters can be provided in PATH, GET or POST (form or json). The parameters in PATH are overriden by parameters in GET, POST and json (in that order). In PATH, individual options are separated by semicolon and values are separated by commas (where multiple values can be used).   Example for bigrams (ngram of size 2):
        * PATH: /tokens=a word,another word
        * GET: /?tokens=a word&tokens=another word
        * POST (json):

          ```javascript
            {
                "tokens": ["a word", "another word"]
            }
          ```
      operationId: getStatsFrequencyNgramsSourceLangCorpusNgramSize
      x-api-path-slug: statsfrequencyngramssource-langcorpusngramsize-get
      parameters:
      - in: query
        name: contains
        description: Find ngrams containing the given token(s)
      - in: path
        name: corpus
        description: For corpora other than nmc (New Monitor Corpus) please contact
          api@oxforddictionaries
      - in: query
        name: format
        description: Option specifying whether tokens should be returned as a single
          string (option google) or as a list of strings (option oup)
      - in: query
        name: limit
        description: pagination - results limit
      - in: query
        name: maxDocumentFrequency
        description: Restrict the query to entries that appera in at most `maxDocumentFrequency`
          documents
      - in: query
        name: maxFrequency
        description: Restrict the query to entries with frequency of at most `maxFrequency`
      - in: query
        name: minDocumentFrequency
        description: Restrict the query to entries that appear in at least `minDocumentFrequency`
          documents
      - in: query
        name: minFrequency
        description: Restrict the query to entries with frequency of at least `minFrequency`
      - in: path
        name: ngram-size
        description: the size of ngrams requested (1-4)
      - in: query
        name: No Name
      - in: query
        name: offset
        description: pagination - results offset
      - in: query
        name: punctuation
        description: Flag specifying whether to lookup ngrams that include punctuation
          or not (possible values are true and false; default is false)
      - in: path
        name: source_lang
        description: IANA language code
      - in: query
        name: tokens
        description: List of tokens to filter
      responses:
        200:
          description: OK
      tags:
      - Stats
      - Frequency
      - Ngrams
      - Source
      - Lang
      - Corpus
      - Ngram-size
  /stats/frequency/word/{source_lang}/:
    get:
      summary: Retrieve the frequency of a word derived from a corpus.
      description: |-
        This endpoint provides the frequency of a given word. When multiple database records match the query parameters, the returned frequency is the sum of the individual frequencies. For example, if the query parameters are lemma=test, the returned frequency will include the verb "test", the noun "test" and the adjective "test" in all forms (Test, tested, testing, etc.)   If you are interested in the frequency of the word "test" but want to exclude other forms (e.g., tested) use the option trueCase=test. Normally, the word "test" will be spelt with a capital letter at the beginning of a sentence. The option trueCase will ignore this and it will count "Test" and "test" as the same token. If you are interested in frequencies of "Test" and "test", use the option wordform=test or wordform=Test. Note that trueCase is not just a lower case of the word as some words are genuinely spelt with a capital letter such as the word "press" in Oxford University Press.   Parameters can be provided in PATH, GET or POST (form or json). The parameters in PATH are overriden by parameters in GET, POST and json (in that order). In PATH, individual options are separated by semicolon and values are separated by commas (where multiple values can be used). Examples:
        * PATH: /lemma=test;lexicalCategory=noun
        * GET: /?lemma=test&lexicalCategory=noun
        * POST (json):

          ```javascript
            {
              "lemma": "test",
              "lexicalCategory": "noun"
            }
          ```

         One of the options wordform/trueCase/lemma/lexicalCategory has to be provided.
      operationId: getStatsFrequencyWordSourceLang
      x-api-path-slug: statsfrequencywordsource-lang-get
      parameters:
      - in: query
        name: corpus
        description: For corpora other than nmc (New Monitor Corpus) please contact
          api@oxforddictionaries
      - in: query
        name: lemma
        description: The lemma of the word to look up (e
      - in: query
        name: lexicalCategory
        description: The lexical category of the word(s) to look up (e
      - in: query
        name: No Name
      - in: path
        name: source_lang
        description: IANA language code
      - in: query
        name: trueCase
        description: The written form of the word to look up with normalised case
          (Books --> books)
      - in: query
        name: wordform
        description: The written form of the word to look up (preserving case e
      responses:
        200:
          description: OK
      tags:
      - Stats
      - Frequency
      - Word
      - Source
      - Lang
  /stats/frequency/words/{source_lang}/:
    get:
      summary: Retrieve a list of frequencies of a word/words derived from a corpus.
      description: |-
        This endpoint provides a list of frequencies for a given word or words. Unlike the /word/ endpoint, the results are split into the smallest units.   To exclude a specific value, prepend it with the minus sign ('-'). For example, to get frequencies of the lemma 'happy' but exclude superlative forms (i.e., happiest) you could use options 'lemma=happy;grammaticalFeatures=-degreeType:superlative'.   Parameters can be provided in PATH, GET or POST (form or json). The parameters in PATH are overriden by parameters in GET, POST and json (in that order). In PATH, individual options are separated by semicolon and values are separated by commas (where multiple values can be used).   The parameters wordform/trueCase/lemma/lexicalCategory also exist in a plural form, taking a lists of items. Examples:
        * PATH: /wordforms=happy,happier,happiest
        * GET: /?wordforms=happy&wordforms=happier&wordforms=happiest
        * POST (json):
        ```javascript
          {
            "wordforms": ["happy", "happier", "happiest"]
          }
        ```
         Aside from individual frequency requests, users can also post a list of items for which they would like to get frequencies. The list has to be uploaded in json and the required fields are "items" and "collate".   The field "items" is a list of items for which you want the frequencies. The content of the items depends on the option for "collate". The value of "collate" should be a list of "columns" that the items contain. The list is limited to combinations of "wordform", "lemma", "trueCase" and "lexicalCategory". The fields that are listed in the "collate" options have to be present in each item. Here are some examples of queries:
        * ### Get frequencies of provided wordforms:
        ```javascript
          {
              "collate": ["wordform"],
              "items": [{"wordform": "test"}, {"wordform": "Test"}]
          }
        ```
        * ### Get frequencies of provided lemmas:
        ```javascript
          {
              "collate": ["lemma"],
              "items": [{"lemma": "test"}, {"lemma": "Test"}]
          }
        ```
        * ### Get frequencies of provided lemmas per lexical category:
        ```javascript
          {
              "collate": ["lemma", "lexicalCategory"],
              "items": [
                  {"lemma": "test", "lexicalCategory": "verb"},
                  {"lemma": "test", "lexicalCategory": "noun"}
              ]
          }
        ```
      operationId: getStatsFrequencyWordsSourceLang
      x-api-path-slug: statsfrequencywordssource-lang-get
      parameters:
      - in: query
        name: corpus
        description: For corpora other than nmc (New Monitor Corpus) please contact
          api@oxforddictionaries
      - in: query
        name: grammaticalFeatures
        description: The grammatical features of the word(s) to look up entered as
          a list of k:v (e
      - in: query
        name: lemma
        description: The lemma of the word to look up (e
      - in: query
        name: lexicalCategory
        description: The lexical category of the word(s) to look up (e
      - in: query
        name: limit
        description: pagination - results limit
      - in: query
        name: maxFrequency
        description: Restrict the query to entries with frequency of at most `maxFrequency`
      - in: query
        name: maxNormalizedFrequency
        description: Restrict the query to entries with frequency of at most `maxNormalizedFrequency`
      - in: query
        name: minFrequency
        description: Restrict the query to entries with frequency of at least `minFrequency`
      - in: query
        name: minNormalizedFrequency
        description: Restrict the query to entries with frequency of at least `minNormalizedFrequency`
      - in: query
        name: No Name
      - in: query
        name: offset
        description: pagination - results offset
      - in: query
        name: sort
        description: sort the resulting list by wordform, trueCase, lemma, lexicalCategory,
          frequency, normalizedFrequency
      - in: path
        name: source_lang
        description: IANA language code
      - in: query
        name: trueCase
        description: The written form of the word to look up with normalised case
          (Books --> books)
      - in: query
        name: wordform
        description: The written form of the word to look up (preserving case e
      responses:
        200:
          description: OK
      tags:
      - Stats
      - Frequency
      - Words
      - Source
      - Lang
  /wordlist/{source_lang}/{filters_advanced}:
    get:
      summary: Retrieve list of words for category with advanced options
      description: Use this to apply more complex filters to the [list of words](documentation/glossary?term=wordlist).
        For example, you may only want to filter out words for which all [senses](documentation/glossary?term=sense)
        match the filter, or only its 'prime sense'. You can also filter by word length
        or match by substring (prefix).
      operationId: getWordlistSourceLangFiltersAdvanced
      x-api-path-slug: wordlistsource-langfilters-advanced-get
      parameters:
      - in: query
        name: exact
        description: If exact=true wordlist returns a list of entries that exactly
          matches the search string
      - in: query
        name: exclude
        description: Semicolon separated list of parameters-value pairs (same as filters)
      - in: query
        name: exclude_prime_senses
        description: Semicolon separated list of parameters-value pairs (same as filters)
      - in: query
        name: exclude_senses
        description: Semicolon separated list of parameters-value pairs (same as filters)
      - in: path
        name: filters_advanced
        description: 'Semicolon separated list of wordlist parameters, presented as
          value pairs: LexicalCategory, domains, regions, registers'
      - in: query
        name: limit
        description: Limit the number of results per response
      - in: query
        name: No Name
      - in: query
        name: offset
        description: Offset the start number of the result
      - in: query
        name: prefix
        description: Filter words that start with prefix parameter
      - in: query
        name: word_length
        description: Parameter to speficy the minimum (>), exact or maximum (5 - more
          than 5 chars; 5
      responses:
        200:
          description: OK
      tags:
      - Wordlist
      - Source
      - Lang
      - Filters
      - Advanced
  /wordlist/{source_lang}/{filters_basic}:
    get:
      summary: Retrieve a list of words in a category
      description: Use this to retrieve a [list of words](documentation/glossary?term=wordlist)
        for particular [domain](documentation/glossary?term=domain), [lexical category](documentation/glossary?term=lexicalcategory),
        [register](documentation/glossary?term=registers) and/or [region](documentation/glossary?term=regions).
        View the full list of possible filters using the filters Utility endpoint.  The
        response only includes [headwords](documentation/glossary?term=headword),
        not all their possible [inflections](documentation/glossary?term=inflection).
        If you require a full [wordlist](documentation/glossary?term=wordlist) including
        [inflected forms](documentation/glossary?term=inflection), contact us and
        we can help.
      operationId: getWordlistSourceLangFiltersBasic
      x-api-path-slug: wordlistsource-langfilters-basic-get
      parameters:
      - in: path
        name: filters_basic
        description: 'Semicolon separated list of wordlist parameters, presented as
          value pairs: LexicalCategory, domains, regions, registers'
      - in: query
        name: limit
        description: Limit the number of results per response
      - in: query
        name: No Name
      - in: query
        name: offset
        description: Offset the start number of the result
      responses:
        200:
          description: OK
      tags:
      - Wordlist
      - Source
      - Lang
      - Filters
      - Basic
  /domains/{source_language}/{target_language}:
    get:
      summary: Lists available domains in a given bilingual language dataset.
      description: Returns a list of the available [domains](/glossary?tag=#domains&expand)
        for a given bilingual language dataset.
      operationId: getDomainsSourceLanguageTargetLanguage
      x-api-path-slug: domainssource-languagetarget-language-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Domains
      - Source
      - Language
      - Target
      - Language
  /entries/{source_lang}/{word_id}/definitions:
    get:
      summary: Retrieve only definitions in entry search.
      description: Find available [dictionary entries](/glossary?tag=#entry&expand)
        for given word and language. Filter results by categories.
      operationId: getEntriesSourceLangWordDefinitions
      x-api-path-slug: entriessource-langword-iddefinitions-get
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
      - Definitions
  /entries/{source_lang}/{word_id}/examples:
    get:
      summary: Retrieve only example sentences in entry search.
      description: Find available [dictionary entries](/glossary?tag=#entry&expand)
        for given word and language. Filter results by categories.
      operationId: getEntriesSourceLangWordExamples
      x-api-path-slug: entriessource-langword-idexamples-get
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
      - Examples
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