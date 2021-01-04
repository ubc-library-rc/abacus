## Search syntax tips

**Searching for phrases** is often an effective way to quickly locate data. This is done by enclosing multiple terms in double quotation marks: `"adult literacy"`. While this can be a powerful way to search when you know specifically what you are looking for, it is important to be aware of its potential limitations--namely, it is very restrictive and may incidentally exclude material of interest. For example, a search for `"adult literacy survey"`  will return the *International Adult Literacy Survey (IALS)*, but not the *Adult Literacy and Life Skills Survey*.

> Searching for phrases must be done using *double* quotation marks. Using single quotation marks is equivalent to using *no* quotation marks. Thus, `'income inequality'` produces the same results as `income inequality`: a search for objects containing the term "income" OR the term "inequality".

**Making use of logical operators** will greatly improve search results. In addition to the `AND` and `OR` operators discussed above, other useful Boolean operators include `NOT` (`!`), `+`, and `-`. The `NOT` and `-` operators function similarly, requiring that the term following the operator not be present in search results, while the `+` operator requires that the term is present. For instance, `literacy !child`, or `literacy -child`, will return all results on "literacy" without the term "child", while `+"adult literacy" survey` requires that material be returned containing the phrase "adult literacy", but may or may not contain the term "survey".

> To use Boolean operators in word form (e.g. `AND`, `OR`, `NOT`), all letters must be uppercase. Additionally, when using the `!` operator, unlike its word form `NOT`, do not include a space before the term it applies to--correct: `education !primary`, incorrect: `education ! primary`.

**To escape special characters**, precede them with a backslash (`\`). For example, the syntax for searching for "What is to be done?: Living in a world where 1+1 is !" would be `"What is to be done\?\: Living in a world where 1\+1 is \!"`, since `?`, `:`, `+`, and `!` are all special characters.

For added control over the Boolean logic of a search, users can **group clauses to form sub-queries** using parentheses. Searching for `vaccine AND ("corona virus" OR "COVID-19")` will return material that matches either "vaccine" and "corona virus" or "vaccine" and "COVID-19".

Users can also narrow their search within Abacus by **querying specific fields**. The syntax for this requires, first, specifiying the field to be searched (e.g. `title`), followed by a `:`, and then the term to search for: `title:financialization`. (NOTE: There is no space between the colon and the search term. Including one will run a different search: one for "title" OR "financialization".) Searching for multiple terms within a field requires specifying the field before each term. For example, the sytnax for searching for the terms "financial" and "markets" within the "title" field is `title:financial AND title:markets`. Using the query `title:financial markets` will search for "financial" in the "title" field and "markets" in Abacus' "description" field. To search for the phrase "financial markets" in the "title" field, wrap the phrase in double quotation marks: `title:"financial markets"`.

Abacus supports the use of both single- and multiple-character **wildcards** in its search software. Single-character wildcard searches use the `?` operator. For instance, `?oom` matches "zoom", "room", and "boom", but not "broom". The `?` operator can appear anywhere in a term (beginning, middle, or end). The `*` operator matches zero or more sequential characters in a term. So, `revolution*` matches "revolution", "revolutionary", and "revolutionaries". Like the `?` operator, it can be placed anywhere in a term.

> Wilcard operators function only on terms, not phrases.

**Searching by specifying a date range** can also be an effective way to find data. Dates and times in Abacus are formatted as `YYYY-MM-DDThh:mm:ssZ`, where:
- `YYYY` is the year,
- `MM` is the month,
- `DD` is the day of the month,
- `T` denotes the change from date to time (This always remains constant; it does not require changing.),
- `hh` is the hour of the day using a 24-hour clock (e.g. 1 pm is 13, 10 pm is 22, etc.),
- `mm` is the minutes,
- `ss` is the seconds, and
- `Z` denotes that the time is in Coordinated Universal Time (UTC).

> Since the date format contains colons, which are a special character, escaping is required: `1973-12-22T14\:33\:46Z`. Alternatively, this query can be written without escaping using double quotation marks: `"1973-12-22T14:33:46Z"`. If a date is included within brackets, such as for a date range, then escaping is not required: `[1973-12-22T14:33:46Z TO 1975-11-02T17:39:42Z]`.

**Range syntax** is denoted in Abacus as `[ TO ]`, where both a lower and upper bound are specified. Different types of brackets indicate whether these bounds are inclusive or exclusive. Square brackets `[]` represent inclusive lower and upper bounds, whereas curly brackets `{}` represent exclusive bounds. These can be combined within a single query: `{1956-02-16 TO 1988-05-03]`. The current time can be represented using the special value `NOW`, while an asterisk `*` represents either the earliest or most recent data deposit, depending on its location within a query. Thus, entering `[* TO 2001-09-11}` would return all matched objects from the earliest in the repository up to (but excluding) 11 September 2001, whereas entering `[2001-09-11 TO *]` would return all matched objects from (and including) 11 September 2001 up to the most recent related deposit.
