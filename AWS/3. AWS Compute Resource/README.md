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
          
          
          
#AWS Batch 
    
    Manage & Run Batch Computing Workload
    Batch Procesing means Executing series of jobs and tasks
    
    5 Step Process
    
    1) Job 
        - Unit of work to be run 
        - Run as a containerized application on EC2 instances
        - status may be submitted/pending/running/faied so on
    
    2) Job Definations
        - Specific parameters of the job 
        - Number of CPU / Which Volume /Which IAM Role /Which Mount Point 
        
    3) Job Queues
        - Scehduled jobs are placed in a queue .
        - Multiple queues are created based on priority 
        - Support on-demand and spot instances 
        
    4) Job Scheduling 
        - When a job should run and in which environment
        - FIFO concept
        - Highest Priority queue run first
        
    5) Compute Environment
        - Bascially Managed/Unmanaged ECS Cluster 
        
#Amazon LightSail
    
    Allows to deploy virtual Private server 
    Good for small scale use , and easy to onfigure 
    
    7 Step Process in 1 screen 
    
    1) Pick Instance Image
         - OS only or App & OS
    
    2) Select Avilability Zone 
    
    3) Add Launch Script 
         - Similar to User Data in EC2 
         
    4) SSH Key Pair
         - Can add existing or create new one 
         
    5) Chosse Instance Plan 
         -  For CPU , memory & Storage 
         -  SSD Solid State Drive storage avilable
    
    6) Name Instance 
         - Give unique instance name 
        
    7) Click Create 
    
#Amazon Elastic Load Balancing -  ELB 

    Used to direct and route traffic to multiple instance  
    
    NOTE: Basically how you direct traffic equally to multiple instances
    NOTE: Load Balancers only work in same region but multiple AZs
    NOTE: Only Works within a single VPC
    
    3 Types of Load Balancing 
           - Classic Load Balancing 
                - Route traffic based on applications and N/W information
           - Application Load Balancing 
                - Route traffic based on advance application lavel for multiple applications 
                  running on same instance 
                - Operating at the request level
           - Network Load Balancing
                - when you need ultra-high performance and static IP addresses for your application
                - Operating at the connection level
    7 Step Process 
    
    1)  Define Load Balancer
           - Name it
           - Internal or External 
           - Add Availailty Zone / Subnets 
    
           - Internal Load Balancer
                - Have Internal IP Address
                - Can only be accessed from private AWS network
           - External Load Balancer (Also called Internet Facing Load Balancer)
                - Have Public IP Address 
                - Receives traffic from internet and distribute to instances
                
    2)  Assign Security Groups 
                
    3)  Configure Security Settings
    
    4)  Configure Health Checks
            - Response Timeout:
                The amount of time to wait when receiving a response from the health check, in seconds.
                Valid values: 2 to 60. Default: 5
            - HealthCheck Interval:            
                The amount of time between health checks of an individual instance, in seconds. 
                Valid values: 5 to 300. Default: 30
            - Unhealthy Threshold:
                The number of consecutive failed health checks that must occur before declaring an EC2 instance unhealthy. 
                Valid values: 2 to 10. Default: 2
            - Healthy Threshold:
                The number of consecutive successful health checks that must occur before declaring an EC2 instance healthy. 
                Valid values: 2 to 10. Default: 10
            
    5)  Add EC2 instances  
            - Cross-Zone Load Balancing
                -  used to ensure that your LB distributes incoming requests evenly across all 
                   instances in its enabled Availability Zones, ignoring the default of round-robin
                
            - Connection Draining 
                -  used to ensure that a Classic Load Balancer stops sending requests to instances 
                   that are marked as unhealthy 
    6)  Add Tags
    7)  Review 
   
    Go to Security Group , Edit security groups of Instances , to custom and address is security group of load balancer.
    
 
    LAB:  Create Your First Classic Load Balancer

#Amazon Auto Scaling 

    Allows you to autometically increase or decrease resources 
    
    2 Step Process
    
    1)  Launch Configuration
          - Template used by Auto scaling group to launch new instances 
          - Similar to EC2 Instance launch steps 
          
    2)  Auto Scaling Group 
          - Configure Auto Scaling Group based on created Launch Configuration
              - Name Auto Scaling Group
              - Number of Instances to start with / Group Size
              - Select Network & Subnet
              - Under Advance , you can select the Load Balancer
          - Configure Scaling Policy 
              - Specify Range
              - Increase & Decrease Policy
              - Create Alram
          - Configure Notifications
          - Configure Tags
          - Review

    LAB:  Create Your First Auto Scaling Group
          Working with Amazon EC2 Auto Scaling Groups
          Launching Auto Scaling Groups Behind a Classic Load Balacer
          
#Amazon Elastic Container Service (ECS)

    