# MLOps Car Price Predictor

Full CI/CD deployment with GitHub Actions.

## Architecture

```
This Repo
|-- backend/           -> GitHub Action -> Azure Function App (mlops-predict-cicd-7811)
|-- frontend/          -> GitHub Action -> Azure Static Web App
|-- .github/workflows/
|   |-- deploy-backend.yml   (triggers on backend/ changes)
|   |-- deploy-frontend.yml  (triggers on frontend/ changes)
```

## URLs
- **Frontend:** https://kind-wave-04f059600.7.azurestaticapps.net
- **Backend API:** https://mlops-predict-cicd-7811.azurewebsites.net/api

## How to Update
- Edit `frontend/index.html` -> push -> frontend auto-deploys
- Edit `backend/function_app.py` -> push -> backend auto-deploys
