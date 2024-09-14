library(rvest)
url <- "https://web.archive.org/web/20181024132313/http://www.stevetheump.com/Payrolls.htm"
h <- read_html(url)
# We learned that tables in html are associated with the table node.  Use the html_nodes() function and the table node type to extract the first table. Store it in an object nodes:

nodes <- html_nodes(h, "table")

# The html_nodes() function returns a list of objects of class xml_node. We can see the content of each one using, for example, the html_text() function. You can see the content for an arbitrarily picked component like this:

html_text(nodes[[8]])

html_table(nodes[[8]])


# To lear this is a seful web: https://statsandr.com/blog/web-scraping-in-r/

