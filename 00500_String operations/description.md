The available string operations are: (for more info [read this](https://docs.mulesoft.com/mule-user-guide/v/3.7/dataweave-reference-documentation#string))

* range selector => `"A very long string"[0..8]` => `"A very lo"`
* index selector => `"A very long string"[10]` => `"g"`
* sizeOf => `sizeOf "foo"` => `3`
* contains => `"foo" contains "o"` => `true`
* matches => `"Mariano long string" matches /^Mariano.*/` => `true`
* match => `"aabccd" match /(a).(b)(c.)d/` => `["aabccd","a","b","cc"]`
* find => `"aabccde" find /(a).(b)(c.)d/` => `[[0, 0, 2, 3]]`
* scan => `"EmiEmi" scan /(mi)/` => `[["mi","mi"],["mi","mi"]]`
* splitBy: <br/>
`"A very long string" splitBy /\s/` => `["A", "very", "long", "string"]`<br/>
`"A very long string" splitBy " "` => `["A", "very", "long", "string"]`
* joinBy => `["a","b","c"] joinBy "-"` => `"a-b-c"`
* trim => `trim "   abc   "` => `"abc"`
* upper => `upper "abc"` => `"ABC"`
* lower =>`lower "ABC"` => `"abc"`
* startsWith => `"Mariano" startsWith "Mar"` => `true`
* endsWith => `"Emiliano" endsWith "no"` => `true`

>Given an input array of words, write a script that outputs an array of strings with the words that have 5 or more letters.<br/>
Use the variable `payload` to reference the given input.

**NOTE**: When chaining multiple operations you'll probably have to use **parenthesis** to enclose your expressions, depending on the precedence of the used operators.

E.g. <br/>
`"foo,DataWeave,bar,rocks" => ["DataWeave", "rocks"]`
