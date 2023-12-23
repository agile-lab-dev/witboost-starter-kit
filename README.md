<br/>
<p align="center">
    <a href="https://www.agilelab.it/witboost">
        <img src="docs/img/witboost_logo.svg" alt="witboost" width=600 >
    </a>
</p>
<br/>

Designed by [Agile Lab](https://www.agilelab.it/), Witboost is a versatile platform that addresses a wide range of sophisticated data engineering challenges. It enables businesses to discover, enhance, and productize their data, fostering the creation of automated data platforms that adhere to the highest standards of data governance. Want to know more about Witboost? Check it out [here](https://www.agilelab.it/witboost) or [contact us!](https://www.agilelab.it/contacts)

This repository is a guide to our Starter Kit meant to showcase Witboost's integration capabilities and provide a "batteries-included" product.

# Witboost Starter Kit

- [Provisioners](#provisioners)
- [Templates](#templates)

## Provisioners

### What's a Specific Provisioner?

A Specific Provisioner is a microservice which is in charge of deploying components that use a specific technology. When the deployment of a Data Product is triggered, the platform generates it descriptor and orchestrates the deployment of every component contained in the Data Product. For every such component the platform knows which Specific Provisioner is responsible for its deployment, and can thus send a provisioning request with the descriptor to it so that the Specific Provisioner can perform whatever operation is required to fulfill this request and report back the outcome to the platform.

You can learn more about how the Specific Provisioners fit in the broader picture [here](https://docs.witboost.agilelab.it/docs/p2_arch/p1_intro/#deploy-flow).

### Available Specific Provisioners and Scaffolds

We provide two main kinds of projects:
- Provisioners: these are actual implementations for a specific technology that you can customize to suit your needs
- Scaffolds: these are projects that you can start from if you want to implement a provisioner yourself

| Kind        | Project                                                                                  | Technology                | Supported components      | Notes                                                                                                                                |
|-------------|------------------------------------------------------------------------------------------|---------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Provisioner | [MWAA SP](https://github.com/agile-lab-dev/witboost-mwaa-specific-provisioner)           | Scheduling - Airflow/MWAA | Workload                  |                                                                                                                                      |
| Provisioner | [Hasura SP](https://github.com/agile-lab-dev/witboost-hasura-specific-provisioner)       | GraphQL - Hasura          | Output Port               | Needs the [Hasura Authentication Webhook and Role Mapper](https://github.com/agile-lab-dev/witboost-hasura-auth-webhook-role-mapper) |
| Provisioner | [Snowflake SP](https://github.com/agile-lab-dev/witboost-snowflake-specific-provisioner) | DWH - Snowflake           | Output Port, Storage Area |                                                                                                                                      |
| Scaffold    | [Python Scaffold](https://github.com/agile-lab-dev/witboost-python-scaffold)             | Generic - Python          | NA                        |                                                                                                                                      |
| Scaffold    | [Terraform Scaffold](https://github.com/agile-lab-dev/witboost-terraform-scaffold)       | Generic - Terraform       | NA                        |                                                                                                                                      |

## Templates

### What's a Template?

A Template is a tool that helps create components inside a Data Mesh. Templates help establish a standard across the organization. This standard leads to easier understanding, management and maintenance of components. Templates provide a predefined structure so that developers don't have to start from scratch each time, which leads to faster development and allows them to focus on other aspects, such as testing and business logic.

For more information, please refer to the [official documentation](https://docs.witboost.agilelab.it/docs/p1_user/p6_advanced/p6_1_templates/#getting-started).

### Available Templates

| Component    | Project                                                                                             | Technology                | Specific Provisioner                                                                     | Notes |
|--------------|-----------------------------------------------------------------------------------------------------|---------------------------|------------------------------------------------------------------------------------------|-------|
| Data Product | [Data Product](https://github.com/agile-lab-dev/witboost-data-product-template)                     | NA                        | No Specific Provisioner needed                                                           |       |
| Output Port  | [Hasura Output Port](https://github.com/agile-lab-dev/witboost-hasura-output-port-template)         | GraphQL - Hasura          | [Hasura SP](https://github.com/agile-lab-dev/witboost-hasura-specific-provisioner)       |       |
| Output Port  | [Snowflake Output Port](https://github.com/agile-lab-dev/witboost-snowflake-output-port-template)   | DWH - Snowflake           | [Snowflake SP](https://github.com/agile-lab-dev/witboost-snowflake-specific-provisioner) |       |
| Storage Area | [Snowflake Storage Area](https://github.com/agile-lab-dev/witboost-snowflake-storage-area-template) | DWH - Snowflake           | [Snowflake SP](https://github.com/agile-lab-dev/witboost-snowflake-specific-provisioner) |       |
| Workload     | [DBT Workload](https://github.com/agile-lab-dev/witboost-dbt-workload-template)                     | Data processing - DBT     | No Specific Provisioner needed                                                           |       |
| Workload     | [MWAA Workload](https://github.com/agile-lab-dev/witboost-mwaa-workload-template)                   | Scheduling - Airflow/MWAA | [MWAA SP](https://github.com/agile-lab-dev/witboost-mwaa-specific-provisioner)           |       |

## License

This project is available under the [Apache License, Version 2.0](https://opensource.org/licenses/Apache-2.0); see [LICENSE](LICENSE) for full details.

## About us

<br/>
<p align="center">
    <a href="https://www.agilelab.it">
        <img src="docs/img/agilelab_logo.svg" alt="Agile Lab" width=600>
    </a>
</p>
<br/>

Agile Lab creates value for its Clients in data-intensive environments through customizable solutions to establish performance driven processes, sustainable architectures, and automated platforms driven by data governance best practices.

Since 2014 we have implemented 100+ successful Elite Data Engineering initiatives and used that experience to create Witboost: a technology-agnostic, modular platform, that empowers modern enterprises to discover, elevate and productize their data both in traditional environments and on fully compliant Data mesh architectures.

[Contact us](https://www.agilelab.it/contacts) or follow us on:
- [LinkedIn](https://www.linkedin.com/company/agile-lab/)
- [Instagram](https://www.instagram.com/agilelab_official/)
- [YouTube](https://www.youtube.com/channel/UCTWdhr7_4JmZIpZFhMdLzAA)
- [Twitter](https://twitter.com/agile__lab)
