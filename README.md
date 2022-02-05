# s3rpldemo

# Introduction

TODO: Testing aws S3 bucket replication using pipeline

#Steps:
Create repo in dummyProjects
Clone repo into own pc
Commit and push baseline project
In azure devops Pipelines>Pipelines (\_build) and using the no gui interface:

- Set build pipeline using the windows image
- Add steps
- Save and run
  In azure devops Pipelines>Releases (\_release):
- +New > New release Pipeline
- +Add Azure Repos tag: repos
- Set stages (dev,qa,prod)
- Add tasks to stage´s job
- Create release

First commit in develop branch

Replication references
Configuring replication for source and destination buckets owned by the same account

sls deploy --stage dev --region useast1

### Para recibir archivos en la cuenta propia desde la cuenta transversal:

- Cuenta transversal necesita tener el bucket con regla de replicación y un role con permisos para S3
- Cuenta propia necesita tener un bucket con versionamiento
- Cuenta propia necesita un bucketPolicy que haga referencia al bucket propio y referencia al role de la cuenta transversal

#Troubleshoot
Cambiar el destino a cross account y no same account
