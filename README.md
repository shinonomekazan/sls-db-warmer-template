# sls-db-warmer-template
Template for Serverless Framework project of scheduled lambdas to warm Aurora Serverless databases using auto pause

## Usage

1. Install depenencies

```
npm i
```

2. Add database configuration/AWS credentials to `./env/.env`

- `.env` file will be read by default. If you need variables for multiple environments, create separate `.env` files for each `--stage`. (i.e. `sls deploy --stage production` will use `.env` by default, and also look for `.env.production`) Read more about the serverless dotenv plugin here: https://www.serverless.com/plugins/serverless-dotenv-plugin

3. Modify `./src/handler.ts` file with details for database(s) to warm.

4. Set schedule in `./serverless-settings/schedules.yml`

5. Run locally

```
npm run start:sls
```

6. Deploy
```
npm run deploy
```