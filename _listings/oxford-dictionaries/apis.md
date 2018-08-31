---
name: Oxford Dictionaries
x-slug: oxford-dictionaries
description: If you&rsquo;re looking to enhance your app or website with dictionary
  data, don&rsquo;t compromise on quality. The Oxford Dictionaries API offers easy
  and intuitive access to Oxfords dictionary content, which is trusted around the
  world. Here at Oxford Dictionaries, home of the OED, we love words. That&rsquo;s
  why we have experienced lexicographers tracking the living language, delving deep
  into our corpora and monitoring a wide range of media in order to understand how
  words are being used and how language is evolving. This research is used by our
  editors to write and edit dictionary entries and translations, meaning we&rsquo;re
  able to offer up-to-date, accurate, and reliable lexical content in multiple languages.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
x-kinRank: "7"
x-alexaRank: "0"
tags: Oxford Dictionaries
created: "2018-08-30"
modified: "2018-08-30"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/apis.md
specificationVersion: "0.14"
apis:
- name: Oxford Dictionaries - Lists available domains in a bilingual dataset
  x-api-slug: domainssource-domains-languagetarget-domains-language-get
  description: Returns a list of the available [domains](documentation/glossary?term=domain)
    for a given bilingual language dataset.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/domainssource-domains-languagetarget-domains-language-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/domainssource-domains-languagetarget-domains-language-get-openapi.md
- name: Oxford Dictionaries - Lists available domains in a monolingual dataset
  x-api-slug: domainssource-language-get
  description: Returns a list of the available [domains](documentation/glossary?term=domain)
    for a given monolingual language dataset.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/domainssource-language-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/domainssource-language-get-openapi.md
- name: Oxford Dictionaries - Retrieve corpus sentences for a given word
  x-api-slug: entriessource-languageword-idsentences-get
  description: Use this to retrieve sentences extracted from  corpora which show how
    a word is used in the language. This is available for English and Spanish. For
    English, the sentences are linked to the correct [sense](documentation/glossary?term=sense)
    of the word in the dictionary. In Spanish, they are linked at the [headword](documentation/glossary?term=headword)
    level.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-languageword-idsentences-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-languageword-idsentences-get-openapi.md
- name: Oxford Dictionaries - Retrieve dictionary information for a given word
  x-api-slug: entriessource-langword-id-get
  description: Use this to retrieve definitions, [pronunciations](documentation/glossary?term=pronunciation),
    example sentences, [grammatical information](documentation/glossary?term=grammaticalfeatures)
    and [word origins](documentation/glossary?term=etymology). It only works for dictionary
    [headwords](documentation/glossary?term=headword), so you may need to use the
    [Lemmatron](documentation/glossary?term=lemma) first if your input is likely to
    be an [inflected](documentation/glossary?term=inflection) form (e.g., 'swimming').
    This would return the linked [headword](documentation/glossary?term=headword)
    (e.g., 'swim') which you can then use in the Entries endpoint. Unless specified
    using a region filter, the default lookup will be the Oxford Dictionary of English
    (GB).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-id-get-openapi.md
- name: Oxford Dictionaries - Retrieve words that mean the opposite
  x-api-slug: entriessource-langword-idantonyms-get
  description: Retrieve words that are opposite in meaning to the input word ([antonym](documentation/glossary?term=thesaurus)).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-idantonyms-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-idantonyms-get-openapi.md
- name: Oxford Dictionaries - Specify GB or US dictionary for English entry search
  x-api-slug: entriessource-langword-idregionsregion-get
  description: USe this filter to restrict the lookup to either our Oxford Dictionary
    of English (GB) or New Oxford American Dictionary (US).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-idregionsregion-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-idregionsregion-get-openapi.md
- name: Oxford Dictionaries - Retrieve words that are similar
  x-api-slug: entriessource-langword-idsynonyms-get
  description: Use this to retrieve words that are similar in meaning to the input
    word ([synonym](documentation/glossary?term=synonym)).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-idsynonyms-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-idsynonyms-get-openapi.md
- name: Oxford Dictionaries - Retrieve synonyms and antonyms for a given word
  x-api-slug: entriessource-langword-idsynonymsantonyms-get
  description: Retrieve available [synonyms](documentation/glossary?term=thesaurus)
    and [antonyms](documentation/glossary?term=thesaurus) for a given word and language.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-idsynonymsantonyms-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-idsynonymsantonyms-get-openapi.md
- name: Oxford Dictionaries - Apply filters to response
  x-api-slug: entriessource-langword-idfilters-get
  description: Use filters to limit the [entry](documentation/glossary?term=entry)
    information that is returned. For example, you may only require definitions and
    not everything else, or just [pronunciations](documentation/glossary?term=pronunciation).
    The full list of filters can be retrieved from the filters Utility endpoint. You
    can also specify values within the filter using '='. For example 'grammaticalFeatures=singular'.
    Filters can also be combined using a semicolon.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-idfilters-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-idfilters-get-openapi.md
- name: Oxford Dictionaries - Retrieve translation for a given word
  x-api-slug: entriessource-translation-languageword-idtranslationstarget-translation-language-get
  description: Use this to return translations for a given word. In the event that
    a word in the dataset does not have a direct translation, the response will be
    a [definition](documentation/glossary?term=entry) in the target language.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-translation-languageword-idtranslationstarget-translation-language-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-translation-languageword-idtranslationstarget-translation-language-get-openapi.md
- name: Oxford Dictionaries - Lists available filters
  x-api-slug: filters-get
  description: Returns a list of all the valid filters to construct API calls.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/filters-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/filters-get-openapi.md
- name: Oxford Dictionaries - Lists available filters for specific endpoint
  x-api-slug: filtersendpoint-get
  description: Returns a list of all the valid filters for a given endpoint to construct
    API calls.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/filtersendpoint-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/filtersendpoint-get-openapi.md
- name: Oxford Dictionaries - Lists available grammatical features in a dataset
  x-api-slug: grammaticalfeaturessource-language-get
  description: Returns a list of the available [grammatical features](documentation/glossary?term=grammaticalfeatures)
    for a given language dataset.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/grammaticalfeaturessource-language-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/grammaticalfeaturessource-language-get-openapi.md
- name: Oxford Dictionaries - Check a word exists in the dictionary and retrieve its
    root form
  x-api-slug: inflectionssource-langword-id-get
  description: Use this to check if a word exists in the dictionary, or what 'root'
    form it links to (e.g., swimming > swim). The response tells you the possible
    [lemmas](documentation/glossary?term=lemma) for a given [inflected](documentation/glossary?term=inflection)
    word. This can then be combined with other endpoints to retrieve more information.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/inflectionssource-langword-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/inflectionssource-langword-id-get-openapi.md
- name: Oxford Dictionaries - Apply optional filters to Lemmatron response
  x-api-slug: inflectionssource-langword-idfilters-get
  description: Retrieve available [lemmas](documentation/glossary?term=lemma) for
    a given [inflected](documentation/glossary?term=inflection) wordform. Filter results
    by categories.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/inflectionssource-langword-idfilters-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/inflectionssource-langword-idfilters-get-openapi.md
- name: Oxford Dictionaries - Lists available dictionaries
  x-api-slug: languages-get
  description: Returns a list of monolingual and bilingual language datasets available
    in the API
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/languages-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/languages-get-openapi.md
- name: Oxford Dictionaries - Lists available lexical categories in a dataset
  x-api-slug: lexicalcategorieslanguage-get
  description: Returns a list of available [lexical categories](documentation/glossary?term=lexicalcategory)
    for a given language dataset.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/lexicalcategorieslanguage-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/lexicalcategorieslanguage-get-openapi.md
- name: Oxford Dictionaries - Lists available regions in a monolingual dataset
  x-api-slug: regionssource-language-get
  description: Returns a list of the available [regions](documentation/glossary?term=regions)
    for a given monolingual language dataset.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/regionssource-language-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/regionssource-language-get-openapi.md
- name: Oxford Dictionaries - Lists available registers in a  monolingual dataset
  x-api-slug: registerssource-language-get
  description: Returns a list of the available [registers](documentation/glossary?term=registers)
    for a given monolingual language dataset.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/registerssource-language-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/registerssource-language-get-openapi.md
- name: Oxford Dictionaries - Lists available registers in a bilingual dataset
  x-api-slug: registerssource-register-languagetarget-register-language-get
  description: Returns a list of the available [registers](documentation/glossary?term=registers)
    for a given bilingual language dataset.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/registerssource-register-languagetarget-register-language-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/registerssource-register-languagetarget-register-language-get-openapi.md
- name: Oxford Dictionaries - Retrieve possible matches to input
  x-api-slug: searchsource-lang-get
  description: Use this to retrieve possible [headword](documentation/glossary?term=headword)
    matches for a given string of text. The results are culculated using headword
    matching, fuzzy matching, and [lemmatization](documentation/glossary?term=lemma)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/searchsource-lang-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/searchsource-lang-get-openapi.md
- name: Oxford Dictionaries - Retrieve possible translation matches to input
  x-api-slug: searchsource-search-languagetranslationstarget-search-language-get
  description: Use this to find matches in our translation dictionaries.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/searchsource-search-languagetranslationstarget-search-language-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/searchsource-search-languagetranslationstarget-search-language-get-openapi.md
- name: Oxford Dictionaries - Retrieve the frequency of ngrams (1-4) derived from
    a corpus
  x-api-slug: statsfrequencyngramssource-langcorpusngramsize-get
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/statsfrequencyngramssource-langcorpusngramsize-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/statsfrequencyngramssource-langcorpusngramsize-get-openapi.md
- name: Oxford Dictionaries - Retrieve the frequency of a word derived from a corpus.
  x-api-slug: statsfrequencywordsource-lang-get
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/statsfrequencywordsource-lang-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/statsfrequencywordsource-lang-get-openapi.md
- name: Oxford Dictionaries - Retrieve a list of frequencies of a word/words derived
    from a corpus.
  x-api-slug: statsfrequencywordssource-lang-get
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/statsfrequencywordssource-lang-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/statsfrequencywordssource-lang-get-openapi.md
- name: Oxford Dictionaries - Retrieve list of words for category with advanced options
  x-api-slug: wordlistsource-langfilters-advanced-get
  description: Use this to apply more complex filters to the [list of words](documentation/glossary?term=wordlist).
    For example, you may only want to filter out words for which all [senses](documentation/glossary?term=sense)
    match the filter, or only its 'prime sense'. You can also filter by word length
    or match by substring (prefix).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/wordlistsource-langfilters-advanced-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/wordlistsource-langfilters-advanced-get-openapi.md
- name: Oxford Dictionaries - Retrieve a list of words in a category
  x-api-slug: wordlistsource-langfilters-basic-get
  description: Use this to retrieve a [list of words](documentation/glossary?term=wordlist)
    for particular [domain](documentation/glossary?term=domain), [lexical category](documentation/glossary?term=lexicalcategory),
    [register](documentation/glossary?term=registers) and/or [region](documentation/glossary?term=regions).
    View the full list of possible filters using the filters Utility endpoint.  The
    response only includes [headwords](documentation/glossary?term=headword), not
    all their possible [inflections](documentation/glossary?term=inflection). If you
    require a full [wordlist](documentation/glossary?term=wordlist) including [inflected
    forms](documentation/glossary?term=inflection), contact us and we can help.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/wordlistsource-langfilters-basic-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/wordlistsource-langfilters-basic-get-openapi.md
- name: Oxford Dictionaries - Lists available domains in a given bilingual language
    dataset.
  x-api-slug: domainssource-languagetarget-language-get
  description: Returns a list of the available [domains](/glossary?tag=#domains&expand)
    for a given bilingual language dataset.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/domainssource-languagetarget-language-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/domainssource-languagetarget-language-get-openapi.md
- name: Oxford Dictionaries - Retrieve only definitions in entry search.
  x-api-slug: entriessource-langword-iddefinitions-get
  description: Find available [dictionary entries](/glossary?tag=#entry&expand) for
    given word and language. Filter results by categories.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-iddefinitions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-iddefinitions-get-openapi.md
- name: Oxford Dictionaries - Retrieve only example sentences in entry search.
  x-api-slug: entriessource-langword-idexamples-get
  description: Find available [dictionary entries](/glossary?tag=#entry&expand) for
    given word and language. Filter results by categories.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-idexamples-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-idexamples-get-openapi.md
- name: Oxford Dictionaries - Retrieve only pronunciations in entry search.
  x-api-slug: entriessource-langword-idpronunciations-get
  description: Find available [dictionary entries](/glossary?tag=#entry&expand) for
    given word and language. Filter results by categories.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-idpronunciations-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-idpronunciations-get-openapi.md
- name: Oxford Dictionaries - Find translation for a given word.
  x-api-slug: entriessource-langword-idtranslationstarget-lang-get
  description: "Returns target language translations for a given word ID and source
    language. \nIn the event that a word in the dataset does not have a direct translation,
    the response will be a [definition](/glossary?tag=#entry&expand) in the target
    language."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-idtranslationstarget-lang-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/entriessource-langword-idtranslationstarget-lang-get-openapi.md
- name: Oxford Dictionaries - Lists available registers in a given bilingual language
    dataset.
  x-api-slug: registerssource-languagetarget-language-get
  description: Returns a list of the available [registers](/glossary?tag=#registers&expand)
    for a given bilingual language dataset.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/registerssource-languagetarget-language-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/registerssource-languagetarget-language-get-openapi.md
- name: Oxford Dictionaries - Find translation results for search query.
  x-api-slug: searchsource-langtranslationstarget-lang-get
  description: Find available translation results  for a search query and language.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/searchsource-langtranslationstarget-lang-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/oxford-dictionaries/master/_listings/oxford-dictionaries/searchsource-langtranslationstarget-lang-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://orghunter.api.gallery.streamdata.io
- type: x-api-stack
  url: http://oxford.dictionaries.stack.network
- type: x-blog
  url: https://api-blog.oxforddictionaries.com/
- type: x-developer
  url: https://developer.oxforddictionaries.com/
- type: x-faq
  url: https://developer.oxforddictionaries.com/faq
- type: x-forum
  url: https://forum.oxforddictionaries.com/api/
- type: x-twitter
  url: https://twitter.com/OxfordWordsAPI
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---