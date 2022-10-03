# rust-json-input-validation

An example for doing basic JSON input validation with Rust, using warp.

Run with `cargo run` and then:


For basic, and improved JSON parse handling:

```bash
curl -X POST http://localhost:8080/create-basic -H "Content-Type: application/json" -d '{ "email": 1, "address": { "street": "indiranagar", "street_no": 1 }, "pets": [{ "name": "ludo" }] }'

curl -X POST http://localhost:8080/create-path -H "Content-Type: application/json" -d '{ "email": 1, "address": { "street": "indiranagar", "street_no": 1 }, "pets": [{ "name": "ludo" }] }'
```

And for validating the outcoming struct:

```bash
curl -X POST http://localhost:8080/create-validator -H "Content-Type: application/json" -d '{ "email": "abcd@example.com", "address": { "street": "indiranagar", "street_no": 1 }, "pets": [{ "name": "" }] }'
```
