# Photo & Video Upload Website - AWS Architecture Design Project

## Project Overview
This project presents a serverless, event-driven AWS architecture for scaling a multimedia upload and management platform. Our team designed this architecture as part of the **COS20019: Cloud Computing Architecture** course at Swinburne University of Technology, Vietnam. This project supports high traffic, efficient processing, and secure management of multimedia content, leveraging AWS managed services to ensure scalability, reliability, and cost-effectiveness.

### Team Members
- **Thanh Nam Vu** - Student ID: 104991276
- **Alexander Rigato** - Student ID: 105338913
- **Phuong Bao Minh Nguyen** - Student ID: 104339685
- **Hoai Thuong Triet Nguyen** - Student ID: 103522028

### Course Information
- **Tutorial Session**: Thursday, 4:30 PM

## Project Objectives
- **Scalability**: Implement a serverless, auto-scaling AWS architecture that can handle rapid traffic growth.
- **Efficient Media Processing**: Use AWS services to process media files asynchronously, allowing for thumbnail creation, video transcoding, and image labeling.
- **Secure and Accessible Storage**: Store uploaded media and metadata securely while enabling efficient access and retrieval.
- **Event-Driven Workflow**: Employ an event-driven design with SNS and SQS for decoupling processes, optimizing resource usage, and improving response times.

## Architecture Overview
This architecture uses a suite of AWS services to deliver high performance and scalability for a global audience. Here are the primary components:

1. **AWS Route 53**: Manages DNS and routes user traffic to the application.
2. **AWS WAF**: Provides security by filtering and protecting the application from malicious requests.
3. **AWS CloudFront**: Accelerates content delivery by caching static and dynamic content globally.
4. **Amazon API Gateway**: Acts as a gateway to backend services, handling API requests and forwarding them to Lambda functions.
5. **AWS Lambda**: Runs backend processing, such as media processing and metadata handling, without the need for server management.
6. **Amazon S3**: Stores multimedia files, including raw uploads, processed outputs, and thumbnails.
7. **Amazon DynamoDB**: Stores metadata associated with each media file, facilitating fast and efficient access.
8. **SNS & SQS**: Manages asynchronous task distribution for smooth processing of media workflows.
9. **AWS Rekognition & MediaConvert**: Enhances the application with features like AI-based labeling and adaptive bitrate streaming for videos.
10. **IAM Roles**: Ensures secure access to services within the AWS ecosystem.

## Features
- **Photo & Video Upload**: Users can upload media files through a web or mobile interface.
- **Metadata Management**: Metadata for each upload (e.g., name, description, creation date) is stored in DynamoDB for quick access.
- **Automated Processing**: The system processes media to generate labels, thumbnails, and transcodes videos upon upload.
- **User-Friendly Interface**: Displays uploaded media in a table format with fields for each file's name, description, date, and tags.

## Architecture Diagrams
### Frontend Workflow
![Frontend Diagram](Front%20end%20diagram.png)

### Backend Workflow
![Backend Diagram](Back%20end%20diagram.png)

### Complete AWS Architecture
<img src="https://github.com/NathanVuSwinburne/AWS_Cloud_Computing_Project/blob/main/AWS%20Archirtecture%20diagram.png" />

## Instructions to Run the Project
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/YOUR_USERNAME/AWS_Cloud_Computing_Project.git
## Deploy on AWS
1. **Set up AWS services** according to the architecture diagrams.
2. **Configure IAM roles** to ensure secure access to all components.

## Access the Application
- **Use the web/mobile interface** to test media uploads.
- **View uploaded media** along with its metadata and other details.

## Technologies Used
- **AWS Services**: Route 53, WAF, CloudFront, API Gateway, Lambda, S3, DynamoDB, SNS, SQS, Rekognition, MediaConvert, CloudWatch, IAM
- **Frontend & Backend Integration**: Implemented using a serverless architecture to enable seamless scalability and performance.

## Future Improvements
- **Caching Layer for Metadata**: Adding a caching layer like ElastiCache could improve metadata retrieval times.
- **Enhanced Processing Capabilities**: Support additional media types and more advanced processing options.
- **User Authentication**: Incorporate a user authentication layer using AWS Cognito for a personalized user experience.

## Summary
This project provided valuable insights into designing and implementing a scalable, serverless cloud architecture. We learned to leverage AWS managed services to optimize performance, manage asynchronous tasks, and ensure secure media processing. This project equipped us with practical knowledge of cloud architecture, teamwork, and real-world problem-solving.
