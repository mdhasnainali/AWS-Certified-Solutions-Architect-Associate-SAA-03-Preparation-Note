# AWS Certified Solutions Architect – Associate (SAA-C03) Notes

Study notes for the AWS SAA-C03 exam. Each note starts with a **Core idea**, then covers the topic, and ends with a summary, self-check questions and key terms.

Course slides: [AWS_SAA-C03_Slides.pdf](resources/AWS_SAA-C03_Slides.pdf)

## Study Plan

### Step 1 — Get a free AWS account

Reading alone is not enough. Build things.

- Sign up at [aws.amazon.com/free](https://aws.amazon.com/free/) and choose the **Free plan**.
- New accounts get **$100 credit at sign-up**, plus **$20 each** (up to $100 more) for five starter tasks: launch an EC2 instance, create an RDS database, build a Lambda function, use Amazon Bedrock, and set up an AWS Budget. All five are exam topics — do them.
- The free plan lasts **6 months or until credits run out**, whichever comes first. You are not charged unless you upgrade to a paid plan.
- Check your balance in the console's **Explore AWS** widget or **Billing → Credits**.

**Stay safe while practicing:**
- Turn on **MFA** for the root user, then create an IAM user for daily work ([IAM basics](01_access_control/01_IAM_basic.md)).
- Create an **AWS Budget** with an email alert on day one.
- Delete what you build when the lab is done: EC2, NAT Gateways, RDS, load balancers and Elastic IPs keep costing money while they exist.
- Use one region (e.g. `us-east-1`) so nothing gets forgotten in another region.

### Step 2 — Learn the topics in order

Go through folders `01` → `17`. They follow the course order, and later topics build on earlier ones.

For each note:
1. Read the matching section in the [slides](resources/AWS_SAA-C03_Slides.pdf).
2. Read the note. Start with the **Core idea**, then the body.
3. **Do it in the console.** Launch the instance, create the bucket, attach the policy. One hands-on lab beats three re-reads.
4. Answer the **Check Yourself** questions without looking. Re-read only what you missed.
5. Skim **Key Terms** — if a term feels unfamiliar, go back to it.

### Step 3 — Learn with an AI assistant

Use an AI chat (Claude, ChatGPT, etc.) as a personal tutor. Paste a note or a section and try prompts like:

| Goal | Prompt |
|---|---|
| Understand | "Explain VPC endpoints like I'm new to networking, with a real-world analogy." |
| Compare | "Gateway endpoint vs interface endpoint — when do I pick each? Give exam keywords." |
| Quiz | "Ask me 10 SAA-C03 scenario questions on S3 storage classes, one at a time. Grade each answer and explain." |
| Find gaps | "Here is my note on RDS. What exam-relevant topics are missing?" |
| Fix mistakes | "I chose SQS but the answer was Kinesis. Why? What clue word did I miss?" |
| Hands-on | "Give me a step-by-step console lab for an ALB with Auto Scaling, and the clean-up steps after." |
| Revise | "Make 20 flashcards from this note." |

Tips:
- Ask **why** the wrong options are wrong, not only why the right one is right.
- AWS changes often. If an answer sounds off, check the official AWS docs or FAQ.
- Never paste access keys or account IDs into a chat.

### Step 4 — Take the practice tests

After learning everything, take the [practice tests](https://www.udemy.com/course/aws-certified-solutions-architect-associate-practice-tests-k/) (Udemy).

- Take each test **timed** (65 questions, 130 minutes) to build exam stamina.
- Review **every** question after, including the ones you got right by guessing.
- Write down weak topics and go back to those notes.
- Aim for **80%+** on practice tests before booking the real exam (pass mark is 720/1000).

### Step 5 — Final revision

In the last week, revise with [`00_exam_guide`](00_exam_guide):
- [Exam preparation](00_exam_guide/01_exam_preparation.md) — format, domains, test-day rules.
- [Decision guide](00_exam_guide/02_exam_patterns_decision_guide.md) — clue word → service.
- [Stories](00_exam_guide/03_exam_patterns_stories.md) — one story per service.
- [Quick notes](00_exam_guide/04_all_topics_quick_notes.md) — every topic on one page for the day before.

Exam-day reminders: answer every question (no penalty for wrong answers), flag hard ones and come back, and watch the last words — *cheapest*, *least effort*, *most available*, *most secure* — they decide the answer.

## Contents

### 00 · Exam Guide
- [Exam preparation — format, domains, test-day rules](00_exam_guide/01_exam_preparation.md)
- [Exam patterns — service decision guide](00_exam_guide/02_exam_patterns_decision_guide.md)
- [Exam patterns — stories, pictures and answers](00_exam_guide/03_exam_patterns_stories.md)
- [All topics — quick notes](00_exam_guide/04_all_topics_quick_notes.md)

### 01 · Access Control
- [IAM basics](01_access_control/01_IAM_basic.md)
- [Organizations and IAM advanced](01_access_control/02_Organizations_and_IAM_advanced.md)

### 02 · Compute
- [EC2 basics](02_compute/01_basic_EC2.md)
- [EC2 advanced](02_compute/02_advanced_EC2.md)
- [EC2 instance storage — EBS, AMI, Instance Store, EFS](02_compute/03_EC2_instance_storage.md)

### 03 · Scalability and High Availability
- [Load balancing and Auto Scaling](03_scalability_and_high_availability/01_load_balancer_and_auto_scaling.md)

### 04 · Database
- [RDS, Aurora and ElastiCache](04_database/01_RDS_Aurora_ElastiCache.md)
- [Choosing a database](04_database/02_choosing_a_database.md)

### 05 · DNS
- [Route 53](05_dns/01_route53.md)

### 06 · Solution Architect Decisions
- [Basic architecture discussions](06_solution_architect_decisions/01_basic.md)
- [Serverless architectures](06_solution_architect_decisions/02_serverless_architectures.md)
- [Well-Architected Framework and Trusted Advisor](06_solution_architect_decisions/03_well_architected_and_trusted_advisor.md)

### 07 · Storage
- [S3 basics](07_storage/01_S3_basic.md)
- [S3 advanced](07_storage/02_S3_advanced.md)
- [S3 security](07_storage/03_S3_security.md)
- [Hybrid storage and data migration — Snow, FSx, Storage Gateway, DataSync](07_storage/04_hybrid_storage_and_migration.md)

### 08 · CDN
- [CloudFront and Global Accelerator](08_cdn/01_CloudFront_and_Global_Accelerator.md)

### 09 · Integration and Messaging
- [SQS, SNS, Kinesis, Amazon MQ](09_integration_and_messaging/01_SQS_SNS_Kinesis_MQ.md)

### 10 · Containers
- [ECS, EKS, Fargate, ECR, App Runner](10_containers/01_ECS_EKS_Fargate_ECR.md)

### 11 · Serverless
- [Lambda, DynamoDB, API Gateway, Step Functions, Cognito](11_serverless/01_Lambda_DynamoDB_API_Gateway.md)

### 12 · Data and Machine Learning
- [Data analytics — Athena, Glue, Redshift, EMR, OpenSearch, QuickSight, MSK](12_data_and_ml/01_data_analytics.md)
- [Machine learning services](12_data_and_ml/02_machine_learning.md)

### 13 · Monitoring
- [CloudWatch, EventBridge, CloudTrail, Config](13_monitoring/01_CloudWatch_CloudTrail_Config.md)

### 14 · Security
- [Encryption, KMS, Secrets, ACM, WAF, Shield, GuardDuty](14_security/01_encryption_and_security.md)

### 15 · Networking
- [VPC and networking](15_networking/01_VPC.md)

### 16 · Disaster Recovery
- [Disaster recovery and migrations](16_disaster_recovery/01_disaster_recovery_and_migration.md)

### 17 · Other Services
- [Other services — exam quick hits](17_other_services/01_other_services.md)
