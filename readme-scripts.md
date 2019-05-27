# mdas-ii

- Dashes work just as well
- And if you have sub points, put two spaces before the dash or star:
  -  Like this
  -  And this

MDAS Tech Challenge Tasks
1. A maximum of 10,000 characters (not including spaces). ~ 3 pages 
2. A maximum of 10 diagrams/images. See list of graphics under solution.pdf.	 
3. Instructions for deploying the solution in an AWS account, provide system requirements/assumptions to run the script	John / Andrew 
4. Repository hierarchy list
5. Solution description with a hierarchy list of core technologies used including a single level architecture diagram 
  - validate tools against final used (Sai’s spreadsheet needs to be validated with team for tools used)  
  - update spreadsheet for final confirmed tools 
  - Update TCC SecDevOps picture with the tools used  
  - Create a single page architecture based on Netflix example provided 
  - AWS infrastructure Diagram  
  - Solution description for 3 pages 

6. Instructions for running from code to full deployment 
7. Consideration of the stability, maintainability (including fault tolerance and monitoring), and scalability security of the 
solution.


## Instructions for deploying the solution in an AWS account





## Repository Hierarchy




## Solution Description



## Instructions for running from code to full deployment




## Consideration of the stability, maintainability (including fault tolerance and monitoring), and scalability security of the 
solution

Stability and maintainability of application has been a strong consideration for our solution approach. The solution is based on simple architecture, uses proven and well known technology stack and is well augmented with unit and integration test cases to ensure stability and maintainability.
The application uses OpenShift Container Platform that is designed for scaling. The platform allows for hundreds of containerized workloads to be scheduled and run without any performance bottlenecks. The physical resources such as compute nodes and storage can be scaled as the workload and user base grows. 

Fault tolerance is provided to critical container workloads via OpenShift built-in mechanisms. In addition, data and configuration settings for container images can be persisted across instances via persistent volume claims and stateful sets. Monitoring of application will be supported by AWS CloudWatch.
We use OWASP scan to identify and address security vulnerabilities within the application code beside that OpenShift Container Platform has built-in enterprise grade security, all the way from the operating system layer up to the container registries. OpenShift allows administrators to configure role-based authorization to manage the system resources such as compute, networking, and storage, and application workloads.