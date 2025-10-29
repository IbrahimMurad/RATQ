# quran.com

[quran.com](https://quran.com/) is a platform supported by [Quran.Foundation](https://quran.foundation/) designed to make the Quran accessible to everyone by providing translations, tafsir (exegesis), recitations, and word-by-word translations. It offers various tools for deeper Quranic study in multiple languages, making it easier to understand the Quran's meanings.

## Key Features & Offerings

Quran.com is designed to support every stage of engagement with the Quran—from reading and memorization to study and reflection. Our features include:

- It supports multifaceted access to Quranic content, including verse-by-verse translations and detailed linguistic analysis.
    
- The platform integrates powerful search capabilities enriched by semantic technologies such as Kalimat to enhance search relevance.
    
- Quran.com exposes content APIs ([https://api-docs.quran.foundation/](https://api-docs.quran.foundation/)) that provide programmatic access to Quranic chapters, verses, and translations.
    
- The back-end uses Elasticsearch for efficient full-text searching and Kalimat for semantic understanding to improve the quality and relevance of user queries.
- It has a developer portal with API documentation to help developers build Quran-related applications.
    
- The website applies advanced natural language processing tools for Quranic Arabic morphology, syntax, and semantics.
  
- For developers, its both front-end ([https://github.com/quran/quran.com-frontend-next](https://github.com/quran/quran.com-frontend-next)) and back-end ([https://github.com/quran/quran.com-api](https://github.com/quran/quran.com-api)) source code are open for usage and collaboration.

## Resources and Contributions

- [Tanzil](https://tanzil.net/): An international Quranic project aimed at providing a highly-verified precise Quran text.
- [QuranComplex](https://qurancomplex.gov.sa/): King Fahd Glorious Qur'an Printing Complex is a leader in serving the Glorious Qur'an and its Sciences, translating its Meanings, and safeguarding the Qur'anic Text from distortion, through the optimal use of advanced technologies in the field of printing, audio recordings, electronic publishing and digital applications.
- [Collin Fair](https://github.com/cpfair/quran-align): A tool for producing word-precise segmentation of recorded Qur'anic recitation.
- [QuranEnc](https://quranenc.com/en/home): A portal featuring free and trustworthy translations of the meanings and exegeses of the noble Qur'an in many world languages.
- [Zekr](https://zekr.org): An open platform Quran study tool for browsing and researching on the Quran
- [Tarteel](https://tarteel.ai/): An AI-powered Quran memorization app. It's designed to help you memorize smarter, whether you're searching for a verse, tracking your progress, or following along with your recitation.
- [Lokalize](https://lokalise.com/): A computer-aided translation system that focuses on productivity and quality assurance and provides a seamless localization workflow.

## Searching Feature

The architecture of Quran.com search integrates both Elasticsearch and Kalimat to leverage their respective strengths, but they serve different roles within the system.

### Elasticsearch Components

- **Core Search Back-end**: Elasticsearch acts as the primary engine for full-text search. It indexes Quranic data and helps perform fast, keyword-based searches across large volumes of text.​
- **Index and Shard Management**: It manages the creation of indices, primary shards, and replicas. Elasticsearch distributes data across nodes for scalability, fault tolerance, and load balancing.
- **Data Storage and Retrieval**: Handles storage of Quranic data, supporting real-time querying, filtering, and aggregations. Elasticsearch responds quickly to keyword and phrase searches, making it suitable for straightforward search needs.
### Kalimat Components

- **Semantic Search Layer**: Kalimat is a neural network-based semantic search engine that understands the context and meaning of queries. It enriches the search process by interpreting user intent beyond simple keyword matching.
- **Complementary Role**: It likely overlays or integrates with Elasticsearch, providing more nuanced, concept-based search results, especially for complex or natural language questions. Kalimat interacts with the search API, analyzing either part of or the entire query for better relevance.

### How They Work Together


-  **Hybrid Architecture** 
	  Elasticsearch handles rapid, full-text searches. Kalimat processes user queries for semantic understanding. The combined system sends semantic insights from Kalimat to enhance or refine the search query in Elasticsearch.
- **Workflow**: When a user makes a search:
    1. Kalimat interprets the query to understand its context.
    2. The optimized or enriched query is sent to Elasticsearch.
    3. Elasticsearch retrieves precise keyword matches, which are then filtered or ranked based on Kalimat’s understanding.

### Diagram Concept

While no explicit diagram was available in the search results, the architecture can be visualized as:
```text
User Query
    |
    v
Kalimat (Semantic Understanding)
    |
    v
Enhanced Search Query
    |
    v
Elasticsearch (Full-Text Index & Search)
    |
    v
Search Results
```

## Conclusion
quran.com provide the users with web, android, and IOS applications both online and offline and provides developers with an API that requires only a request for the API-Key at the first time (and it is free). But it does not provided in source data by any means. Only contributors can have a mini dumb by joining their slack channel and requesting it from the project's collaborator.