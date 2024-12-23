

Create a GCP project with billing enabled

Clone git repo with template terraform modules
```git clone https://github.com/gautierc-thelio/solutions-terraform-cloudbuild-gitops.git```

Create the bucket for terraform backend

```gsutil mb -c standard -l europe-west9 gs://${PROJECT_ID}-tfstate```

Enable object versioning
```gcloud storage buckets update gs://${PROJECT_ID}-tfstate --versioning```