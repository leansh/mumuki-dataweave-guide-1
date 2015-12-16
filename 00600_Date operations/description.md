In this lesson we'll see some examples of how to parse and format dates in DataWeave.<br/>
Dates in DataWeave follow the [ISO-8601](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html) standard and are defined between '|' characters.

Read about the dates [here](https://docs.mulesoft.com/mule-user-guide/v/3.7/dataweave-reference-documentation#dates).
<br/>
For more examples go to [this page](http://userguide.icu-project.org/formatparse/datetime).

* date => `|2003-10-01|`
* time => `|23:59:56|`
* datetime => `|2005-06-02T15:10:16Z|`
* localdatetime =>`|2005-06-02T15:10:16|`
* period => `|PT9M| => 9 minutes` / `|P1Y| => 1 Year`
* timeZone => `|-08:00|`

##### Parsing a date string
This is how you convert a date string to the dataweave internal date representation.
The result is the date `|1989-07-23|`
```
"23 07 1989" as :date {format: "dd MM yyyy"}
```

##### Converting a date to a string with a format
The result is the string `"23 Jul 1989"`
```
|1989-07-23| as :string {format: "dd MMM yyyy"}
```

>Given a JSON input like the following, write a script to change the format of the dates from `July 23, 1989` to `1989/07/23`.

```JSON
[
  {
    "user": "El Captain",
    "birthday": "February 19, 1985"
  },
  {
    "user": "El Coca",
    "birthday": "October 04, 1992"
  }
]
```

Use the variable `payload` to reference this input.
