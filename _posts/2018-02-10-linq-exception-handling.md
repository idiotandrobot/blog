---
layout: post
title: LINQ Expression error handling
category: post
tags:
- C#
- LINQ
---
No straightforward way of adding exception handling to a LINQ query.

<noscript>
  <a href="https://gist.github.com/be47c8a6ee57e533d2ce6e1ee7673647#file-linq_list_to_dictionary-cs">Gist: LINQ List to Dictionary.cs</a>
</noscript>
{% gist be47c8a6ee57e533d2ce6e1ee7673647 file-linq_list_to_dictionary-cs %}

<noscript>
  <a href="https://gist.github.com/be47c8a6ee57e533d2ce6e1ee7673647#file-linq_expression-cs">Gist: LINQ Query Syntax</a>
</noscript>
{% gist be47c8a6ee57e533d2ce6e1ee7673647 file-linq_expression-cs %}

<noscript>
  <a href="https://gist.github.com/be47c8a6ee57e533d2ce6e1ee7673647#file-linq_expression_with_error_handling-cs">Gist: LINQ Method Syntax with exception handling</a>
</noscript>
{% gist be47c8a6ee57e533d2ce6e1ee7673647 file-linq_expression_with_error_handling-cs %}

Via 

- [StackOverflow: Exception handling within a LINQ Expression](https://stackoverflow.com/questions/4322542/exception-handling-within-a-linq-expression)
- [StackOverflow: Selecting List&lt;string&gt; into Dictionary with index](https://stackoverflow.com/questions/39386251/selecting-liststring-into-dictionary-with-index)
- [Query Syntax and Method Syntax in LINQ (C#)](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/query-syntax-and-method-syntax-in-linq)
