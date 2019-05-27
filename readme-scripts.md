# mdas-ii
MDAS Tech Challenge
1.0 (i)	A maximum of 10,000 characters (not including spaces). ~ 3 pages	Syed A	05/23 Noon
2.0 (ii)	A maximum of 10 diagrams/images. 	See list of graphics under solution.pdf.	05/22 COB
3.0 (iii)	Instructions for deploying the solution in an AWS account, provide system requirements/assumptions to run the script	John / Andrew 
4.0 (iv)	Repository hierarchy list	Prasad	
5.0 (v)	v. Solution description with a hierarchy list of core technologies used including a single level architecture diagram (i.e. https://bit.ly/2GOC4gM)
--- validate tools against final used (Sai’s spreadsheet needs to be validated with team for tools used) - Vijay
--- update spreadsheet for final confirmed tools - Vijay
--- Update TCC SecDevOps picture with the tools used - Syed
--- Create a single page architecture based on Netflix example provided - Syed
--- AWS infrastructure Diagram – Vijay
--- Solution description for 3 pages - Syed	Syed & Paul (Graphics)

6.0 (vi)	Instructions for running from code to full deployment	John / Andrew
7.0 (vii)	Consideration of the stability, maintainability (including fault tolerance and monitoring), and scalability security of the 
solution.	Syed/John


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