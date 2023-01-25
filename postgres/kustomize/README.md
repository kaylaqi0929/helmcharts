# Postgres

# Configuration
Relies on three environment variables in order to build the kubernetes Secret. The env.template file so far demonstrates setting six vars, POSTGRES_DB, POSTGRES_GENERAL_DATABASE, POSTGRES_ADMIN, POSTGRES_PASSWORD, POSTGRES_GENERAL_USERNAME, and POSTGRES_GENERAL_PASSWORD. 
Copy the template and create a custom env file to set the vars.

cp env/env.template env/mydeployment.env
# Deployment

source env/mydeployment.env

kustomize build . | kubectl apply -f -
oc kustomize | oc apply -f -

To deploy in ArgoCD.

# Connecting to Postgres server
  select Topology in OpenShift;
  
  select postgres-server-0;
  
  select tab Terminal;
  
  run command: psql -U postgres.
  
For more psql commands, refer to https://www.geeksforgeeks.org/postgresql-psql-commands/.
