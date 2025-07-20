# AWS-CCP

Final Summary:

### 4 - IAM
- CLI: manage AWS services through terminal (you need access keys)  
- SDK: manage AWS services through programming code (you need access keys)  
- Audit: IAM credential report and IAM Access Advisor  

### 5 - EC2  
**Instance types:**  
- On-demand: Full price, pay as you go  
- Spot: Cheapest, up to 90% off, can be interrupted  
- Reserved standard: Discounted with 1–3 year commitment  
- Reserved convertible: Discounted with flexibility to change types  
- Dedicated host: Most expensive, you rent a whole physical server  
- Dedicated instance: Cheaper, runs on dedicated physical hardware but no full server control  

### 6 - EC2 Storage  
- EBS: Network drive attached to 1 EC2 (mapped to 1 AZ), used for backups or switching AZs  
- AMI: Ready-to-use EC2 instances with customizations  
- EC2 Instance Store: High-performance disk, but lost when instance is stopped  

**Network file systems:**  
- EFS: Can be attached to many EC2s in 1 Region  
- EFS-IA: Cheaper for infrequent use  
- FSx: Network file system for Windows  

### 7 - ELB & ASG  
- **Availability:** App deployed across multiple AZs  
- **Scalability:** Vertical and horizontal scaling  
- **Elasticity:** Auto scale based on demand  
- **Agility:** Quickly create and remove resources  

**ELB Types:**  
- Application LB: Web traffic (HTTP/HTTPS)  
- Network LB: Fast TCP traffic  
- Gateway LB: Route traffic to virtual appliances  

### 8 - S3  
- Buckets and objects are tied to a Region  
- Bucket policy: Grants public access if configured  
- Lifecycle Rules: Automatically move/delete files to reduce cost  
- S3 Versioning: Keep multiple versions of a file  
- S3 Replication: Copy objects within or across regions  
- Storage Gateway: Connect on-prem to AWS storage  

**S3 Storage Classes:**  
- Standard: Frequent access  
- IA: Infrequent access, cheaper  
- 1Z-IA: Single AZ, cheaper, less durable  
- Intelligent Tiering: Auto-move based on usage  
- Glacier (Instant, Flexible, Deep): Archived storage options  

**Data Transfer Services:**  
- Snowcone (up to 8TB), Snowball (up to 80TB), Snowmobile  
- OpsHub: GUI for managing Snow devices  
- DataSync: Fast, secure transfer between on-prem and AWS  

### 9 - Databases & Analytics  
- **Relational:** RDS, Aurora (MySQL/PostgreSQL)  
- **Serverless Query:** Athena (on S3)  
- **Multi-AZ:** High availability DB backup  
- **Read Replicas:** Scalable read performance  
- **Multi-Region:** Disaster recovery and latency  

**Others:**  
- ElastiCache (in-memory)  
- DynamoDB (NoSQL) + DAX (cache)  
- Redshift (analytics/data warehouse)  
- EMR (Hadoop)  
- Quicksight (dashboards)  
- DocumentDB (MongoDB-compatible)  
- QLDB (ledger)  
- Glue (ETL)  
- Neptune (graph DB)  
- Timestream (time-series)  

### 10 - Other Compute Services  
- ECS: Docker container management (you provide EC2)  
- Fargate: Serverless containers  
- ECR: Container image storage  
- Batch: Run batch jobs  
- Lightsail: Simplified compute  
- Lambda: Serverless functions, pay per use  
- API Gateway: Expose Lambda as HTTP API  

### 11 - Deployment & Infrastructure Management  
- CloudFormation: Infrastructure as code (IaC)  
- Elastic Beanstalk: PaaS for app deployment  
- CodeCommit: Git repository  
- CodeBuild: Continuous integration  
- CodeDeploy: Hybrid deployments  
- CodePipeline: CI/CD automation  
- Systems Manager: Manage EC2/on-prem, patching, automation  
- CodeArtifact: Package and dependency management  
- AWS CDK: IaC using programming languages  

### 12 - Global Applications  
- Route 53: DNS + latency routing + disaster recovery  
- CloudFront: CDN, edge caching  
- S3 Transfer Acceleration: Faster uploads/downloads via edge  
- Global Accelerator: Improve global app performance  
- Outposts: Run AWS hardware in your datacenter  
- Wavelength: 5G edge compute  
- Local Zones: AWS compute closer to users  

### 13 - Cloud Integrations  
- SQS: Queue service  
- SNS: Push notifications  
- Kinesis: Real-time data streams  
- Amazon MQ: Managed message broker (RabbitMQ, ActiveMQ)  

### 14 - Monitoring  
- CloudWatch: Metrics, logs, alarms  
- CloudTrail: API call auditing  
- CloudTrail Insights: Anomaly detection  
- X-Ray: Debug distributed apps  
- AWS Health Dashboard: AWS-wide service status  
- Account Health Dashboard: Status for your AWS account  
- CodeGuru: ML-powered code reviews  

### 15 - VPC & Networking  
- VPC: Private network for your AWS resources  
- Subnets: Public if attached to Internet Gateway  
- NAT Gateway: Enables internet for private subnets  
- NACL: Stateless firewall  
- Security Group: Stateful EC2 firewall  
- VPC Peering: Connect 2 VPCs  
- Elastic IP: Static IP (costs if unused)  
- VPC Endpoint: Private connection to AWS services  
- PrivateLink: Connect to 3rd-party VPC privately  
- Site-to-Site VPN, Client VPN, Direct Connect  
- Transit Gateway: Hub to connect many VPCs and networks  

### 16 - Security & Compliance  
- Shield: DDoS protection  
- KMS: Encryption with AWS-managed keys  
- CloudHSM: Encryption with customer-managed keys  
- Certificate Manager: Manage SSL/TLS  
- Artifact: Access compliance reports  
- GuardDuty: Detect threats  
- Inspector: Scan for vulnerabilities  
- Detective: Root cause analysis  
- Network Firewall: VPC-level firewall  
- Config: Track config changes  
- Macie: Sensitive data in S3  
- CloudTrail: API call logging  
- SecurityHub: Centralized security view  
- Firewall Manager: Enforce security rules  
- Trusted Advisor: Cost, performance, limits, security insights  

### 17 - Machine Learning  
- Rekognition: Image/video analysis  
- Transcribe: Speech to text  
- Polly: Text to speech  
- Lex: Build chatbots  
- Comprehend: NLP  
- SageMaker: Build/train ML models  
- Kendra: Intelligent search  
- Personalize: Recommendations  
- Connect: Call center with ML  

### 18 - Billing & Account Management  
- Compute Optimizer: Recommend instance types  
- Pricing Calculator: Estimate monthly cost  
- Billing Dashboard: High-level summary  
- Cost Allocation Tags: Track spending by tag  
- Cost & Usage Reports: Detailed billing dataset  
- Cost Explorer: Visualize spending and forecast  
- Billing Alarms: Part of CloudWatch (us-east-1)  
- Budgets: More advanced alerts  
- Savings Plan: Commit to save over time  
- Cost Anomaly Detection: ML-based anomaly alerts  
- Service Quotas: Track resource limits  

### 19 - Advanced Identity  
- STS: Temporary credentials  
- Cognito: User identity for apps  
- Directory Services: Integrate Active Directory  
- IAM Identity Center: Centralized access for multiple accounts  

### 20 - Other Services  
- WorkSpaces: Cloud desktops  
- AppStream 2.0: Stream desktop apps to browsers  
- Elastic Transcoder: Convert media formats  
- AppSync: GraphQL APIs  
- Amplify: Full-stack app platform  
- Infrastructure Composer: Drag-and-drop IaC  
- Device Farm: Test apps on real mobile devices  
- AWS Backup: Centralized backup tool  
- Disaster Recovery Strategies:
  - Backup & Restore (cheapest)  
  - Multi-site / Hot-site (most expensive)  
- EDR: Real-time replication for fast failover  
- DataSync: Move large datasets from on-prem to AWS  

**7 Rs of Cloud Migration:**  
1. Retire: Remove unused apps  
2. Retain: Keep on-prem  
3. Rehost: Lift-and-shift  
4. Relocate: Move many VMs to cloud  
5. Repurchase: Switch to SaaS  
6. Replatform: Minor cloud optimizations  
7. Refactor: Re-architect for the cloud  

- Application Migration Service: Move on-prem servers to AWS  
- Migration Evaluator: Cost and migration planning  
- Migration Hub: Track all migrations  
- Step Functions: Serverless workflows  
- Pinpoint: Send/track marketing messages (SMS, email, etc.)  

### 21 - Architecting & Ecosystem  
**Well-Architected Framework (6 Pillars):**  
- Operational Excellence  
  - Use IaC  
  - Small, reversible changes  
  - Anticipate failure  
- Security  
- Reliability  
- Performance Efficiency  
- Cost Optimization  
- Sustainability  

**Cloud Architecture Framework:**  
- Guidance for building secure, scalable systems  

---

### Extra Notes  
- **CloudEndure Disaster Recovery**: Real-time replication to AWS  
- **IAM Access Analyzer**: Detect public/shared resources  
- **AWS Managed Services (AMS)**: Enterprise-level managed operations  
- **MemoryDB**: Redis-compatible, low-latency DB  
- **API Gateway**: Expose Lambda via HTTP/REST  
- **EventBridge**: Serverless event bus  
- **Storage Types in AWS:**
  - File: Shared systems (EFS)  
  - Object: S3 (media, backups)  
  - Block: EBS (raw volumes)  

- **Billing Conductor**: Custom billing views and chargebacks  
- **Global Accelerator**: Speed up global apps (static IP)  
- **CloudFront**: CDN for fast content delivery  
- **Local Zones**: AWS compute/storage near end users (low latency)
