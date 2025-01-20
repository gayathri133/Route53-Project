# Secure Custom Web Hosting using Route 53

## Project Overview
This project demonstrates the implementation of a secure and scalable custom web hosting solution using Amazon Route 53, S3, ACM, and CloudFront. The goal is to host a website accessible via a custom domain name with enhanced security, performance, and global availability.

---

## Features
- **Domain Management**: Leverages Amazon Route 53 for DNS management and custom domain name configuration.
- **Security**: Implements HTTPS using SSL/TLS certificates issued via AWS Certificate Manager (ACM).
- **Performance**: Utilizes Amazon CloudFront for content delivery and caching, ensuring low latency and high-speed access.
- **Storage**: Hosts static assets securely in an Amazon S3 bucket.
- **Scalability and Availability**: Ensures reliable global access through CloudFront's edge locations and Route 53 routing.

---

## Architecture Diagram
A serverless and distributed architecture is implemented:
1. **Frontend Tier**:
   - Static content hosted in an S3 bucket.
   - Secured with HTTPS via CloudFront and ACM.
2. **Domain Management**:
   - Amazon Route 53 for custom domain name routing.
   - Configured DNS records (A, CNAME) for CloudFront distribution.
3. **Content Delivery Network**:
   - CloudFront ensures global delivery with caching and reduced latency.

---

## Prerequisites
- An AWS account.
- A registered custom domain (managed or transferred to Route 53).
- Basic understanding of AWS services like S3, Route 53, ACM, and CloudFront.

---

## Services Used
1. **Amazon Route 53**:
   - DNS management for custom domain.
   - Health checks and routing policies for reliability.
2. **Amazon S3**:
   - Secure static asset hosting.
   - Static website hosting enabled.
3. **AWS Certificate Manager (ACM)**:
   - SSL/TLS certificate provisioning for HTTPS.
4. **Amazon CloudFront**:
   - Content Delivery Network (CDN) for secure and fast content distribution.

---

## Setup Instructions
1. **Domain Configuration**:
   - Register or transfer your domain to Route 53.
   - Create a hosted zone and set up DNS records for the custom domain.

2. **SSL/TLS Setup**:
   - Use ACM to request a public certificate for your domain.
   - Attach the certificate to the CloudFront distribution.

3. **Deploy Frontend**:
   - Upload static assets (HTML, CSS, JS) to an S3 bucket.
   - Enable static website hosting and configure permissions.

4. **Configure CloudFront**:
   - Create a CloudFront distribution pointing to the S3 bucket as the origin.
   - Attach the SSL/TLS certificate to enable HTTPS.

5. **Testing**:
   - Verify DNS configuration and domain accessibility via Route 53.
   - Test HTTPS connection and CloudFront performance.
   - Ensure proper caching and content delivery behavior.

---

## Security Considerations
- Enable encryption at rest and in transit for all resources.
- Use IAM roles and policies to secure access to AWS resources.
- Configure S3 bucket policies to prevent unauthorized access.
- Monitor access logs in CloudFront for potential security issues.

---

## Project Documentation  
For detailed architecture diagrams, configurations, and additional notes, refer to the "Route53 Project Documentation.docx" 

