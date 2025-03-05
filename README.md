# Sensitive-Document-Classifier
 Sensitive Document Classifier This repository contains an AI-powered classifier that determines whether a file is Sensitive (Y) or Non-Sensitive (N) using metadata—without accessing document content.   Features    Classifies files based on filename, path, extension, size, and timestamps  
# Sensitive Document Classifier

## Project Description
The Sensitive Document Classifier is an AI-powered tool designed to determine whether a file is **Sensitive (Y) or Non-Sensitive (N)** using only metadata—without accessing the document content. It employs Machine Learning (ML), Deep Learning (DL), or Large Language Models (LLMs) for classification and provides a confidence score for each prediction.

## Features
- Classifies files based on filename, path, extension, size, and timestamps.
- Predicts a confidence score for each classification.
- Runs locally without external APIs.
- Works via CLI input or as a deployable API.

## Installation & Setup
### Prerequisites
Ensure you have the following installed:
- **Visual Studio Code (VS Code)**: [Download Here](https://code.visualstudio.com/)
- **Node.js & npm**: [Download Here](https://nodejs.org/)

### Install Required Extensions in VS Code
1. Open VS Code and go to Extensions (`Ctrl+Shift+X`).
2. Install the following extensions:
   - ESLint
   - Prettier - Code formatter
   - Tailwind CSS IntelliSense
   - ES7+ React/Redux snippets
   - JavaScript and TypeScript Nightly
   - Error Lens
   - Path Intellisense

### Setting Up the Project
1. Clone the repository:
   ```sh
   git clone https://github.com/your-repo/sensitive-document-classifier.git
   cd sensitive-document-classifier
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Install additional UI components:
   ```sh
   npx shadcn@latest init
   npx shadcn@latest add button card tabs badge input label progress separator toast
   ```
4. Start the development server:
   ```sh
   npm run dev
   ```
5. Open your browser and go to `http://localhost:3000`.

## Modules & Functionality
- **Document Classification Interface**: Allows users to input file metadata for classification.
- **Model Training Section**: Enables training of AI models on labeled metadata.
- **Results Dashboard**: Displays classification results with confidence scores.
- **User Experience Enhancements**: Includes toast notifications, interactive components, and a responsive design.

## Example Usage
### CLI Input
```sh
python classify.py --file "C:\Users\bank_statement_2024.xlsx"
```
**Output:**
```
File: bank_statement_2024.xlsx
Predicted: Sensitive (Y)
Confidence Score: 92%
```

### API Endpoint
**Request:**
```sh
POST /classify
{
  "filename": "C:\\Users\\passport.pdf",
  "size": 2048,
  "timestamp": "2025-03-05T12:00:00"
}
```
**Response:**
```json
{
  "predicted": "Sensitive",
  "confidence_score": 95
}
```
```
## Troubleshooting
- **Module not found errors**: Run `npm install` again.
- **Server not starting**: Ensure no other process is using port 3000.
- **Styling issues**: Verify Tailwind CSS configuration.

## Next Steps
- Enhance the AI model for better accuracy.
- Implement additional metadata-based classification techniques.
- Extend the API for broader integrations.

By following this guide, you should be able to set up, run, and contribute to the Sensitive Document Classifier project efficiently!

