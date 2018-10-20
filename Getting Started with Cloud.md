#Getting Started with Cloud Computing 

Cloud Computing

    A remote virtual pool of on demand shared resources offering Compute , Storage & Network 
    services that can be rapidly deployed at scale.
    
    Virtualization is key to Cloud Computing 
    
Key  Cloud Concepts

    -   On Demand resourcing (with in no time )
    -   Utility Based metering ( Pay as you go )
    -   Shared Infrastructure 
    -   Scalable   # In and out (by chaging number of instance) , up and down (by changing CPU)
    -   Highly Avilable # Replicated across different geographical region
    -   Secure ( more secure than traditional data centers

Cloud Service Models

    -   Infrastructure as a Service (IAAS) # providing the underlying resources – compute, storage and networking
    -   Container as a Service (CAAS) # Manages container-based workloads
    -   Platform as a Service (PAAS)  # lies in the middle of SaaS and IaaS
    -   Software as a Service (SAAS)  # delivers entire functioning applications through the Internet
    
Cloud Deployment Models 

    -   Public 
    -   Private 
    -   Hybrid
    
Private Cloud : 

    -   Infrastructure is privately hosted , managed and ownened by self
    -   Greater and more direct control over its data
    -   Hardware held on premise
    -   Higher cost ( Operational and maintenance Cost)
    -   More Secured 
    -   Similar to tradional approach but differs in
            -   Cloud principles are applied like
                    -   Virtualization
                    -   On demand resourcing 
                    -   Use of Scalability
                    -   Creating pool of shared compute , storage & network resources 
Region vs Zone

    Availability Zones = Data Center
    Region = Collection of AZ 
            
            Example NA-1a, NA-1b  
                    Region NA-1
                    AZ = NA-1a, NA-1b
    
                    us-east-1 (Region)
                    us-east-1a, us-east-1b (AZ)
    A Region have 2 AZ bare minimum , except Beijing and US GOV in AWS
    Both are mandatory iniputs 