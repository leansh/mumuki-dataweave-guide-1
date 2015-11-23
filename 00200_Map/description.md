From the [docs](https://docs.mulesoft.com/mule-user-guide/v/3.7/dataweave-reference-documentation#operators):
>The map operation returns an array that is the result of applying a transformation function (lambda) to each of the elements in an array.

So in other words: it receives an `array` and returns a `transformed array` (with the same amount of elements)

For example:
```ruby
users: ["jhon", "petter", "mat"] map upper $
```
 returns (in JSON):
```ruby
{
  "users": ["JHON", "PETTER", "MAT"]
}
```
In the previous example we are applying the `upper` function to each element in the users array.<br/>
Note that to refer to the array element under iteration we use the symbol **$**.<br/>
You can also name the lambda parameters like this:
```ruby
users: ["jhon", "petter", "mat"] map upper ((name, index) -> upper name)
```

>Write a script that outputs an array of objects like the following, with `id` values from 1 to 10:
```ruby
[
  {id: 1},
  {id: 2},
  ...
]
```
