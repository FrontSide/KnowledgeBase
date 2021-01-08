
From a list of json objects (array of objects or jsonl file) show only certain fields for each objects but keep it in json format
e.g. For each object in a jsonl file users.jsonl, show the name, address and age of each user (do not output any other fields).

```
$ cat users.jsonl | jq -r '{name, address, age}'

{
"name": "Mr Man",
"address": "1 Street",
"age": 34
}
{
"name": "Mrs Woman",
"address": "2 Road",
"age": 46
}

```

To only output the raw values for each field use
```
$ cat users.jsonl | jq -r '.name, .address, .age'

Mr Man
1 Street
34
Mrs Woman
2 Road
46
```
