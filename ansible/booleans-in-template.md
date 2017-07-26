# Boolean in templates

So I have a variable:

```yaml
vars:
  bool_var: true
```

And I want to use it in a template to generate json file:

```
{
  "bool_val": {{ bool_var }}
}
```

Expected result is quite obvious:

```json
{
  "bool_val": true
}
```

But because ansible is in Python it will print it in a different way:

```json
{
  "bool_val": True
}
```

which is invalid json. There are at least two solutions:

```
{{ bool_var | to_json }}
```

which will generate:

```json
{
  "bool_val": "true"
}
```

As a result we got string which might not fit our need. Alternative:

```
{{ bool_var | lower }}
```

and finally result is equal to expected one:

```json
{
  "bool_val": true
}
```

