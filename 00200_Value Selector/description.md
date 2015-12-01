The way to navigate structures in DW is by using **Selector Expressions**.
The available selectors are:
* Single-value selector `<object>.<key-name>`
* Multi-value selector `<object>.*<key-name>`
* Descendants selector `<object>..<key-name>`
* Indexed selector `<object>[<index>]`
* Expression selector `<object>[?(<filter-expression>)]`

In this lesson we'll see the **single-value** selector.<br/>
This selector returns the **first value** whose **key matches the expression**
```json
{
  "name": "Nial",
  "address": {
    "street": {
      "name": "Italia",
      "number": 2164
    },
    "area": {
      "zone": "San Isidro",
      "name": "Martinez"
    }
  }
}
```
Let's call the previous json input `payload`. To retrieve the `street name`("Italia"), we'd have to do:
```ruby
payload.address.street.name
```
>Now try to get the `area name`("Martinez") using single-value selectors
