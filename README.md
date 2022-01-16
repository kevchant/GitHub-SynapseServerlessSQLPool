# Azure Synapse Serverless SQL Pool Database Project using GitHub Actions

Example of a Migration-Based deployment that deploys to an Azure Synapse serverless SQL Pool using GitHub Actions. Based on a blog post I wrote called 'CI/CD for serverless SQL pools using GitHub Actions' (https://bit.ly/31sAPQx).

It uses a yaml pipeline, which in GitHub is called a workflow. You can find this file is in the '/.github/workflows' folder. 

For this pipeline you also need to setup the below encrypted secrets (https://bit.ly/3nd0Jj8)
  sqlinstance - Your Serverless SQL Pool endpoint (the one that ends with -ondemand)
  database - The database in the SQL Pool you want the update deployed to. Note it has to exist BEFORE this the scripts are run.
  UserName - User name to connect to the Serverless SQL Pool endpoint, try and keep this secret
  Pw - Password of above user, definitely keep this one secret

In order to use it in GitHub Actions you can either import or fork this repository into another GitHub repository.

Afterwards, you can select the yaml file in the GitHub repository and tailor the pipeline to suit your needs. Or, you can clone your repository locally and change the pure yaml file there.

Please note that the databases have to exist in the serverless SQL Pools for this to work. In addition, you might want to create a file in Azure Data Lake storage that contains the heading used for the SchemaVersions table (https://dbup.readthedocs.io/en/latest/more-info/journaling/). From there, you can try using it as the SchemaVersions table in the code.

This repository is provided "as is" based on the MIT license (https://opensource.org/licenses/MIT). Basically, I am not responsible for your use of it.
