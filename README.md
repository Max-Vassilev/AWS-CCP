# AWS-CCP

Final Summary:


✅ 4 - IAM:
CLI: manage AWS services through terminal (you need access keys)
SDK: manage AWS services through programming code (you need access keys)
Audit: IAM credential report and IAM Access Advisor

✅ 5 - EC2:
Instance types:
- On-demand: Full price, pay as you go.
- Spot: Cheapest, up to 90% off, can be interrupted.
- Reserved standard: Discounted with 1-3 year commitment.
- Reserved convertible: Discounted with flexibility to change types. 
- Dedicated host: Most expensive, you rent a whole physical server.
- Dedicated instance: Cheaper, instances run on dedicated physical hardware but no full server control.

✅ 6- EC2 Storage:
EBS: Network drive attached to 1 EC2 (mapped to 1 AZ), used for backups or switching to EC2 in another AZ
AMI: Ready to use EC2 instances with customisations
EC2 Instance Store: High-performance hardware disc attached to EC2, but lost when the instance is stopped (even for 1 minute)

EFS: Network file system, can be attached to many EC2’s in 1 Region
EFS-IA: Cheaper but for infrequent use
FSx: Network file system for windows

✅ 7- ELB & ASG:
Availability: when the app is in multiple AZ’s 
Scalability (vertical and horizontal)
Elasticity: automatically scale up and down based on demand
Agility: work faster by creating and deleting resources in the cloud quickly
ELB types:
- Application LB: For web (HTTP/HTTPS) traffic.
- Network LB: For fast TCP traffic.
- Gateway LB: Routes traffic to virtual appliances (like firewalls).

✅ 8 - S3:
Buckets and objects are tied to a Region
Bucket policy: With it you can grant public access to S3 bucket
AWS Lifecycle Rules automatically move or delete S3 files based on rules you set to save costs.
S3 Versioning: different versions of an object (file)
S3 Replication (same region and cross-region): copy S3 objects to another bucket2
Storage Gateway: connects on-premises storage to AWS cloud storage for hybrid setups.
S3 Storage Classes:
- Standard: For frequent, fast access.
- IA: Less frequent access, cheaper.
- 1Z-IA: Like IA but stored in one zone, cheaper, less durable.
- Intelligent tiering: Moves data between tiers based on use (example standard —> IA).
- Glacier - instant: Rare access to archived data, instant retrieval, very cheap.
- Glacier - flexible: Rare access to archived data, retrieval in minutes/hours, cheaper.
- Glacier - deep: Very rare access to archived data, retrieval in hours, cheapest.
Snow family: physical devices for moving large data sets to/from AWS (Snowcone - up to 8TB, Snowball - up to 80TB, Snowmobile).
OpsHub: graphical tool to manage Snow devices easily.
Datasync: Helps you move large amounts of data quickly and securely between on-premises storage, AWS services, or between AWS services (like S3, EFS, FSx)
Storage Gateway: Extend on-premises storage with S3

✅ 9 - Databases & Analytics:
Relational DB: Good for OLTP, RDS and Aurora (MySQL and PostgreSQL)
Athena: Serverless SQL queries on data stored in S3
Multi-AZ: Backup database in another AZ to avoid downtime
Read Replicas: Copies used only for reading to make data faster and reduce load
Multi-Region: Copies in other Regions for safety and speed
In-memory: ElastiCache
Key/Value: DynamoDB (serverless, NoSQL) & DAX (cache for DynamoDB)
Redshift: Warehouse and analytical processing (SQL can be used to query data)
EMR: Hadoop cluster
Quicksight: dashboards on your data
DocummentDB: MongoDB (also NoSQL)
QLDB: Financial transactions, cryptographically verifiable
Glue: ETL
Neptune: Graph database
Timestream: Time-series DB

✅ 10 - Other Compute Services:
ECS (for Docker): you provide the EC2 instances
Fargate: Same but serverless 
ECR: Store images
Batch: run batch jobs on many EC2 instances
Lightsail: Simplified AWS
Lambda: serverless function as a service, billing per call and per duration
API Gateway: expose lambda function as HTTP API

✅ 11 - Deployments and Managing Infrastructure at Scale:
CloudFormation: IaC
Beanstalk: PaaS for deploying code (example: ELB + EC2 + RDS)
CodeCommit: Git
CodeBuild: CI
CodeDeploy (hybrid): CD
CodePipeline: CI/CD
Systems Manager (hybrid): Manage EC2 and on-prem servers, identify issues, see their status, automate patching and run tasks at scale
CodeArtifact: Store dependancies 
AWS CDK: IaC with different programming languages (compiles to CloudFormation template)

✅ 12 - Global Applications in AWS:
Route 53: global DNS, route users to closest deployment with least latency, great for disaster recovery
CloudFront: Replicate part of your app at Edge locations and cache common requests to decrease latency
S3 Global Acceleration: Use Edge locations to speed up upload and download from S3 buckets
AWS Global Accelerator: improve global application availability and performance using the AWS global network
AWS Outposts: Deploy AWS Racks in your own data center
WaveLength: 5G
AWS Local Zones: bring apps closer to users (Boston, Miami, and others)

13 - Cloud Integrations:
SQS: queue service used do decouple applications in AWS
SNS: Notification service
Kenisis: Real-time data streaming
Amazon MQ: Message broker (supports RabbitMQ, Apache ActiveMQ and others)

14 - Cloud Monitoring:
CloudWatch: Monitoring service that collects and tracks metrics, stores and analszes logs, and responds to system changes through alarms.
CloudTrail: audit API calls
CloudTrail Insights: Automated analysis for the CloudTrail data
X-ray: Analyse and debug applications, such as those build with microservices architecture
AWS Health Dashboard: Status about ALL services
AWS Account Health Dashboard: Status of services that impact your infrastructure
CodeGuru: Automated code review

15 - VPS & Networking:
A VPC has subnets inside it
A subnet is public (accessible from the internet) when it has Internet gateway
To access private subnets you need NAT Gateway
Stateless firewall for a sublet -Network ACL
EC2 firewall: Security Group
VPC Peering: Connect 2 VPS’s together
Elastic IP: Fixed IP that costs money even if not used
VPC Endpoint: Private access to AWS services from a VPC
Private link: Privately connect to a service in 3rd party VPC
Site to Site VPC: Connect data center to VPC using public network
ClientVPN: Open VPN Connection to your VPC from your computer
Direct Connect: direct private connection to AWS
Transit Gateway: Connect many VPC’s and on-premises networks together

16 - Security and Compliance:
Shield: DDOS protection
KMS: Encryption - AWS manages the keys
CloudHSM: Encryption - You manage your keys
AWS Certificate Manager: SSL/TLS certificates
Artefact: Access to compliance reports
GuardDuty: Find malicious behaviour by analysing VPC and CloudTrail logs
AWS Inspector: Find software vulnerabilities in EC2, ECR, Lambda
AWS Detective (ML service): Deeper analysis - identify root cause of issues
Network firewall: firewall for a VPC
Config: Track configuration changes and compliance against rules
Macie: Find sensitive data in S3 buckets
CloudTrail: Track and audit API calls made by used within account
AWS SecurityHub: gather security findings from multiple AWS accounts
Firewall manager: Manage security rules across an Organisation
Trusted Advisor: analyses your cloud setup for security, cost, performance, reliability, and limits

17 - Machine Learning:
Rekognition: Recognises things from images
Transcribe: Speech to text
Polly: Text to speech
Amazon Lex: Chatbots
Connect: Cloud contact center
Comprehend: NLP - Natural Language Processing
SageMaker: Build machine learning models
Kendra: Document search (S3, RDS, Google drive and other sources)
Personalise: personalised recommendations  

18 - Account Management, Billing and Support:
Compute optimiser: recommends resource configurations to reduce cost
Pricing Calculator: Estimate cost of services
Billing Dashboard: High-level + available with free tier
Cost Allocation Tags: Tag resources to create detailed reports
Cost and Usage Reports: Most complete billing dataset
Cost Explorer: View detailed current usage + forecast
Billing Alarms: in us-east-1, part of CloudWatch
Budgets: More advanced, also alarms
Savings Plan: save money with long term usage of AWS Cost Anomaly Detection: Detect unusual spending using ML
Service Quotas: Helps you track and manage the limits (quotas) of AWS resources (like number of EC2 instances), and notifies you when you're close to reaching them.

19 - Advanced Identity:
Security Token Service (STS): Issue temporary limited-access credentials to access AWS services
Cognito: Create users database for mobile/web app
Directory Services: Integrate Microsoft active directory in AWS
IAM Identity Center: 1 login for multiple AWS users

20 - Other Services:
AWS WorkSpaces: Cloud desktops (Windows/Linux) for users DaaS
AppStream 2.0: Stream individual desktop apps to a browser.
Elastic Transcoder:  Converts media files (S3) to different formats for various devices.
AppSync: GraphQL
AWS Amplify: Toolset to build, deploy, and host full-stack web and mobile apps quickly.
AWS Infrastructure composer: Drag and drop service for IaC
AWS Device Farm: Service to test your mobile and web apps on real devices (iOS, Android, and more) in the cloud.
AWS Backup: Copying data to a separate location so it can be restored if lost or damaged.
Disaster Recovery Strategy: Cheapest: Backup and Restore, Most expensive: Multi-site/Hot-site
EDR (elastic disaster recovery): Replicates servers in real time and lets you quickly recover them as EC2 instances during a disaster.
DaraSync: Move large amount of data from on-premises to AWS (S3, EFS, FSX for windows) incremental.

7 Rs of Cloud Migration:
1. Retire – Stop using apps that are no longer needed.
2. Retain – Keep the app where it is (don’t move it).
3. Rehost – Move the app to the cloud without changes (lift and shift).
4. Relocate – Move many servers or systems to the cloud all at once.
5. Repurchase – Replace the app with a cloud version (like switching to a SaaS tool).
6. Replatform – Make small changes to improve performance in the cloud.
7. Refactor – Completely rebuild the app to take full advantage of the cloud.

AWS Application Migration Service: Moves on-premises servers to AWS quickly with minimal downtime.
AWS Migration Evaluator: Analyses your servers and gives cost and migration recommendations for AWS.
AWS Migration Hub: Central location to track your migration.
AWS Step Functions: Runs tasks in order to automate workflows.
AWS Pinpoint: Send and receive SMS’s (or email) for marketing campaigns 

21 - AWS Architecting and Ecosystem:

Well Architected Framework - 6 pillars:
Operational Excellence: Run and monitor systems, improve processes.
- Use IaC
- Make small, frequent and reversible changes
- Anticipate failiure
Security: Protect data, systems, and assets.
Reliability: Ensure systems recover and work as intended.
Performance Efficiency: Use resources efficiently as demand changes.
Cost Optimization: Avoid unnecessary costs.
Sustainability: Minimize environmental impact.

Cloud Architecture Framework:
…








Unknown: 
CloudEndure Disaster Recovery: Continuously replicates your servers to AWS for fast disaster recovery.
AWS IAM Access Analyzer: Finds resources shared outside your account and suggests least-privilege policies.
AWS Managed Services (AMS - Enterprise Plan): Manages AWS operations like monitoring, patching, and backups for enterprises.
MemoryDB: Redis-compatible, in-memory database for low-latency, real-time use cases.
API Gateway: Exposes Lambda and other services via HTTP/REST APIs.
AWS EventBridge: Event bus to connect applications using events from AWS services or custom sources.
File vs Object vs Block Storage in AWS:
* File: For shared file systems (e.g., EFS).
* Object: Stores data as objects (e.g., S3). Good for backups, media.
* Block: Raw storage volumes for EC2 (e.g., EBS). Like a hard drive.
Transit Gateway: Connects multiple VPCs and on-prem networks through a central hub.
Billing Conductor: Customize and group billing info for cost tracking and internal chargebacks.





* Global Accelerator: Speeds up global app traffic using AWS network (use case: fast, static IP access)
* CloudFront: Delivers cached content via CDN (use case: fast website/video/API delivery)
* Local Zones: Provide AWS compute and storage near users (use case: low-latency apps like gaming, media rendering, or real-time data processing)
