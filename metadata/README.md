# metadata

In `metadata/`, information is stored about individuals who make appearances in the corpus data.

## Orgaization

Individuals must be assigned a unique identifier (wiki_id?). Csv files are constructed around single attributes and the unique identifier serves as a primary key (Normal database principles). e.g.:

`individual.csv`
```
id, name
uuid-1, john smith
uuid-2, jane dowski
```

`state.csv`
```
id, state
uuid-1, Ireland
uuid-2, Poland
```

etc...