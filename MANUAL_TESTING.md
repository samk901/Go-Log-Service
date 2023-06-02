## Chapter 1 Testing
- Run main.go, http server will start up on localhost:8080
- Use curl to add some records to our log
```
curl -X POST localhost:8080 -d '{"record": {"value": "TGV0J3MgR28gIzEK"}}'
curl -X POST localhost:8080 -d '{"record": {"value": "TGV0J3MgR28gIzIK"}}'
curl -X POST localhost:8080 -d '{"record": {"value": "TGV0J3MgR28gIzMK"}}'
```
Should see offset being incremented as our store grows
Use GET to grab records
```
curl -X GET localhost:8080 -d '{"offset":1}'
```