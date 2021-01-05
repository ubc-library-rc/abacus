## Search syntax tips

**Making use of logical operators** will greatly improve search results. In addition to the `AND` and `OR` operators, other useful Boolean operators include `NOT` (`!`), `+`, and `-`. The `NOT` and `-` operators function similarly, requiring that the term following the operator not be present in search results, while the `+` operator requires that the term is present. For instance, `literacy !child`, or `literacy -child`, will return all results on "literacy" without the term "child", while `+"adult literacy" survey` requires that material be returned containing the phrase "adult literacy", but may or may not contain the term "survey".

> To use Boolean operators in word form (e.g. `AND`, `OR`, `NOT`), all letters must be uppercase. Additionally, when using the `!` operator, unlike its word form `NOT`, do not include a space before the term it applies to--correct: `education !primary`, incorrect: `education ! primary`.

**To escape special characters**, precede them with a backslash (`\`). For example, the syntax for searching for "What is to be done?: Living in a world where 1+1 is !" would be `"What is to be done\?\: Living in a world where 1\+1 is \!"`, since `?`, `:`, `+`, and `!` are all special characters.

For added control over the Boolean logic of a search, users can **group clauses to form sub-queries** using parentheses. Searching for `vaccine AND ("corona virus" OR "COVID-19")` will return material that matches either "vaccine" and "corona virus" or "vaccine" and "COVID-19".

Abacus supports two distinct **search scopes**: "global" and "local". Using the search box on the left-hand side of the user interface will limit results to the dataverse currently selected (a "local" search), while using the search box through selecting the "Search" drop-down menu at the top of the user interface will execute a query on all dataverses in Abacus (a "global" search).

<img style="padding-top: 30px; padding-bottom: 30px; margin-left: 50px" src="images/global_search.png" width="80%"/>

Users can also narrow their search within Abacus by **querying specific fields**. The syntax for this requires, first, specifiying the field to be searched (e.g. `title`), followed by a `:`, and then the term to search for: `title:financialization`. (NOTE: There is no space between the colon and the search term. Including one will run a different search: one for "title" OR "financialization".)

Searching for multiple terms within a field requires specifying the field before each term. For example, the sytnax for searching for the terms "financial" and "markets" within the "title" field is `title:financial AND title:markets`. Using the query `title:financial markets` will search for "financial" in the "title" field and "markets" in Abacus' "description" field. To search for the phrase "financial markets" in the "title" field, wrap the phrase in double quotation marks: `title:"financial markets"`.

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

**Range syntax** is denoted in Abacus as `[ TO ]`, where both a lower and upper bound are specified. Different types of brackets indicate whether these bounds are inclusive or exclusive. Square brackets `[]` represent inclusive lower and upper bounds, whereas curly brackets `{}` represent exclusive bounds. These can be combined within a single query: `{1956-02-16 TO 1988-05-03]`.

The current time can be represented using the special value `NOW`, while an asterisk `*` represents either the earliest or most recent data deposit, depending on its location within a query. Thus, entering `[* TO 2001-09-11}` would return all matched objects from the earliest in the repository up to (but excluding) 11 September 2001, whereas entering `[2001-09-11 TO *]` would return all matched objects from (and including) 11 September 2001 up to the most recent related deposit.

> **Truncation:** Users do not need to specify complete dates and times to search using date ranges. For instance, a search using the date range `[1956 TO 1998-05]` will produce relevant items from (and including) 1 January 1956 through 31 May 1998.
