## Summary
Github Action that sets a parameter in AWS param store based on a flag value in Flagsmith. 
AWS credentials are fetched from the environment for security reasons. 

### Inputs
1. FLAG_NAME: name of feature flag on flagsmith and parameter on AWS
2. FLAGSMITH_ENV_KEY: flagsmith server-side environment key used to get the feature flag.

### Outputs
1. FLAG_VALUE: value of the feature flag fetched from flagsmith. Will not be set if the flag doesn't exist or can't be retreived.
2. PARAM_VERSION: version number obtained from AWS after setting the parameter, if returned by AWS.