# MCQ Creator Application with LangChain

## Project Overview

This project implements an MCQ (Multiple Choice Question) generation application using **LangChain** and **OpenAI**'s language models. The application allows users to upload a PDF or text file and generate MCQs based on the content of the file. Users can customize the number of MCQs, the subject, and the complexity level of the questions.

The core functionality is implemented in the `app.py` file, which uses Streamlit to create the user interface, and interacts with LangChain to process the uploaded file, generate MCQs, and display the results.

## Features

- **File Upload**: Users can upload PDF or text files from which MCQs will be generated.
- **Customizable Inputs**: 
  - Number of MCQs (between 3 and 50).
  - Subject for the MCQs.
  - Complexity level (e.g., "Simple").
- **MCQ Generation**: The app uses OpenAI’s API via LangChain to generate MCQs based on the content of the uploaded file.
- **Result Display**: The generated MCQs are displayed in a table format, along with a review section for feedback.

## How It Works

### 1. User Input
The user uploads a PDF or text file and specifies the number of MCQs, subject, and complexity level. 

### 2. Text Extraction
The content of the uploaded file is read using the `read_file()` function from the `utils.py` file.

### 3. MCQ Generation
The extracted text is sent to `generate_evaluate_chain()` in `mcqgenerator.py`, which interacts with OpenAI's API to generate the MCQs based on the user-specified parameters.

### 4. Response Handling
Once the MCQs are generated, they are displayed in a table format. Additionally, a review of the generated MCQs is shown for the user's feedback.
