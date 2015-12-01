The `filter` operation takes an array and returns an array with the elements that pass the criteria specified in the lambda.

For example:

```ruby
users: ["jhon", "petter", "mat"] filter ($ contains "t")
```
 returns (in JSON):

```json
{
  "users": ["petter", "mat"]
}
```

The **lambda** behaves exactly like in the example with `map`.<br/>
You can also name the lambda parameters like this:

```ruby
users: ["jhon", "petter", "mat"] filter ((name, index) -> name contains "t")
```

>Write a script to filter an array like the following one so that only the objects with `id` between 8 and 18 remain:<br/>
(To refer to this input use the variable named `payload`)

```json
[
  {"id": 5, "name": "Jorge"},
  {"id": 10, "name": "Matias"},
  {"id": 15, "name": "Mariano"},
  {"id": 20, "name": "Alejo"}
]
```
