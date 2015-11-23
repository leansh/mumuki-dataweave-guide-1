As we'll see later, all the elements present in other formats (XML, JSON, CSV, etc) are mapped to these data types.

For example:

```ruby
<names>
  <name>Mariano</name>
</names>
```
is equivalent to:

```ruby
{
  names: {
    name: "Mariano"
  }
}
```
