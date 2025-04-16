# Playwright sample project

## Install dependencies
````shell
npm install
````

## Configure Orangebeard
Ensure that: `reporter: [['@orangebeard-io/playwright-orangebeard-reporter']]` is configured in playwright.config.ts  
  
Create orangebeard.json:
```shell
{
	"endpoint": "https://praegus.orangebeard.app",
	"token": "<LISTENER_TOKEN>",
	"project": "<PROJECT>",
	"testset": "Playwright test examples",
	"description": "A run from playwright",
	"attributes": [
		{
			"key": "Commit",
			"value": "a375342a"
		},
		{
			"value": "Demo"
		}
	],
	"referenceUrl": "https://gitlab.com/orangebeard-io/listener-api/-/pipelines/1637473171"
}
```

## Run tests

````shell
npm run test
```
