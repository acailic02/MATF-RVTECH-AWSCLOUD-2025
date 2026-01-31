# Strucni kurs RivianAWS

## Potrebne stvari za pokretanje:
- node.js i npm
- localstack
- awslocal cli
- serverless
- definisati .env fajl sa i njemu promenjive OCM_API_KEY, OCM_URL, CHARGERS_TABLE

## Uputstvo za build-ovanje i pokretanje:

1. Instalirati dependencije komandom:
   ```
   npm install
2. Pokrenuti lockalstack preko dokera komandom:
   ```
   docker compose up -d
3. Deploy-ovati serverless funkcije na localstack komandom:
   ```
   serverless deploy
4. Deploy-ovati/azurirati sajt na s3 bucket komandom:
   ```
   awslocal s3 sync ./web s3://punjaci-website
   #ili
   npm run deploy-frontend-fixed-bucket
5. Aplikacija radi na lokaciji: [http://punjaci-website.s3-website.localhost.localstack.cloud:4566/](http://punjaci-website.s3-website.localhost.localstack.cloud:4566/)
