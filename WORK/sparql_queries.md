# Анализ Wikidata

Для анализа предметной области экологии был выполнен SPARQL-запрос к базе знаний Wikidata.

## Запрос

```sparql
SELECT ?item ?itemLabel
WHERE {
  VALUES ?item {
    wd:Q125928
    wd:Q132580
    wd:Q7202090
    wd:Q11394
  }

  SERVICE wikibase:label {
    bd:serviceParam wikibase:language "ru,en".
  }
}
```

## Полученные данные

| item | itemLabel |
|---|---|
| wd:Q125928 | глобальное потепление |
| wd:Q132580 | переработка отходов |
| wd:Q7202090 | пластиковое загрязнение |
| wd:Q11394 | вымирающие виды |

Результаты запроса были выгружены в файл  
`wikidata_ecology_sample.csv`.
