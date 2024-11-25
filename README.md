
# Build and Deploy Gen AI Applications on Google Cloud with Genkit and Go Workshop

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
git remote add origin "git@github.com:${GITHUB_USERNAME}/codelab-genai.git"
git add .
git commit -m "add http server"
git push -u origin main
# Connect Cloud Build to the repo
# Setup Cloud Run
echo -e "\n\nOnce the build finishes, visit your live application:\n \
    "$( \
        gcloud run services list | \
        grep codelab-genai | \
        awk '/URL/{print $2}' | \
        head -1 \
    )" \n\n"
```