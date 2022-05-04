---
title: Using CsvHelper GetRecords with a Non-standard Csv
tags:
- .NET
- C#
- CsvHelper
---
It's possible to use the CsvHelper CsvReader.GetRecords method to read non-standard Csv files (i.e. with extraneous, but correctly csv formatted, rows). This is done by creating a new Func for the CsvReader.Configuration.ShouldSkipRecord property. The approach used requires that records (i.e. valid data rows) are identifiably different from extraneous rows in some way (e.g. only valid data rows have a date in the first column).

Related

- [Parsing and Mapping CSV files with a header not on the first row](https://github.com/JoshClose/CsvHelper/issues/523)
- [Make ShouldSkipRecord changeable without overriding CsvReader](https://github.com/JoshClose/CsvHelper/issues/529)
- [config.ShouldSkipRecord Func overrides config.SkipEmptyRecords = true](https://github.com/JoshClose/CsvHelper/issues/575)