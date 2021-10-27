# Reproduction case for serverless/serverless#10167

## Steps

1. `npm install && npm run deploy`
2. Check in CloudWatch: The 'test' function should have produced 2 log streams for a version, both saying "Initialized"
3. Upload a file into the bucket
4. Check in CloudWatch: The 'test' function now has a new log stream for the `$LATEST` version which also contains the request caused by the upload
