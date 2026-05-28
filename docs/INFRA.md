 # Infrastructure Overview — winitapp
_Last updated: 2026-05_

## Vercel

| Project | Framework | Domain | Branch |
|---------|-----------|--------|--------|
| winit-webapp | nextjs | www.divorcelookup.com | master |
| attorney-portal | nextjs | admin.appwinit.com | master |
| winit-platform-appwinit | nextjs | web.appwinit.com | main |
| winitlaw | nextjs | winitlaw.com | main |
| winit-dashboard | nextjs | winit-fetcher-dashboard.vercel.app | master |
| doc-ai-client | vite | doc-ai-client-staging-winit-dev.vercel.app | main |

## AWS

### winit-company (us-east-1)
**CloudFormation stacks**  
*No active stacks documented*

### ouriel-a1 (us-east-1)
**CloudFormation stacks**  
*No active stacks documented*

### ouriel-lemmel (us-east-1)
**CloudFormation stacks**  
*No active stacks documented*

## Heroku

| App | Region | Stack | URL |
|-----|--------|-------|-----|
| attorney-backend-production | us | heroku-22 | https://attorney-backend-production.herokuapp.com/ |
| attorney-backend-staging | us | heroku-22 | https://attorney-backend-staging.herokuapp.com/ |
| parkingpay-api-prod | us | heroku-22 | https://parkingpay-api-prod.herokuapp.com/ |
| parkingpay-api-staging | us | heroku-22 | https://parkingpay-api-staging.herokuapp.com/ |
| sms-api-prod | us | heroku-22 | https://sms-api-prod.herokuapp.com/ |
| sms-api-staging | us | heroku-22 | https://sms-api-staging.herokuapp.com/ |
| winit-admin-site | us | heroku-20 | https://winit-admin-site.herokuapp.com/ |
| winit-admin-site-staging | us | heroku-20 | https://winit-admin-site-staging.herokuapp.com/ |
| winit-api-staging | us | heroku-22 | https://winit-api-staging.herokuapp.com/ |
| winit-jobs-production | us | heroku-22 | https://winit-jobs-production.herokuapp.com/ |
| winit-parse-dashboard | us | heroku-24 | https://winit-parse-dashboard.herokuapp.com/ |
| winit-production | us | heroku-22 | https://winit-production.herokuapp.com/ |
| wi-par-prox-prod | us | heroku-22 | https://wi-par-prox-prod.herokuapp.com/ |
| wi-par-prox-staging | us | heroku-22 | https://wi-par-prox-staging.herokuapp.com/ |

**Addons**
- heroku-redis
- newrelic
- scheduler

## Netlify

*No active sites found.*

## Summary

The winitapp organization runs a split-platform architecture: **Vercel** hosts the public-facing Next.js frontend applications (including marketing sites, admin portals, and dashboards), while **Heroku**
