# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

APP SERVICE
Cost: Very reasonable. There are three different tiers - Dev/Test, Production, and Isolated. Choose according to your requiremnts.
Scalablity: Supports both Vertical or Horizontal scaling.
Availability: Supports multiple languages, such as .NET, .NET Core, Java, Ruby, Node.js, PHP, or Python and support of both Linux and Windows environments.
Workflow: Continous deployment through GitHub workflows on the Azure portal makes updating the CMS app a snap.

Virtual Machine
Cost: Also reasonable cost. Lower up-front cost compared to purchasing and maintaining hardware.
Scalability: Supports both Vertical or Horizontal scaling.
Availability: Support of both Linux and Windows VMs.
Workflow: VMs allow for the installation of custom images and are an excellent choice for migrating from an on-premises server to the cloud. Also works fine to deploy web application etc.

My Choice:
I chose App Service because the CMS app is lightweight, does not require robust compute power, and is easy to deploy through Azure. The CMS App is straightforward and runs on a Python codebase, which is supported by App Service. Overall, a simple choice. 

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

APP Service: If the app requires other languages or framework not supported by azure, this would clearly be a difficult phase. Also, the underlying software on the server is not controllable as our requirements.

Virtual Machine: If this CMS became more popular, it could become more expensive due to requiring more hardware/compute power. Also, if the CMS needed more compute capability, it could also become significantly more expensive.