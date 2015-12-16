In this lesson we'll see how to manipulate strings in DataWeave.<br/>
The available string operations are: <br/>

* range selector => `"A very long string"[0..8]` => `"A very lo"`
* index selector => `"A very long string"[10]` => `"g"`
* sizeOf => `sizeOf "foo"` => `3`
* contains => `"foo" contains "o"` => `true`
* splitBy: `"john smith" splitBy " "` => `["john", "smith"]`
* joinBy => `["a","b","c"] joinBy "-"` => `"a-b-c"`
* trim => `trim "   abc   "` => `"abc"`
* upper => `upper "abc"` => `"ABC"`
* lower =>`lower "ABC"` => `"abc"`
* startsWith => `"Mariano" startsWith "Mar"` => `true`
* endsWith => `"Emiliano" endsWith "no"` => `true`

(for more info [read this](https://docs.mulesoft.com/mule-user-guide/v/3.7/dataweave-reference-documentation#string))

>Given a string of comma separated words, write a script that outputs an array with the words that have 5 or more letters.<br/>
Use the variable `payload` to reference the given input.

E.g. <br/>
`"foo DataWeave bar rocks" => ["DataWeave", "rocks"]`

**NOTE**: When chaining multiple operations you'll probably have to use **parenthesis** to enclose your expressions, depending on the precedence of the operators used.
