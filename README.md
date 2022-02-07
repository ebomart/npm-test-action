![img.shields.io](https://img.shields.io/badge/GITHUB-ACTION-blue?style=for-the-badge&logo=github)
![shell-script](https://img.shields.io/badge/Shell_Script-121011?style=for-the-badge&logo=gnu-bash&logoColor=white)

# NPM TEST 

## What is NPM-TEST-ACTION?

If there’s a package.json file in your project, you have the opportunity to include time-saving scripts for your development process. npm test, the most common example, is actually included by default when you initialize a new package.json file. Most Node.js based projects make use of this pattern, and it’s increasingly common for front-end projects, too

## Usage in your repo:

Add the below code in your repo:

```yaml
on: push
name: NPM test
jobs:
  npm-test:
    runs-on: ubuntu-latest
# Please copy the steps below this
    steps:
    - uses: actions/checkout@master

    - name: NPM test
      uses: ebomart/npm-test-action@main
      with:
        env_name: YOUR_ENV_NAME
        microservice_name: YOUR_VARIABLE_SERIVCE_NAME
```

The npm-test Action has a small number of properties which map to the parameters. These are passed to the action using with, as demonstrated with files in the above example.

| Property | Default   | Description  |   
|---        |---        |---|
| env_name      | -         | Pass the environment name ( npm test:$env_name )  |microservice_name
| microservice_name    | -    | Pass the service name you configured ( npm test:$env_name $microservice_name)  |
