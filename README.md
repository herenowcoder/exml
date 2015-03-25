Exml
====

```elixir
xml = """
<?xml version="1.0" encoding="UTF-8"?>
<bookstore>
    <book>
        <title lang="en">Harry Potter</title>
        <price>29.99</price>
    </book>
    <book>
        <title lang="en">Learning XML</title>
        <price>39.95</price>
    </book>
</bookstore> 
"""

doc = Exml.parse xml

Exml.get doc, "//book[1]/title/@lang"
#=> "en"

Exml.get doc, "//title"
#=> ["Harry Potter", "Learning XML"]
```

See http://www.w3schools.com/xpath/xpath_syntax.asp
