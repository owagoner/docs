---

copyright:
  years: 2015, 2017
lastupdated: "2017-2-13"

---
 
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Getting started with {{site.data.keyword.contdelivery_short}}
{: #cd_getting_started}

Adopt a DevOps approach by using {{site.data.keyword.contdelivery_full}}, which includes toolchains that automate the building and deployment of applications. You can get started by creating a simple deployment toolchain that supports development, deployment, and operations tasks. 
{: shortdesc}

After you create an instance of {{site.data.keyword.contdelivery_short}} by selecting it from the {{site.data.keyword.Bluemix_notm}} catalog, you can choose how you want to get started with the service.
 ![Continuous Delivery welcome page](images/cd_landing_page.png)

 * To get started quickly and deploy your application by using an automated pipeline, in the "Starting with a pipeline" section, click **[Start here](#starting_with_a_pipeline)**. You can add more tools later. 
 * To create and configure a continuous delivery toolchain from a template, in the "Starting from a toolchain template" section, click **[Start here](#starting_from_a_toolchain_template)**. The toolchain integrates tools for planning, developing, deploying pipelines, and managing your applications. You can always add or remove tools from your toolchains.
 * If you already have toolchains, in the "Starting from a toolchain template" section, click **View your toolchains**. For more information about working with toolchains, see [Using toolchains](/docs/services/ContinuousDelivery/toolchains_using.html){: new_window}.
 
**Tip**: Pipelines are managed by toolchains. If you create a pipeline and don't have any existing toolchains, a toolchain with a default name will be created for you. With the toolchain, you can expand the capabilities of your pipeline by integrating with other tools and services. 

##Starting with a pipeline
{: #starting_with_a_pipeline}

Pipelines automate builds, deployments, and more. To get started with an automated pipeline, select a template and provide the location of your GitHub repository (repo).

To [create a pipeline](https://console.ng.bluemix.net/devops/pipelines/dashboard/create){: new_window} ![External link icon](images/launch--glyph.svg) that is configured to deploy a Cloud Foundry application, follow these steps:

1. Click **Cloud Foundry**.
1. If you want to use a different name for the pipeline, change its default name. The pipeline's name identifies it in {{site.data.keyword.Bluemix_notm}}. 
1. If you want to use a different name for the application, change its default name. The application's name identifies it in {{site.data.keyword.Bluemix_notm}}. This name is the application that the pipeline deploys to. 
1. If you don't have a toolchain, a toolchain with a default name is created for you. If you want to use a different name for the toolchain, change its name. Pipelines are managed by toolchains. With the toolchain, you can extend the capabilities of your pipeline by integrating with other tools and services. 

 **Tip**: Pipelines and toolchains belong to organizations (orgs). If you belong to an org that has toolchains, you can use those toolchains even if you didn't create them.
 
1. Either select the toolchain that you want to use or type a name for the new toolchain that you want to create.
1. Provide the location of your GitHub or {{site.data.keyword.ghe_short}} repo.

 **Tip**: If you have not authorized {{site.data.keyword.Bluemix_notm}} to access GitHub, you are prompted to click **Authorize** to go to the GitHub website. If you don't have an active GitHub session, you are prompted to log in. Click **Authorize Application** to allow {{site.data.keyword.Bluemix_notm}} to access your GitHub account. If you have an active GitHub session but you haven't entered your password recently, you might be prompted to enter your GitHub password to confirm.
 
 If you are not authorized to access the {{site.data.keyword.ghe_short}} repo, someone who has admin privileges for the repo must add you. For instructions to authorize with {{site.data.keyword.Bluemix_notm}} Dedicated for {{site.data.keyword.ghe_short}}, see [Getting started with {{site.data.keyword.Bluemix_notm}} Dedicated for {{site.data.keyword.ghe_short}}](/docs/services/ghededicated/index.html){: new_window}. If you need to authorize with your own managed version of {{site.data.keyword.ghe_short}}, follow your internal procedures.

   * If you have a GitHub or {{site.data.keyword.ghe_short}} repo and want to use it, for the repository type, select **Link**. Search for the location of the repo or select the repo from the list of available repos.
   
   * If you want to create an empty GitHub or {{site.data.keyword.ghe_short}} repo, for the repository type, select **New**. Type a name for the repo.
   
   * If you want to create a clone of a GitHub or {{site.data.keyword.ghe_short}} repo, for the repository type, select **Copy**. Search for the location of the repo or select the repo from the list of available repos.
   
   * If you want to fork a GitHub or {{site.data.keyword.ghe_short}} repo so that you can contribute changes through pull requests, select **Fork**. Search for the location of the repo or select the repo from the list of available repos.
 
1. Click **Create**. The pipeline is created, configured, and displayed on the toolchain's Overview page. 
 ![Pipeline card](images/cd_pipeline.png)
 
To create an [empty pipeline](https://console.ng.bluemix.net/devops/pipelines/dashboard/create){: new_window} ![External link icon](images/launch--glyph.svg) without any preconfigured stages:

1. Click **Custom**.
1. If you want to use a different name for the pipeline, change its default name. The pipeline's name identifies it in {{site.data.keyword.Bluemix_notm}}. 
1. If you don't have a toolchain, a toolchain with a default name is created for you. If you want to use a different name for the toolchain, change its name. Pipelines are managed by toolchains. With the toolchain, you can extend the capabilities of your pipeline by integrating with other tools and services.
1. Either select the toolchain that you want to use or type a name for the new toolchain that you want to create.
1. Click **Create**. An empty pipeline is created and represented as a card on the toolchain's Overview page.

##Starting from a toolchain template
{: #starting_from_a_toolchain_template}

To create and configure a continuous delivery toolchain from a [template](https://console.ng.bluemix.net/devops/create){: new_window} ![External link icon](images/launch--glyph.svg):

1. On the **Create a Toolchain** page, click a toolchain template.  
1. Review the diagram of the toolchain that you are about to create. The diagram shows each tool integration in its lifecycle phase in the toolchain. 

 **Tip**: A few of the toolchain templates have multiple instances of a tool integration. For example, the Microservices toolchain template on {{site.data.keyword.Bluemix_notm}} Public contains three instances of GitHub and three instances of Delivery Pipeline, one for each of the three microservices.
 
 The diagram in the following image is an example. When you create a toolchain, the diagram shows each tool integration that is part of the toolchain.
 ![Toolchain_diagram](images/toolchain_diagram.png)
1. Review the default information for the toolchain settings. The toolchain's name identifies it in {{site.data.keyword.Bluemix_notm}}. If you want to use a different name, change the toolchain's name.
1. In the Configurable Integrations section, select each tool integration that you want to configure for your toolchain. A few of the tool integrations do not require configuration. For information about configuring the tool integrations, see [Configuring tool integrations](/docs/services/ContinuousDelivery/toolchains_integrations.html){: new_window}.
1. Click **Create**. Several steps run automatically to set up your toolchain. The tool integrations that are set up are different depending on which toolchain template you selected and whether you are using {{site.data.keyword.Bluemix_notm}} Public or {{site.data.keyword.Bluemix_notm}} Dedicated. For example, when you create a Microservices toolchain on {{site.data.keyword.Bluemix_notm}} Public, these steps are run: 

 * The toolchain is created.
 * If you configured Delivery Pipeline, the pipelines are created and run.
 * If you configured Sauce Labs, the toolchain is set up to add Sauce Labs test jobs to the pipelines.
 * If you configured PagerDuty, the toolchain is set up to send alert notifications to the PagerDuty service that you specified.
 * If you configured Slack, the toolchain is set up to send notifications about deployment status to the Slack channel that you specified.
 * If you configured GitHub, the sample GitHub repo is cloned into your GitHub account.
 

# Related Links
{: #rellinks}

## Tutorials and Samples
{: #samples}

* [Create a pipeline](https://www.ibm.com/devops/method/tutorials/tutorial_first_pipeline){:new_window} ![External link icon](images/launch--glyph.svg)
* [Create and use your first toolchain](https://www.ibm.com/devops/method/tutorials/tutorial_toolchain_flow){:new_window} ![External link icon](images/launch--glyph.svg)
* [Create a custom toolchain](https://www.ibm.com/devops/method/tutorials/tutorial_toolchain_custom){:new_window} ![External link icon](images/launch--glyph.svg)
* [Create a toolchain that includes {{site.data.keyword.DRA_short}}](https://www.ibm.com/devops/method/tutorials/tutorial_toolchain_devops_insights){:new_window} ![External link icon](images/launch--glyph.svg)
* [Create and use a microservices toolchain](https://www.ibm.com/devops/method/tutorials/tutorial_toolchain_microservices){:new_window} ![External link icon](images/launch--glyph.svg)
* [Create a toolchain from a template on {{site.data.keyword.Bluemix_notm}} Dedicated](https://www.ibm.com/devops/method/tutorials/tutorial_dedicated_toolchain_template_flow){:new_window} ![External link icon](images/launch--glyph.svg)
* [Create a toolchain from an app on {{site.data.keyword.Bluemix_notm}} Dedicated](https://www.ibm.com/devops/method/tutorials/tutorial_dedicated_toolchain_app_flow){:new_window} ![External link icon](images/launch--glyph.svg)

## Related Links
{: #general}

* [{{site.data.keyword.contdelivery_full}}](https://www.ibm.com/devops/method/content/deliver/tool_continuous_delivery/){:new_window} ![External link icon](images/launch--glyph.svg)
* [Empty toolchain](https://www.ibm.com/devops/method/toolchains/toolchain_empty){:new_window} ![External link icon](images/launch--glyph.svg)
* [Microservices toolchain](https://www.ibm.com/devops/method/toolchains/microservices_toolchain){:new_window} ![External link icon](images/launch--glyph.svg)
* [Simple Cloud Foundry toolchain](https://www.ibm.com/devops/method/toolchains/simple_toolchain){:new_window} ![External link icon](images/launch--glyph.svg)
* [Simple Cloud Foundry toolchain with {{site.data.keyword.DRA_short}}](https://www.ibm.com/devops/method/toolchains/toolchain_devops_insights){:new_window} ![External link icon](images/launch--glyph.svg)
* [Simple container toolchain](https://www.ibm.com/devops/method/toolchains/toolchain_simple_container){:new_window} ![External link icon](images/launch--glyph.svg)
* [Simple secure container toolchain](https://www.ibm.com/devops/method/toolchains/toolchain_simple_secure_container){:new_window} ![External link icon](images/launch--glyph.svg)
* [IBM Bluemix Garage Method](https://www.ibm.com/devops/method){:new_window} ![External link icon](images/launch--glyph.svg)
