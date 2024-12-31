# TaskPlanner_AI
# Task Planner Generator from Meeting Recordings

This application automatically generates task planners from meeting recordings by extracting key details such as tasks, deadlines, assignees. The solution leverages AWS services like Amazon Transcribe, Lambda, DynamoDB, S3, EC2 and integrates OpenAI's NLP for task extraction and Reactjs for UI design. It streamlines task management and improves productivity by converting meeting recordings into actionable tasks.

## Features

- **Automatic Task Extraction**: Extract tasks, assignees, deadlines, and other key details from meeting recordings.
- **Real-Time Transcription**: Uses Amazon Transcribe to convert audio to text.
- **AI-Powered NLP**: OpenAI's language models and NLP techniques are used to extract task details (task names, assignees, deadlines) from transcribed text.
- **Dynamic Task Planner**: The extracted data is organized into a structured task planner for easy management and tracking.
- **Cloud Storage with S3**: Meeting recordings are stored securely on Amazon S3.
- **Serverless Architecture**: AWS Lambda functions trigger the transcription and task extraction processes.
- **Database Integration with DynamoDB**: Task data is stored and organized in Amazon DynamoDB for fast retrieval and updates.

## Architecture Overview

The application uses a serverless architecture that leverages multiple AWS services, making it scalable, cost-efficient, and secure.

### 1. **Amazon Transcribe**
   - **Amazon Transcribe** is used to convert meeting audio recordings into text. The transcription process is triggered when a recording is uploaded to an S3 bucket.

### 2. **AWS Lambda**
   - **AWS Lambda** is used to trigger processes when a new recording is uploaded. It:
     - Invokes Amazon Transcribe to transcribe the audio.
     - Calls another Lambda function to process the transcribed text and extract actionable task details using NLP.

### 3. **OpenAI & NLP**
   - OpenAI’s language models and NLP techniques analyze the transcribed text. It identifies tasks, assignees, and deadlines within the meeting content and filters out unnecessary information.

### 4. **Amazon S3**
   - Meeting recordings are securely stored in **Amazon S3**. The recordings are accessible for transcription and are retained for future reference or processing.

### 5. **Amazon DynamoDB**
   - Task details (task names, assignees, deadlines) are stored in **Amazon DynamoDB**, allowing for fast, scalable, and flexible storage of task data.

### 6. **Task Planner Generation**
   - The extracted data is organized into a structured task planner, making it easy to track tasks, deadlines, and assignees. The planner is available to the user for viewing and management.

## Workflow

1. **Upload Meeting Recording**: A user uploads a meeting recording to an S3 bucket.
2. **Trigger Transcription**: The upload event triggers an AWS Lambda function that invokes **Amazon Transcribe** to convert the audio to text.
3. **Data Extraction**: The transcribed text is passed through NLP models (via OpenAI) to extract relevant task details such as task description, assignees, and deadlines.
4. **Task Data Storage**: The extracted task data is stored in **Amazon DynamoDB**.
5. **Task Planner Generation**: A structured task planner is generated and made available to the user.

## Technologies Used

- **Amazon Web Services (AWS)**:
  - **Amazon S3**: Storage for meeting recordings.
  - **Amazon Transcribe**: Converts audio recordings into text.
  - **AWS Lambda**: Serverless compute for processing and triggering tasks.
  - **Amazon DynamoDB**: NoSQL database for storing task data.
- **OpenAI API**: Language models for NLP processing and task extraction.
- **Natural Language Processing (NLP)**: Techniques used to process and extract structured information from the transcribed text.

## Benefits

- **Automated Task Generation**: Automatically generate actionable tasks and task planners from meeting recordings.
- **Increased Efficiency**: Saves time by eliminating the need for manual note-taking and task tracking.
- **Scalable and Cost-Effective**: Built on AWS, the application scales seamlessly and reduces overhead by utilizing serverless architecture.
- **AI-Enhanced**: OpenAI’s language models and NLP enhance the accuracy of task extraction.
- **Secure**: Data is stored securely using AWS services like S3 and DynamoDB.

## How It Works

1. **Upload a Recording**: Upload your meeting recording to the designated S3 bucket.
2. **Task Extraction**: The app automatically processes the recording through Amazon Transcribe, followed by NLP-based task extraction using OpenAI’s language models.
3. **Task Planner**: A task planner with the extracted data (task descriptions, assignees, and deadlines) is generated and made available for review and action.

## Getting Started

### Prerequisites

- AWS Account with access to the following services:
  - Amazon S3
  - AWS Lambda
  - Amazon Transcribe
  - Amazon DynamoDB
  - OpenAI API Key (for NLP and text processing)

### Installation

1. Clone this repository to your local machine.
2. Set up your AWS environment (using AWS CLI or through the AWS Management Console).
3. Configure the necessary AWS services (S3, Lambda, Transcribe, DynamoDB).
4. Deploy the Lambda functions for transcription and task extraction.
5. Integrate the OpenAI API for NLP-based extraction.
6. Upload a recording to the configured S3 bucket to see the app in action.

## Conclusion

This application automates the tedious task of generating task planners from meeting recordings, saving valuable time and ensuring that no important task or deadline is overlooked. By integrating AWS services and OpenAI’s NLP, this solution provides an intelligent, scalable, and secure approach to managing tasks in a professional environment.


## Developers

Ambar Shrivastava
Sai Charan Reddy Vangala
Santhosh Ravula
Manasa Gunreddy
