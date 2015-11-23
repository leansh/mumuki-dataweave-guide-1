In this lesson we'll learn about DataWeave types.

The available types are:
* string => `"foo"` or `'foo'`
* number => `123`
* date => `|2003-10-01|`
* datetime => `|2005-06-02T15:10:16Z|`
* localdatetime =>`|2005-06-02T15:10:16|`
* array => `["a", "b", "c"]`
* range => `[1..3]` This generates the array `[1, 2, 3]`
* object<br/>

An object is a collection of key-value pairs and it's defined like this:
```ruby
{
  foo: "bar"
}
```

Our object has a key `foo` with value `bar`

>Now try to define an object with a key `name` and value `Mariano`
