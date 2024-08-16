# github-actions-tutorial

## What is CI/CD

CI/CD, which stands for Continuous Integration and Continuous Delivery (or Deployment), is a set of practices and tools in software development that aim to automate and streamline the process of integrating code changes and delivering them to production environments. This approach is central to modern DevOps practices, facilitating faster and more reliable software delivery.

### Continuous Integration (CI)

Continuous Integration is a development practice where developers frequently merge their code changes into a central repository, usually multiple times a day. Each integration is automatically verified by building the application and running a suite of tests to detect errors quickly. This practice encourages smaller, incremental updates, reducing the complexity of merging changes and improving collaboration among team members.

### Continuous Delivery (CD)

Continuous Delivery extends CI by ensuring that code changes are automatically tested and prepared for release to production. It involves automating the release process so that software can be deployed to production at any time, with minimal manual intervention. This practice ensures that the codebase is always in a deployable state, allowing for frequent and reliable releases.

### Continuous Deployment

Continuous Deployment goes a step further by automating the entire release process, including deploying code changes to production as soon as they pass the necessary tests. This eliminates the need for a manual release decision, allowing for rapid and continuous delivery of new features and updates to users.

### Benefits of CI/CD

Implementing a CI/CD pipeline offers numerous benefits, including:

- **Reduced Risk**: Automated testing and deployment reduce the likelihood of errors reaching production.
- **Faster Time to Market**: Frequent and reliable releases allow teams to deliver new features and updates more quickly.
- **Improved Code Quality**: Continuous testing and integration help maintain high code quality.
- **Enhanced Collaboration**: CI/CD practices foster better collaboration among development and operations teams.

Overall, CI/CD is a critical component of agile and DevOps methodologies, enabling organizations to deliver software more efficiently and with higher quality.

## History of CI/CD

The evolution of Continuous Integration and Continuous Delivery (CI/CD) is a fascinating journey that has significantly transformed the software development landscape. This evolution has been marked by the introduction of various tools and methodologies that have streamlined the process of integrating and deploying code changes, making software development more efficient and reliable.

### Early Beginnings

The concept of Continuous Integration (CI) was first introduced by Grady Booch in 1991 as part of his work on object-oriented design. CI aimed to reduce integration problems by ensuring that developers frequently merge their code changes into a shared repository, allowing for early detection of integration issues. This idea was further developed in the late 1990s with the advent of Extreme Programming, which advocated for more frequent releases and emphasized practices like pair programming and test-driven development.

### Emergence of Tools

Initially, the lack of automated tools meant that software testing and delivery were largely manual processes. This changed in 2001 with the release of **CruiseControl**, the first open-source tool designed to automate build management, making continuous delivery more achievable. CruiseControl was primarily Java-focused, which led to the creation of language-specific variants for other programming environments.

In 2011, **Jenkins** was introduced as a successor to Hudson CI, following Oracle's decision to trademark Hudson. Jenkins quickly became popular due to its flexibility, extensive plugin ecosystem, and strong community support, which allowed it to support a wide range of programming languages and tasks.

### Continuous Delivery and Deployment

The concepts of Continuous Delivery (CD) and Continuous Deployment emerged around 2009, as described by Jez Humble and David Farley in their book _Continuous Delivery_. These practices extended CI by automating the deployment process, ensuring that software could be reliably released to production at any time. Continuous Deployment takes this a step further by deploying every change that passes the automated tests directly to production, minimizing human intervention.

### Modern CI/CD Landscape

Today, CI/CD is an integral part of DevOps, with a plethora of tools available to support various aspects of the software lifecycle. Popular CI/CD tools include:

- **Jenkins**: Known for its versatility and plugin support, Jenkins is widely used for automating various stages of the CI/CD pipeline.
- **GitLab CI/CD**: Integrated with GitLab, this tool offers seamless CI/CD capabilities directly within the GitLab platform, providing a unified experience for version control and deployment.
- **CircleCI**: Offers cloud-based CI/CD services with a focus on speed and ease of use, supporting a wide range of languages and environments.
- **Travis CI**: Known for its simplicity, Travis CI is popular among open-source projects for its straightforward configuration and integration with GitHub.
- **Github Actions**: Last but not least, the tool that we learning through this book. :-)

## An introduction to github actions

GitHub Actions is a dynamic continuous integration and continuous delivery (CI/CD) platform that empowers developers to automate their build, test, and deployment processes directly within GitHub. By leveraging GitHub Actions, developers can create workflows that respond to various events in their repositories, such as code pushes, pull requests, or issue creations, thereby streamlining the software development lifecycle.

At its core, GitHub Actions allows for the automation of tasks through workflows defined in YAML files. These workflows consist of jobs and steps that can include running scripts, executing tests, and deploying code. The platform supports a wide range of programming languages and environments, providing flexibility and scalability for diverse development needs.

One of the standout features of GitHub Actions is its integration with the GitHub ecosystem, which facilitates seamless automation triggered by repository events. This integration not only enhances productivity but also ensures that code quality and deployment processes are consistently maintained across projects. With GitHub Actions, developers can focus more on innovation and less on the repetitive aspects of software development, making it an invaluable tool in modern DevOps practices.

## Pricing for GitHub Actions

GitHub Actions provides a flexible pricing model that allows developers to automate their workflows with ease. The pricing structure is designed to accommodate various usage patterns, whether for public or private repositories.

### Free Usage

GitHub Actions is free for public repositories, allowing unlimited use of GitHub-hosted runners. This encourages open-source projects to leverage CI/CD capabilities without incurring additional costs.

### Pricing for Private Repositories

For private repositories, GitHub provides a certain amount of free minutes and storage based on the account's plan. Beyond these included amounts, additional usage incurs costs:

- **GitHub Free**: Includes 2,000 minutes per month.
- **GitHub Pro**: Includes 3,000 minutes per month.
- **GitHub Team**: Includes 3,000 minutes per month.

### Cost for Additional Minutes

If you exceed the included minutes, the following rates apply:

#### Linux Runners

- **2-vCPU**: $0.008 USD per minute
- **4-vCPU**: $0.016 USD per minute
- **8-vCPU**: $0.032 USD per minute
- **16-vCPU**: $0.064 USD per minute

#### Windows Runners

- **2-vCPU**: $0.016 USD per minute
- **8-vCPU**: $0.064 USD per minute
- **16-vCPU**: $0.128 USD per minute

#### macOS Runners

- **3-vCPU**: $0.08 USD per minute
- **12-vCPU**: $0.12 USD per minute
- **6-vCPU (M1)**: $0.16 USD per minute

### Self-Hosted Runners

Self-hosted runners allow you to run workflows on your own infrastructure. They offer flexibility and control over the hardware and operating system environments. Importantly, self-hosted runners do not incur additional costs based on usage, as they utilize your own resources. This can be a cost-effective solution for teams with specific needs or high usage requirements.

### Storage Costs

Additional storage beyond the included amount is charged at $0.25 USD per GB. Data transfer out, outside of Actions, costs $0.50 USD per GB.

### Billing and Spending Limits

- Accounts have a default spending limit of 0 USD, preventing additional usage beyond the included amounts. This limit can be adjusted to allow for more usage.
- Organizations can connect an Azure Subscription ID to manage and pay for usage beyond the included amounts.

### Estimating Costs

To estimate potential costs, GitHub provides a [Pricing Calculator](https://github.com/pricing/calculator) that allows users to configure and estimate expenses based on their specific usage patterns.

By understanding the pricing structure, teams can effectively manage their budgets while leveraging the powerful automation capabilities of GitHub Actions.
