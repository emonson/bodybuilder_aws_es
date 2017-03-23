## bodybuilder_aws_es

I wanted to make a minimal functional example of faceted search of an 
[Elasticsearch](https://www.elastic.co/)
(ES) database stored in 
[AWS ES](https://aws.amazon.com/elasticsearch-service/)
using basic HTML and JavaScript. The queries (JSON) are built using 
[bodybuilder](http://bodybuilder.js.org/),
which makes it much much easier to compose the queries to the ES JSON API.

This particular example searches a database of
US intellectual property (IP) court cases from 1900-2010 or so.
The query string will get parsed, so you can put more complicated search terms using
`AND`, `OR`, and `field:term` combinations, as well as proximity searches like
`"image appropriation"~5`. See the documentation for the 
[Lucene Query Parser Syntax](https://lucene.apache.org/core/2_9_4/queryparsersyntax.html)
for more details.

Click on facets to apply them as filters. Then, click on an applied facet filters
below the search bar to remove that filter. A new search clears out any facets.

Note: This uses a Prev - Next pager for navigating results, but there is a 
more complete pagination example in the "pagination" branch.
