# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

Analyze costs, scalability, availability: I am considering Standard tier pay as you go pricing model for both VM and App sevice. However app service is almost 1.5 times costlier than VM which can further increase if support is included in monthly plan. 
In case of scalability, both VM and App Service offers autoscaling, loadbalancer and scale-limit. But, 1000 nodes per scale set and 30 instances in VM and App Service respectively.
In case of availability, both VM and App Service offers SLA and Multi-region failover. However, SLA for VM offers upto 99.99% but for App Service it's upto 99.95%. Also, VM have different parameters in SLA like Availability Zone, Data Disk etc.

My Choice:
I chose App Service because the CMS app is lightweight, does not require robust compute power, and is easy to deploy through Azure. The CMS App is straightforward and runs on a Python codebase, which is supported by App Service. For such a simple app, developer keep up and running in minutes without any underlying software. 

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

APP Service: If the app requires other languages or framework not supported by azure, this would clearly be a difficult phase. Also, the underlying software on the server is not controllable as our requirements.

Virtual Machine: If this CMS became more popular, it could become more expensive due to requiring more hardware/compute power. Also, if the CMS needed more compute capability, it could also become significantly more expensive.