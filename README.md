# Azure Synapse Serverless SQL Pool Database Project using GitHub Actions

Example of a Migration-Based deployment that deploys to an Azure Synapse serverless SQL Pool using GitHub Actions.

It uses a yaml pipeline, which is in the '/.github/workflows' folder.

In order to use it in GitHub Actions you can either import or fork this repository into another GitHub repository.

Afterwards, you can select the yaml file in the GitHub repository and tailor the pipeline to suit your needs. Or, you can clone your repository locally and change the pure yaml file there.

Please note that the databases have to exist in the serverless SQL Pools for this to work. In addition, you might want to create a file in Azure Data Lake storage that contains the heading used for the SchemaVersions table (https://dbup.readthedocs.io/en/latest/more-info/journaling/). From there, you can try using it as the SchemaVersions table in the code.

This repository is provided "as is" based on the MIT license (https://opensource.org/licenses/MIT). Basically, I am not responsible for your use of it.
