# Sample tests to demo the Playwright Listener

## Install dependencies
````shell
npm install
````

### Configure Orangebeard reporter
Ensure that: `reporter: [['@orangebeard-io/playwright-orangebeard-reporter']]` is configured in playwright.config.ts  
  
Create orangebeard.json:
```shell
{
	"endpoint": "https://app.orangebeard.io/[ORGANIZATION]",
	"token": "[LISTENER_TOKEN]",
	"project": "example-project",
    "testset": "Playwright Demo",
    "description": "Playwright run",
    "attributes": [
      {
        "key": "Tool",
        "value": "Playwright"
      }
    ],
    "referenceUrl": "https://docs.orangebeard.io/"
}
```

__It's good practice__ to omit the token from the json file and get it from your env:

Windows cmd:
```
set orangebeard_token=[LISTENER TOKEN]
```
Linux/Mac:
```
export orangebeard_token=[LISTENER TOKEN]
```

### Run the tests

````shell
npm run test
```
