# CS470-FullStackII
**Project Overview**
This project showcases a complete full-stack application (lafs-web - Learn Angular From Scratch Web) deployed in a cloud environment using modern DevOps practices. The application demonstrates proficiency in:

Full-Stack Development: Building responsive web applications with Angular front-end and Node.js back-end
Cloud Infrastructure: Deploying and managing applications on AWS
Containerization: Using Docker for consistent development and deployment environments
Serverless Architecture: Implementing AWS Lambda functions and API Gateway
NoSQL Database Management: Working with Amazon DynamoDB
Static Asset Delivery: Utilizing Amazon S3 for content storage and delivery

Academic Context
This repository represents the culmination of CS 470 coursework, demonstrating the practical application of cloud computing concepts, microservices architecture, and modern web development practices. The project evolved through multiple iterations, from initial setup through API development, testing, and final deployment.
Architecture
The application utilizes a modern cloud-native architecture built on AWS services. The front-end Angular application is containerized using Docker for consistent development and deployment. The back-end leverages serverless AWS Lambda functions accessible through API Gateway, with data persistence in DynamoDB and static assets served from S3.
Component Overview
Front-End Layer:

Angular 7.2 single-page application
Angular Material components for UI
Responsive design supporting all device sizes
Hosted on Amazon S3 with CloudFront CDN

API Layer:

AWS API Gateway managing RESTful endpoints
Request validation and transformation
CORS configuration for cross-origin requests
Throttling and API key management

Compute Layer:

AWS Lambda functions for serverless backend logic
Event-driven execution model
Automatic scaling based on demand
Integration with DynamoDB for data operations

Data Layer:

Amazon DynamoDB for NoSQL data storage
On-demand capacity mode for cost optimization
Point-in-time recovery enabled
Global secondary indexes for efficient queries

Storage Layer:

Amazon S3 for static asset storage
Versioning enabled for data protection
Lifecycle policies for cost management

Technologies Used
Front-End

Angular 7.2 - Modern web application framework
Angular Material 7.3 - Material Design UI components
TypeScript 3.2 - Type-safe JavaScript
SCSS - Enhanced CSS with variables and mixins
RxJS 6.3 - Reactive programming library
Bootstrap 3.4 - Responsive grid and utilities
Font Awesome 4.7 - Icon library

Back-End & Cloud Services

Node.js 10 - JavaScript runtime environment
AWS Lambda - Serverless compute functions
API Gateway - RESTful API management
DynamoDB - NoSQL database service
Amazon S3 - Object storage for static assets
CloudFront - Content delivery network

Development & DevOps

Docker - Container platform for consistent environments
Docker Compose - Multi-container orchestration
Git - Version control system
npm - Package management
Angular CLI 7.3 - Command-line development tools

Testing & Quality Assurance

Karma 4.0 - Test runner
Jasmine 2.99 - Behavior-driven testing framework
Protractor 5.4 - End-to-end testing framework
TSLint 5.11 - TypeScript static analysis tool
Codelyzer 4.5 - Angular-specific linting rules

Features
Application Features

Responsive design that works on all devices and screen sizes
Material Design interface providing modern, intuitive user experience
Fast performance through optimized builds and lazy loading
Secure authentication and authorization via AWS services
Dynamic content delivery from DynamoDB database
Global content distribution via CloudFront CDN
Real-time data updates and state management

Technical Features

Containerized development environment ensuring consistency across machines
Cloud-native architecture designed for scalability and resilience
Structured for CI/CD integration and automated deployment pipelines
Comprehensive code documentation and inline comments
Unit testing and end-to-end testing coverage
Environment-based configuration management
Optimized production builds with code splitting and tree shaking

Docker Configuration Details
The Dockerfile includes:

Node.js 10 base image for compatibility
Angular CLI 6 LTS global installation
Dependency resolution for Browserslist compatibility
Sass compilation compatibility with Node 10
Legacy CSS/PostCSS stack pinned to compatible versions
Port 4200 exposure for development server
Auto-install and serve configuration

The docker-compose.yml provides:

Service definition for the web application
Port mapping (4200:4200) for local access
External network configuration (lafs-net)
Command to install dependencies and start server
Volume mounting for live code reloading during development

AWS Cloud Infrastructure
Services Implemented
Amazon DynamoDB

NoSQL database for application data persistence
On-demand capacity mode for automatic scaling and cost optimization
Global secondary indexes for efficient query patterns
Point-in-time recovery enabled for data protection
Encryption at rest using AWS-managed keys
DynamoDB Streams for event-driven processing

AWS Lambda

Serverless compute for backend business logic
Event-driven execution model triggered by API Gateway
Automatic scaling based on request volume
Integration with DynamoDB for data operations
Environment variable configuration for secrets management
CloudWatch Logs integration for monitoring and debugging

API Gateway

RESTful API endpoints for client-server communication
Request validation and data transformation
CORS configuration for cross-origin resource sharing
API key management and usage plans
Request throttling to prevent abuse
Integration with Lambda functions via proxy integration
Stage management for development, testing, and production

Amazon S3

Static asset storage for images, documents, and files
Versioning enabled for data protection and rollback capability
Lifecycle policies for automatic archival and deletion
Public read access configuration for web assets
Server-side encryption for data security
Cross-region replication for disaster recovery

AWS IAM

Role-based access control for AWS services
Least privilege principle in policy definitions
Service-to-service authentication using IAM roles
Secure credential management without hardcoded secrets
Policy simulation for testing before deployment

Deployment Architecture
The application follows AWS best practices for cloud deployment:
High Availability: Services are distributed across multiple AWS availability zones to ensure resilience against infrastructure failures.
Scalability: Serverless services (Lambda, API Gateway, DynamoDB) automatically scale to handle traffic increases without manual intervention.
Security: All data in transit is encrypted using HTTPS/TLS. Data at rest is encrypted using AWS-managed encryption keys. IAM policies enforce strict access controls.
Cost Optimization: On-demand pricing models and serverless architecture ensure costs scale with actual usage rather than provisioned capacity.
Monitoring: CloudWatch provides comprehensive monitoring, logging, and alerting for all AWS services.

Environment Variables
The application uses environment-specific configurations defined in:

src/environments/environment.ts - Development configuration
src/environments/environment.prod.ts - Production configuration

Key configuration values include:

API Gateway endpoint URLs
AWS region settings
DynamoDB table names
S3 bucket names
Feature flags

Learning Outcomes
Through the completion of this project, the following competencies were developed:
Cloud Computing Skills

Hands-on experience deploying and managing applications on AWS
Understanding of serverless architecture patterns and use cases
Proficiency with core AWS services: Lambda, API Gateway, DynamoDB, S3, IAM
Knowledge of cloud cost optimization strategies
Experience with Infrastructure as Code principles

Containerization and DevOps

Docker container creation and management
Docker Compose for multi-container orchestration
Understanding of container networking and volumes
Creating reproducible development environments
Preparing applications for container-based deployment

Full-Stack Development

Building single-page applications with Angular framework
Implementing responsive, mobile-first user interfaces
Working with TypeScript for type-safe application development
Managing application state and data flow
Integrating front-end applications with RESTful APIs

API Development

Designing RESTful API endpoints
Implementing proper HTTP methods and status codes
Request validation and error handling
API documentation and testing
CORS configuration for web applications

Database Management

Working with NoSQL database design patterns
DynamoDB table design and partition key selection
Creating and using global secondary indexes
Understanding eventual consistency models
Optimizing queries for performance

Software Engineering Practices

Version control with Git and GitHub
Code organization and modular architecture
Unit testing and end-to-end testing
Code quality tools and linting
Documentation and technical writing
