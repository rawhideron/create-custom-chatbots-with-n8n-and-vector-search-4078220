# Build with AI: Create Custom Chatbots with n8n and Vector ```mermaid
graph TB
Internet([Internet Traffic])

subgraph VPC["VPC (Virtual Private Cloud)"]
subgraph PublicSubnets["Public Subnets"]
ALB[Application Load Balancer]
end

subgraph PrivateSubnets["Private Subnets"]
subgraph ECSCluster["ECS Cluster"]
subgraph ECSService["ECS Service"]
Task1[ECS Task/Container 1]
Task2[ECS Task/Container 2]
Task3[ECS Task/Container 3]
end
end
end

TG[Target Group]
ASG[Auto Scaling]
SG1[Security Group - ALB]
SG2[Security Group - ECS Tasks]
end

IAM[IAM Roles & Policies]

Internet --> ALB
ALB --> TG
TG --> Task1
TG --> Task2
TG --> Task3
ASG -.monitors & scales.-> ECSService
SG1 -.controls traffic.-> ALB
SG2 -.controls traffic.-> Task1
SG2 -.controls traffic.-> Task2
SG2 -.controls traffic.-> Task3
IAM -.provides permissions.-> ECSService

style TG fill:#ff9999
style ALB fill:#99ccff
style ECSService fill:#99ff99
style ASG fill:#ffcc99
```


This is the repository for the LinkedIn Learning course `Build with AI: Create Custom Chatbots with n8n and Vector Search`. The full course is available from [LinkedIn Learning][lil-course-url].

![lil-thumbnail-url]

## Course Description

In this practical, scenario-driven course, AI expert Tobias Zwingmann shows you how to build an AI-powered customer support chatbot using n8n and a Large Language Model (LLM) of your choice. Step by step, design a bot that starts small—handling common FAQs with a well-crafted prompt—then level it up by connecting it to Pinecone, enabling deep searches across your documentation, policies, or product data. Learn the tools you need to know through the hands-on experience of solving a real problem. When you complete this course, you will have mastered the core concepts of building custom AI chatbots with n8n and gained insight into moving toward production-ready deployment. Whether you’re in ops, support, or product, this course gives you an edge in experimenting quickly with practical, high-impact AI workflows.

## Instructor

Tobias Zwingmann

AI expert, Author, Keynote Speaker

Check out my other courses on [LinkedIn Learning](https://www.linkedin.com/learning/instructors/tobias-zwingmann?u=104).


[0]: # (Replace these placeholder URLs with actual course URLs)

[lil-course-url]: https://www.linkedin.com/learning/build-with-ai-create-custom-chatbots-with-n8n
[lil-thumbnail-url]: https://media.licdn.com/dms/image/v2/D560DAQHh202gUT8nOQ/learning-public-crop_675_1200/B56ZhcZBvcG4Ac-/0/1753896722337?e=2147483647&v=beta&t=xIHBhgJeRo9hzwG8KnBpR9gl6tcv0w41ZbOtMGZiF5E

