# References - Azure Compute for IDP

This document contains curated resources for learning Azure compute services with Python to build and manage Internal Development Platforms (IDP).

## 📚 Table of Contents

- [Official Documentation](#official-documentation)
- [Books](#books)
- [Articles & Blog Posts](#articles--blog-posts)
- [Video Tutorials](#video-tutorials)
- [Online Courses](#online-courses)
- [Tools & Libraries](#tools--libraries)
- [GitHub Repositories](#github-repositories)
- [Related Learning Repositories](#related-learning-repositories)
- [Community Resources](#community-resources)

-----

## 📖 Official Documentation

### Azure Compute Services

#### Virtual Machines

- [Azure Virtual Machines Documentation](https://learn.microsoft.com/en-us/azure/virtual-machines/) - Complete VM guide
- [Linux VMs in Azure](https://learn.microsoft.com/en-us/azure/virtual-machines/linux/) - Linux VM documentation
- [Windows VMs in Azure](https://learn.microsoft.com/en-us/azure/virtual-machines/windows/) - Windows VM documentation
- [VM Sizes](https://learn.microsoft.com/en-us/azure/virtual-machines/sizes) - VM size reference
- [Managed Disks](https://learn.microsoft.com/en-us/azure/virtual-machines/managed-disks-overview) - Disk management

#### VM Scale Sets

- [Virtual Machine Scale Sets](https://learn.microsoft.com/en-us/azure/virtual-machine-scale-sets/) - VMSS overview
- [Autoscaling](https://learn.microsoft.com/en-us/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-autoscale-overview) - Auto-scale guide
- [Orchestration Modes](https://learn.microsoft.com/en-us/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-orchestration-modes) - VMSS modes

#### Container Services

- [Azure Container Instances](https://learn.microsoft.com/en-us/azure/container-instances/) - ACI documentation
- [Azure Kubernetes Service](https://learn.microsoft.com/en-us/azure/aks/) - AKS documentation
- [Azure Container Registry](https://learn.microsoft.com/en-us/azure/container-registry/) - ACR documentation

#### Batch Computing

- [Azure Batch](https://learn.microsoft.com/en-us/azure/batch/) - Batch computing guide
- [Batch Pools](https://learn.microsoft.com/en-us/azure/batch/batch-pool-create) - Pool configuration
- [Batch Jobs and Tasks](https://learn.microsoft.com/en-us/azure/batch/batch-api-basics) - Job management

### Azure SDK for Python - Compute

#### Management Libraries

- [azure-mgmt-compute](https://learn.microsoft.com/en-us/python/api/overview/azure/mgmt-compute-readme) - Compute management
- [Virtual Machines API](https://learn.microsoft.com/en-us/python/api/azure-mgmt-compute/azure.mgmt.compute.v2023_07_01.operations.virtualmachinesoperations) - VM operations
- [Disks API](https://learn.microsoft.com/en-us/python/api/azure-mgmt-compute/azure.mgmt.compute.v2023_04_02.operations.disksoperations) - Disk operations
- [Images API](https://learn.microsoft.com/en-us/python/api/azure-mgmt-compute/azure.mgmt.compute.v2023_07_01.operations.imagesoperations) - Image management

#### Container Management

- [azure-mgmt-containerinstance](https://learn.microsoft.com/en-us/python/api/overview/azure/mgmt-containerinstance-readme) - ACI management
- [azure-mgmt-containerservice](https://learn.microsoft.com/en-us/python/api/overview/azure/mgmt-containerservice-readme) - AKS management
- [azure-mgmt-containerregistry](https://learn.microsoft.com/en-us/python/api/overview/azure/mgmt-containerregistry-readme) - ACR management

#### Batch Management

- [azure-mgmt-batch](https://learn.microsoft.com/en-us/python/api/overview/azure/mgmt-batch-readme) - Batch management
- [azure-batch](https://learn.microsoft.com/en-us/python/api/overview/azure/batch-readme) - Batch service SDK

### Kubernetes & Containerization

#### Kubernetes

- [Kubernetes Documentation](https://kubernetes.io/docs/home/) - Official Kubernetes docs
- [kubectl Reference](https://kubernetes.io/docs/reference/kubectl/) - kubectl commands
- [Python Kubernetes Client](https://github.com/kubernetes-client/python) - Kubernetes Python SDK

#### Docker

- [Docker Documentation](https://docs.docker.com/) - Docker reference
- [Dockerfile Reference](https://docs.docker.com/engine/reference/builder/) - Dockerfile syntax
- [Docker Compose](https://docs.docker.com/compose/) - Multi-container apps

### Best Practices & Architecture

#### Design Patterns

- [Azure VM Best Practices](https://learn.microsoft.com/en-us/azure/virtual-machines/best-practices) - VM recommendations
- [AKS Best Practices](https://learn.microsoft.com/en-us/azure/aks/best-practices) - AKS guidelines
- [Container Security](https://learn.microsoft.com/en-us/azure/container-instances/container-instances-security) - Security practices

#### Architecture

- [Azure Compute Decision Tree](https://learn.microsoft.com/en-us/azure/architecture/guide/technology-choices/compute-decision-tree) - Choose compute service
- [High Availability Architecture](https://learn.microsoft.com/en-us/azure/architecture/framework/resiliency/overview) - Resilience patterns
- [Scalable Architecture](https://learn.microsoft.com/en-us/azure/architecture/framework/scalability/overview) - Scaling patterns

-----

## 📚 Books

### Azure Compute & Cloud

1. **“Azure for Architects”** by Ritesh Modi (3rd Edition)
- Azure compute architecture
- VM and container strategies
- [Packt Publishing](https://www.packtpub.com/product/azure-for-architects-third-edition/9781803238562)
1. **“Mastering Azure Virtual Desktop”** by Ryan Mangan
- VM deployment patterns
- Virtual infrastructure
- [Packt Publishing](https://www.packtpub.com/product/mastering-azure-virtual-desktop/9781801075305)
1. **“Azure Container Apps: Deploy and Manage Cloud-Native Apps”** by Boris Scholl
- Container services on Azure
- Modern application deployment
- [O’Reilly](https://www.oreilly.com/library/view/azure-container-apps/9781098142094/)

### Kubernetes

1. **“Kubernetes: Up and Running”** by Brendan Burns, Joe Beda, Kelsey Hightower, Lachlan Evenson (3rd Edition)
- Kubernetes fundamentals
- Production deployment
- [O’Reilly](https://www.oreilly.com/library/view/kubernetes-up-and/9781098110192/)
1. **“Kubernetes Patterns”** by Bilgin Ibryam and Roland Huß (2nd Edition)
- Design patterns for Kubernetes
- Cloud-native applications
- [O’Reilly](https://www.oreilly.com/library/view/kubernetes-patterns-2nd/9781098131678/)
1. **“Production Kubernetes”** by Josh Rosso, Rich Lander, Alex Brand, John Harris
- Running Kubernetes in production
- AKS best practices
- [O’Reilly](https://www.oreilly.com/library/view/production-kubernetes/9781492092292/)

### Containers & Docker

1. **“Docker Deep Dive”** by Nigel Poulton
- Docker fundamentals
- Container orchestration
- [Self-published](https://www.amazon.com/Docker-Deep-Dive-Nigel-Poulton/dp/1916585256)
1. **“Docker in Practice”** by Ian Miell and Aidan Hobson Sayers (2nd Edition)
- Practical Docker usage
- Container development
- [Manning Publications](https://www.manning.com/books/docker-in-practice-second-edition)

### Performance & Optimization

1. **“Systems Performance”** by Brendan Gregg (2nd Edition)
- Performance analysis
- System optimization
- [Addison-Wesley](https://www.amazon.com/Systems-Performance-Brendan-Gregg/dp/0136820158)
1. **“Cloud Native DevOps with Kubernetes”** by John Arundel and Justin Domingus
- DevOps practices
- Cloud-native patterns
- [O’Reilly](https://www.oreilly.com/library/view/cloud-native-devops/9781492040750/)

-----

## 📝 Articles & Blog Posts

### Virtual Machines

#### VM Management

- [Azure VM Management Best Practices](https://techcommunity.microsoft.com/t5/azure-compute-blog/best-practices-for-azure-vm-management/ba-p/3456789) - Microsoft
- [Optimizing VM Performance](https://azure.microsoft.com/en-us/blog/optimizing-azure-vm-performance/) - Azure Blog
- [VM Sizing Guidelines](https://learn.microsoft.com/en-us/azure/virtual-machines/sizes-general) - Microsoft Docs

#### High Availability

- [Building Highly Available Applications](https://docs.microsoft.com/en-us/azure/architecture/framework/resiliency/app-design) - Azure Architecture
- [Availability Zones Explained](https://techcommunity.microsoft.com/t5/azure-infrastructure-blog/availability-zones-explained/ba-p/2345678) - Azure Community
- [VM Availability Sets vs Zones](https://cloudskills.io/blog/azure-availability-sets-zones) - Cloud Skills

### Container Services

#### Azure Container Instances

- [When to Use ACI](https://azure.microsoft.com/en-us/blog/when-to-use-azure-container-instances/) - Azure Blog
- [ACI Networking Options](https://docs.microsoft.com/en-us/azure/container-instances/container-instances-virtual-network-concepts) - Microsoft Docs
- [Multi-Container Groups](https://learn.microsoft.com/en-us/azure/container-instances/container-instances-multi-container-group) - Guide

#### Azure Kubernetes Service

- [AKS Production Readiness](https://techcommunity.microsoft.com/t5/azure-architecture-blog/production-ready-aks/ba-p/3456789) - Azure Architecture
- [AKS Networking Deep Dive](https://docs.microsoft.com/en-us/azure/aks/concepts-network) - Microsoft Docs
- [AKS Cost Optimization](https://azure.microsoft.com/en-us/blog/aks-cost-optimization-guide/) - Azure Blog

### Scaling & Performance

#### Auto-scaling

- [VM Auto-scaling Best Practices](https://docs.microsoft.com/en-us/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-autoscale-overview) - Microsoft
- [AKS Cluster Autoscaling](https://learn.microsoft.com/en-us/azure/aks/cluster-autoscaler) - Guide
- [Scaling Strategies Compared](https://cloudskills.io/blog/azure-scaling-strategies) - Cloud Skills

#### Performance Optimization

- [Optimizing Compute Costs](https://azure.microsoft.com/en-us/blog/optimize-your-azure-compute-costs/) - Azure Blog
- [Performance Tuning VMs](https://techcommunity.microsoft.com/t5/azure-compute-blog/vm-performance-tuning/ba-p/2345678) - Azure Community
- [Container Performance](https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/) - Kubernetes Docs

### Security

#### Compute Security

- [Securing Azure VMs](https://docs.microsoft.com/en-us/azure/security/fundamentals/virtual-machines-overview) - Security Center
- [AKS Security Best Practices](https://learn.microsoft.com/en-us/azure/aks/security-best-practices) - Microsoft Docs
- [Container Security](https://learn.microsoft.com/en-us/azure/container-instances/container-instances-security) - Guide

#### Identity & Access

- [Managed Identities for Compute](https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/overview) - AAD Docs
- [AKS Pod Identity](https://learn.microsoft.com/en-us/azure/aks/use-azure-ad-pod-identity) - Guide
- [RBAC for AKS](https://learn.microsoft.com/en-us/azure/aks/azure-ad-rbac) - Access control

-----

## 🎥 Video Tutorials

### Microsoft Official Content

#### Virtual Machines

- [Azure VMs Deep Dive](https://www.youtube.com/watch?v=inaXkN2UrFE) - Azure Friday (30 min)
- [VM Management with Python](https://channel9.msdn.com/Shows/Azure-Friday/Managing-Azure-VMs-with-Python) - Channel 9 (25 min)
- [VM Scale Sets Explained](https://www.youtube.com/watch?v=Ky7eXG7snmI) - Microsoft (20 min)

#### Container Services

- [Azure Container Instances](https://www.youtube.com/watch?v=jAWLQFi4USk) - Azure Friday (15 min)
- [AKS Overview and Best Practices](https://www.youtube.com/watch?v=R-3dfURb2hA) - Microsoft Build (60 min)
- [Container Registry Deep Dive](https://channel9.msdn.com/Shows/Azure-Friday/Azure-Container-Registry) - Channel 9 (20 min)

#### Kubernetes on Azure

- [AKS Workshop Series](https://www.youtube.com/playlist?list=PLLasX02E8BPCrIhFrc_ZiINhbRkYMKdPT) - Microsoft (series)
- [Kubernetes Best Practices](https://www.youtube.com/watch?v=wGz_cbtCiEA) - Brendan Burns (45 min)
- [Deploying to AKS](https://www.youtube.com/watch?v=4ht22ReBjno) - Microsoft DevRadio (30 min)

### Community Content

#### Conference Talks

- [Scaling Kubernetes on Azure](https://www.youtube.com/watch?v=vhvFuPKxQLA) - KubeCon (40 min)
- [Azure Compute at Scale](https://www.youtube.com/watch?v=xbEKvUq3xR0) - Microsoft Ignite (50 min)
- [Container Patterns](https://www.youtube.com/watch?v=vmeZ9dhE1sE) - DockerCon (35 min)

#### Tutorial Series

- [Azure VM Tutorial Series](https://www.youtube.com/playlist?list=PLGjZwEtPN7j-Q59JYso3L4_yoCjj2syrM) - Adam Marczak
- [Kubernetes Tutorial for Beginners](https://www.youtube.com/watch?v=X48VuDVv0do) - TechWorld with Nana (4 hours)
- [Docker Mastery](https://www.youtube.com/playlist?list=PL2We04F3Y_43dAehLMT5GxJhtk3mJtkl5) - Bret Fisher

-----

## 🎓 Online Courses

### Microsoft Learn (Free)

#### Virtual Machines

- [Deploy a VM in Azure](https://learn.microsoft.com/en-us/training/modules/create-windows-virtual-machine-in-azure/) - Module
- [Manage VMs with Azure CLI](https://learn.microsoft.com/en-us/training/modules/manage-virtual-machines-with-azure-cli/) - Module
- [Configure VM availability](https://learn.microsoft.com/en-us/training/modules/configure-virtual-machine-availability/) - Module

#### Containers & Kubernetes

- [Introduction to Kubernetes](https://learn.microsoft.com/en-us/training/modules/intro-to-kubernetes/) - Module
- [Introduction to AKS](https://learn.microsoft.com/en-us/training/modules/intro-to-azure-kubernetes-service/) - Module
- [Deploy to AKS](https://learn.microsoft.com/en-us/training/paths/deploy-applications-to-azure-kubernetes-service/) - Learning path

#### Certifications

- [AZ-104: Azure Administrator](https://learn.microsoft.com/en-us/certifications/azure-administrator/) - Certification
- [AZ-305: Azure Solutions Architect](https://learn.microsoft.com/en-us/certifications/azure-solutions-architect/) - Certification

### Paid Platforms

#### Pluralsight

- [Managing Azure VMs](https://www.pluralsight.com/courses/azure-virtual-machines-managing) - Course
- [Azure Kubernetes Service (AKS) Deep Dive](https://www.pluralsight.com/courses/azure-kubernetes-service-deep-dive) - Course
- [Docker Deep Dive](https://www.pluralsight.com/courses/docker-deep-dive-update) - Course

#### A Cloud Guru / Linux Academy

- [AZ-104: Microsoft Azure Administrator](https://acloudguru.com/course/az-104-microsoft-azure-administrator-certification-prep) - Course
- [Certified Kubernetes Administrator (CKA)](https://acloudguru.com/course/certified-kubernetes-administrator-cka) - Course
- [Azure Container Services](https://acloudguru.com/course/azure-container-services-deep-dive) - Course

#### Udemy

- [AZ-104 Azure Administrator](https://www.udemy.com/course/70533-azure/) - Scott Duffy
- [Docker Mastery](https://www.udemy.com/course/docker-mastery/) - Bret Fisher
- [Kubernetes Mastery](https://www.udemy.com/course/kubernetesmastery/) - School of Devops

#### Linux Foundation

- [Kubernetes Fundamentals (LFS258)](https://training.linuxfoundation.org/training/kubernetes-fundamentals/) - Official training
- [Kubernetes for Developers (LFD259)](https://training.linuxfoundation.org/training/kubernetes-for-developers/) - Developer focused

-----

## 🛠️ Tools & Libraries

### Azure SDK Packages

#### Compute Management

- **[azure-mgmt-compute](https://pypi.org/project/azure-mgmt-compute/)** - VM, disk, image management
- **[azure-mgmt-containerinstance](https://pypi.org/project/azure-mgmt-containerinstance/)** - Container instances
- **[azure-mgmt-containerservice](https://pypi.org/project/azure-mgmt-containerservice/)** - AKS management
- **[azure-mgmt-containerregistry](https://pypi.org/project/azure-mgmt-containerregistry/)** - Container registry
- **[azure-mgmt-batch](https://pypi.org/project/azure-mgmt-batch/)** - Batch computing

#### Supporting Libraries

- **[azure-identity](https://pypi.org/project/azure-identity/)** - Authentication
- **[azure-mgmt-network](https://pypi.org/project/azure-mgmt-network/)** - Network configuration
- **[azure-mgmt-monitor](https://pypi.org/project/azure-mgmt-monitor/)** - Monitoring

### Kubernetes Tools

#### Core Tools

- **[kubectl](https://kubernetes.io/docs/tasks/tools/)** - Kubernetes CLI
- **[helm](https://helm.sh/)** - Kubernetes package manager
- **[kubernetes-python](https://github.com/kubernetes-client/python)** - Kubernetes Python client

#### Development Tools

- **[skaffold](https://skaffold.dev/)** - Development workflow
- **[tilt](https://tilt.dev/)** - Local Kubernetes development
- **[draft](https://draft.sh/)** - Application deployment

#### Management Tools

- **[k9s](https://k9scli.io/)** - Terminal UI for Kubernetes
- **[lens](https://k8slens.dev/)** - Kubernetes IDE
- **[octant](https://octant.dev/)** - Web-based Kubernetes UI

### Container Tools

#### Docker Tools

- **[docker](https://www.docker.com/)** - Container runtime
- **[docker-compose](https://docs.docker.com/compose/)** - Multi-container apps
- **[buildkit](https://github.com/moby/buildkit)** - Build toolkit

#### Registry Tools

- **[crane](https://github.com/google/go-containerregistry/tree/main/cmd/crane)** - Container registry operations
- **[skopeo](https://github.com/containers/skopeo)** - Image operations
- **[trivy](https://github.com/aquasecurity/trivy)** - Container security scanner

### Monitoring & Observability

#### Monitoring

- **[prometheus](https://prometheus.io/)** - Metrics collection
- **[grafana](https://grafana.com/)** - Visualization
- **[datadog](https://www.datadoghq.com/)** - Full-stack observability

#### Logging

- **[fluentd](https://www.fluentd.org/)** - Log collection
- **[elasticsearch](https://www.elastic.co/)** - Log analysis
- **[kibana](https://www.elastic.co/kibana)** - Log visualization

### Testing Tools

#### Infrastructure Testing

- **[pytest](https://pytest.org/)** - Testing framework
- **[testinfra](https://testinfra.readthedocs.io/)** - Infrastructure testing
- **[inspec](https://www.inspec.io/)** - Compliance testing

#### Load Testing

- **[locust](https://locust.io/)** - Load testing
- **[k6](https://k6.io/)** - Performance testing
- **[artillery](https://artillery.io/)** - Load testing

-----

## 💻 GitHub Repositories

### Official Microsoft Repositories

#### Azure Samples

- [Azure Compute Samples](https://github.com/Azure-Samples/compute-python-manage-vm) - VM management examples
- [AKS Samples](https://github.com/Azure-Samples/azure-voting-app-redis) - AKS application samples
- [Container Instance Samples](https://github.com/Azure-Samples/aci-docs-sample-python) - ACI examples

#### AKS Resources

- [AKS Documentation](https://github.com/Azure/AKS) - Official AKS repo
- [AKS Baseline](https://github.com/mspnp/aks-baseline) - Reference architecture
- [AKS Best Practices](https://github.com/Azure/AKS/tree/master/best-practices) - Best practices

### Community Repositories

#### Learning Resources

- [Awesome Kubernetes](https://github.com/ramitsurana/awesome-kubernetes) - Curated K8s resources
- [Awesome Docker](https://github.com/veggiemonk/awesome-docker) - Docker resources
- [Awesome Azure](https://github.com/kristofferandreasen/awesome-azure) - Azure resources

#### Tools & Utilities

- [Azure VM Extensions](https://github.com/Azure/azure-linux-extensions) - Linux VM extensions
- [AKS Engine](https://github.com/Azure/aks-engine) - AKS cluster deployment
- [Azure DevOps Tasks](https://github.com/microsoft/azure-pipelines-tasks) - CI/CD tasks

#### Example Applications

- [Microservices Demo](https://github.com/GoogleCloudPlatform/microservices-demo) - Sample app
- [Sock Shop](https://github.com/microservices-demo/microservices-demo) - Microservices reference
- [Azure Voting App](https://github.com/Azure-Samples/azure-voting-app-redis) - Simple voting app

-----

## 🔗 Related Learning Repositories

### From learning-internal-development-platform Series

1. **[learning-internal-development-platform](https://github.com/vanHeemstraSystems/learning-internal-development-platform)**
- Main overview repository
- Complete learning roadmap
1. **[learning-idp-python-azure-sdk](https://github.com/vanHeemstraSystems/learning-idp-python-azure-sdk)**
- Azure SDK fundamentals
- Prerequisites for compute
1. **[learning-idp-test-driven-development](https://github.com/vanHeemstraSystems/learning-idp-test-driven-development)**
- TDD for infrastructure
- Testing compute resources
1. **[learning-idp-azure-networking](https://github.com/vanHeemstraSystems/learning-idp-azure-networking)**
- Network configuration
- Load balancing
1. **[learning-idp-azure-storage](https://github.com/vanHeemstraSystems/learning-idp-azure-storage)**
- Storage for VMs
- Persistent volumes
1. **[learning-idp-containerization](https://github.com/vanHeemstraSystems/learning-idp-containerization)**
- Container development
- Docker patterns
1. **[learning-idp-infrastructure-as-code](https://github.com/vanHeemstraSystems/learning-idp-infrastructure-as-code)**
- IaC for compute
- Template deployment
1. **[learning-idp-observability](https://github.com/vanHeemstraSystems/learning-idp-observability)**
- Monitoring compute
- Performance metrics

-----

## 👥 Community Resources

### Forums & Discussion

#### Official Microsoft

- [Azure Compute Forum](https://learn.microsoft.com/en-us/answers/tags/133/azure-virtual-machines) - Q&A
- [AKS GitHub Discussions](https://github.com/Azure/AKS/discussions) - AKS community
- [Azure Tech Community](https://techcommunity.microsoft.com/t5/azure-compute-blog/bg-p/AzureComputeBlog) - Compute blog

#### Stack Overflow

- [azure-virtual-machine](https://stackoverflow.com/questions/tagged/azure-virtual-machine) - VM questions
- [azure-aks](https://stackoverflow.com/questions/tagged/azure-aks) - AKS questions
- [azure-container-instances](https://stackoverflow.com/questions/tagged/azure-container-instances) - ACI questions

### Kubernetes Community

#### Official Channels

- [Kubernetes Slack](https://kubernetes.slack.com/) - Community chat
- [Kubernetes Discourse](https://discuss.kubernetes.io/) - Discussion forum
- [CNCF Slack](https://slack.cncf.io/) - Cloud Native community

#### Reddit

- [r/kubernetes](https://www.reddit.com/r/kubernetes/) - Kubernetes discussions
- [r/docker](https://www.reddit.com/r/docker/) - Docker community
- [r/Azure](https://www.reddit.com/r/AZURE/) - Azure discussions

### Blogs & Newsletters

#### Microsoft Blogs

- [Azure Compute Blog](https://techcommunity.microsoft.com/t5/azure-compute-blog/bg-p/AzureComputeBlog) - Official compute blog
- [AKS Blog](https://azure.microsoft.com/en-us/blog/tag/azure-kubernetes-service/) - AKS updates
- [Container Blog](https://techcommunity.microsoft.com/t5/containers/bg-p/Containers) - Container services

#### Community Blogs

- [Kubernetes Blog](https://kubernetes.io/blog/) - Official K8s blog
- [Docker Blog](https://www.docker.com/blog/) - Docker updates
- [CNCF Blog](https://www.cncf.io/blog/) - Cloud Native news

-----

## 📊 Cheat Sheets & Quick References

### Azure Compute

- [Azure VM Sizes Cheat Sheet](https://azure.microsoft.com/en-us/pricing/details/virtual-machines/series/) - VM sizes
- [Azure CLI Compute Commands](https://learn.microsoft.com/en-us/cli/azure/vm) - CLI reference
- [Azure Python SDK Quick Reference](https://github.com/Azure/azure-sdk-for-python/tree/main/sdk/compute) - SDK guide

### Kubernetes

- [Kubernetes Cheat Sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/) - kubectl commands
- [Helm Cheat Sheet](https://helm.sh/docs/intro/cheatsheet/) - Helm commands
- [AKS Cheat Sheet](https://learn.microsoft.com/en-us/azure/aks/kubernetes-walkthrough) - AKS basics

### Docker

- [Docker Cheat Sheet](https://docs.docker.com/get-started/docker_cheatsheet.pdf) - Docker commands
- [Dockerfile Best Practices](https://docs.docker.com/develop/dev-best-practices/) - Build optimization

-----

## 🎯 Next Steps

After mastering Azure Compute, continue with:

1. **[learning-idp-azure-networking](https://github.com/vanHeemstraSystems/learning-idp-azure-networking)** - Network architecture
1. **[learning-idp-observability](https://github.com/vanHeemstraSystems/learning-idp-observability)** - Monitoring solutions
1. **[learning-idp-cicd-pipelines](https://github.com/vanHeemstraSystems/learning-idp-cicd-pipelines)** - Deployment automation
1. **[learning-idp-security](https://github.com/vanHeemstraSystems/learning-idp-azure-security)** - Security hardening

-----

*Last updated: December 18, 2025*
*Part of the learning-internal-development-platform series*
