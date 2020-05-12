# Aggregated Library Solr Configs

Library bibliographic data (via MARC or whatever) offer a strange set of characteristics -- some great, granular
information, some important atrributes thrown willy-nilly into free-text fields, standards that have changed
over time, etc. -- which can make building a search application over these data challenging.

A useful question is "How do people transform/normalize data as it is indexed?" Index-time and query-time
transformations reflect decisions libraries make with respect to which attributes of the text are "important" in
terms of adding to relevancy in the results.

In additon to many blog posts and articles on attempts to improve "library catalog search" (writ large), it might
be useful to look at the actual implementations, and here's a place to put them.


Please drop bill@dueber.com a note if you want me to add your data, or (better yet) submit a pul request!

## Penn State
  * [Solr configuration](https://github.com/psu-libraries/psulib_blacklight/tree/master/solr/conf)

**Noteworthy(?)**:
  * Almost completely driven by dynamic fields (see the [solrconfig.xml](https://github.com/psu-libraries/psulib_blacklight/blob/master/solr/conf/solrconfig.xml) for lists of default fields and weights.
  * Uses a minimal base `text` type: ICU tokenization with NFKC (case/diacritic) folding.

## Standford
  * [So. Many. Solr. Configs](https://github.com/sul-dlss/sul-solr-configs)

**Noteworthy(?)**:
  * Eighty-zillion solr repos for every imagined repository.

## TRLN
  * [Solr config](https://github.com/trln/argon-solr-config)

**Noteworthy(?)**:
  * Derived from [solr6_test_conf](https://github.com/billdueber/solr6_test_conf) and uses the [Standford CJK filters](https://github.com/sul-dlss/CJKFilterUtils).




## University of Michigan
  * [Solr configuration]()
  * [Traject configuration]()

**Noteworthy(?)**:
  * Hideously over-engineered use of XML entities to try to encapsulate common sets of filters


