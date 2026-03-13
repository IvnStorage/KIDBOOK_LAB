# Анализ WikiData

Для поиска информации по теме экологии использовались SPARQL-запросы к базе знаний Wikidata.

## Пример запроса

```sparql
SELECT ?item ?itemLabel
WHERE {
  VALUES ?item { wd:Q3196 wd:Q1323632 wd:Q11435 wd:Q587582 }
  SERVICE wikibase:label { bd:serviceParam wikibase:language "ru,en". }
}
