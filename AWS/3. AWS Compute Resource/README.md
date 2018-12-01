#AWS Compute


    Compute : Brain & Processing power = CPU & RAM 

#Amazon Elastic Compute Cloud -  EC2

    Allows to deploy virtual server within AWS environment 
    
    7 Step Process 
    
    1)  Choose AMI (Amazon Machine Image)
           - Templates of pre-configured EC2 Instances
           - On High level it includes O/S, Common Applications with any custom configurations 
           - You can create your own AMI 
           - AWS Managed AMI , AMI from AWS Market place , AMI from Community , Custom AMI 
    2)  Select Instance Type 
           - Instance type varies based on CPU, Memory , Storage & Networking 
           - 4 types
                - General Purpose 
                       - Balanceof CPU , Memory & Storage
                       - Small & Medium Applications
                       - Comes with EBS by default
                - Compute Optimized 
                       - High Performance i.e CPU
                       - High Performance Front end , web servers
                - GPU 
                       - Optimized for Graphic Intense Applications
                - Memory Optimmized 
                       - Large scale , enterprise-class , in memory applications 
                - Storage Optimizeed 
                       - Low latency & HIgh I/O Performance 
                       - SSD Backed instance storage
    3)  Configure Instance Detail
            - Instanec Perchasing options 
                - On Demand Instance  (BY Default )
                       - Have Flat rate , paid by hour , based on instance type used
                       - Typically used for short term usage , where workload can irregular & Uninterruptable
                       - Testing & Development Environment
                - Reserved Instance 
                       - Purchased for set of time period (1-3 Years) for a reduced cost 75%
                       - All upfront 
                       - Partial Upfront
                       - No Upfront 
                       - Typically used for long term, predicatble workload 
                - Spot instance 
                       - Based on bidding 
                 
             - Tenancy 
                Relates to underlying hosting of your EC2 instance 
                - Shared : Same host may be used by multiple customer 
                - Dedicated Instance 
                - Dedicated Host
    4)  Add Storage
            - Persistent Storage
                - EBS Volumes
                - Physically separated from EC2 instance , logically atttached by AWS N/W
                - Can be detached from instance 
                - Data ramains
            - Ephemeral Storage
                - Temporary Storage on instance , called instance backed storage 
                - Instance store volumes are attached to underlying host
                - Can't be detached from instance
                - Data lost if stopped or terminated , but remains if rebooted 
    5)  Add Tag 
    6)  Add Security Groups
            - Virtual Firewalls fro instance 
            - Ket Pair 
            - Public & Private Key 
            - PPK 
            - PEM 
            
    7)  Review and Launch    

    LAB:  Create Your First Amazon EC2 Instance ( Linux )
          Create Your First Amazon EC2 Instance ( Windows )