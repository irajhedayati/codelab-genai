
```bash
gcloud config set account iraj.hedayati@gmail.com
gcloud auth login
gcloud config set project dataedu-web
gcloud auth application-default login --project=dataedu-web
gcloud services enable run.googleapis.com cloudbuild.googleapis.com aiplatform.googleapis.com
mkdir codelab-genai
cd codelab-genai
go mod init codelab-genai
# add main.go
git init -b main
git config user.email "iraj.hedayati@gmail.com"
git config user.name "Iraj Hedayati"
GITHUB_USERNAME="irajhedayati"
git remote add origin "https://github.com/${GITHUB_USERNAME}/codelab-genai"
```