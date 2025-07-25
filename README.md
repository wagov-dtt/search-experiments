# Google Cloud Search Interface

Simple static frontend for Google Cloud's Discovery Engine Search API.

## Setup

1. **Open [Google Cloud Shell](https://shell.cloud.google.com)**

2. **Set your project and get a token:**
   ```bash
   gcloud config set project YOUR_PROJECT_ID
   gcloud services enable discoveryengine.googleapis.com
   gcloud auth print-access-token
   ```

3. **Open the interface:** https://wagov-dtt.github.io/search-experiments/

4. **Fill in the form:**
   - Project ID: `YOUR_PROJECT_ID`
   - Data Store ID: `YOUR_DATASTORE_ID`
   - Location: `global` (usually)
   - Serving Config: `default_config` (usually)
   - Access Token: (paste the token from step 2)

5. **Click "Copy Config URL" to share**

## Token Refresh

Tokens expire after 1 hour. To get a new one:

```bash
gcloud auth print-access-token
```

Then update the token field in the interface.

## Notes

- Uses Google Cloud Shell (no local installation needed)
- Tokens are temporary and secure
- Static interface works from any web browser
- Create your search data store at: https://console.cloud.google.com/gen-app-builder
