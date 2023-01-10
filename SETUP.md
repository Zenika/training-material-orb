# Setup

## Google Cloud Service Account

In the project `zen-formations` on Google Cloud:

1. Create a service account (e.g. `training-deploy`)
2. As recommended in [doc](https://cloud.google.com/appengine/docs/flexible/roles#recommended_role_for_application_deployment), give the SA the roles:
    - App Engine Deployer (`roles/appengine.deployer`)
    - Service Account User (`roles/iam.serviceAccountUser`)
    - Storage Object Admin (`roles/storage.objectAdmin`)
    - Cloud Build Editor (`roles/cloudbuild.builds.editor`)
3. Also add role App Engine Service Admin (`roles/appengine.serviceAdmin`)
4. Create a JSON key for the SA

## CircleCI context

In CircleCI Zenika & Zenika-Training organizations' settings:

1. Create a context `training-deploy-zenika`
2. Add environment variable:
    - Name: `GAE_KEY_FILE_CONTENT`
    - Value: the bare content of the JSON key of the SA
