# suricata-rule

- 20개 페이지에 대한 rule 작성
- http / https에 대한 테스트 진행

## example http(80)

```
alert tcp any any -> any 80 (msg:"[80]kitribob.wiki access"; content:"GET /"; content:"Host: "; content:"kitribob.wiki"; sid:10004; rev:1;)
```

## example https(443)

```
alert tcp any any -> any 443 (msg:"[443]kitribob.wiki access"; flow:to_server, established; content:"kitribob.wiki"; sid:20001; rev:3;)
```