# Grupos Dinámcos

Crear dynamic group

```
DGCoderepo
ALL {resource.type = 'devopsrepository', resource.compartment.id = 'ocid1.compartment.oc1..XXXXX'}

DGDeploy
All {resource.type = 'devopsdeploypipeline', resource.compartment.id = 'ocid1.compartment.oc1..XXXXX'}

DGBuild
ALL {resource.type = 'devopsbuildpipeline', resource.compartment.id = 'ocid1.compartment.oc1..XXXXX'}

DGConnection	
ALL {resource.type = 'devopsconnection', resource.compartment.id = 'ocid1.compartment.oc1..XXXXX'}	

```

# Policy

Compartment root:
```
Allow dynamic-group DGBuild to manage repos in tenancy
```

Compartment de proycto
```
Allow dynamic-group DGCoderepo to manage devops-family in compartment id ocid1.compartment.oc1..XXXXX
Allow dynamic-group DGBuild to manage repos in compartment id ocid1.compartment.oc1..XXXXX
Allow dynamic-group DGBuild to read secret-family in compartment id ocid1.compartment.oc1..XXXXX
Allow dynamic-group DGBuild to manage devops-family in compartment id ocid1.compartment.oc1..XXXXX
Allow dynamic-group DGBuild to manage generic-artifacts in compartment id ocid1.compartment.oc1..XXXXX
Allow dynamic-group DGBuild to use ons-topics in compartment id ocid1.compartment.oc1..XXXXX
Allow dynamic-group DGCoderepo to read secret-family in compartment id ocid1.compartment.oc1..XXXXX
Allow dynamic-group DGDeploy to manage all-resources in compartment id ocid1.compartment.oc1..XXXXX
Allow dynamic-group DGConnection to read secret-family in compartment id ocid1.compartment.oc1..XXXXX
```
