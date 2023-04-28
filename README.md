This chart requires the use of the helm-kubectl plugin to enable secrets retrieval on ArgoCD, as of April 2023. 

Alternatively, you can specify values by hand for 
`global.customer.edge_db_password` and `global.customer.delta_db_password`.

Here's an example of deploying Edge:
`helm template . --set-file=global.customer.edge_db_password=kubectl://customer-testcustomer/secret/edge.dbfws.credentials.postgresql.acid.zalan.do/jsonpath={.data.password} --debug`