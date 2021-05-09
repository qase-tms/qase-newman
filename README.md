## THIS REPO IS DEPRECATED. IT WAS MOVED [HERE](https://github.com/qase-tms/qase-javascript/tree/master/qase-newman)

---

# Qase Newman Reporter

Install reporter:
```bash
npm install -g newman-reporter-qase
```

## Usage

### Define in tests
```js
//qase: 10
// Qase: 1, 2, 3
// qase: 4 5 6 14
pm.test('expect response be 200', function () {
    pm.response.to.be.info
})
```

### From CLI:
```bash
QASE_RUN_ID=34 # Specify Run ID using ENV
newman run \
    -r qase \ # Enable Qase logger
    --reporter-qase-logging \ # Use reporter logger (like debug)
    --reporter-qase-projectCode PRJCODE \ # Specify Project Code
    --reporter-qase-apiToken <api token> \ # Specify API token
    --reporter-qase-runId 34 \ # Specify Run ID using CLI parameters
    -x # WA for issue https://github.com/postmanlabs/newman/issues/2148#issuecomment-665229759
```
