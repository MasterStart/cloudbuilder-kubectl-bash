# kubectl-bash

This build step extends the [`kubectl`](https://github.com/GoogleCloudPlatform/cloud-builders/blob/master/kubectl/)
cloud builder for [Google Cloud Build](https://cloud.google.com/cloud-build/).

The default builder has an entry-point script which configures context to the cluster and then launches
the `kubectl` command with any arguments passed to the builder.

This builder uses the same entry-point script but launches the `bash` command with any arguments passed
to the builder.

This allows one to execute a bash script with multiple `kubectl` commands with the
cluster credentials configured.

## Building this builder

To build this builder, run the following command in this directory.

$ gcloud builds submit . --config=cloudbuild.yaml
