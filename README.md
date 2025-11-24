 Project Assignment

In this assignment, I have implemented the basic functionality that was given in the requirements.
This project includes:
- Implemented the required features
- Organized the code in separate files
- Added basic validation and error handling
- Made the project ready to submit through GitHub

If any changes or improvements are needed, I can update it.
This is the final version I have completed.
--------------------------------------------------------+-------------------------------------------------+------------------------------------------------------+------------------------------------------------
 Resume Parser – Complete Flow Explanation

This project parses a resume from a given URL and extracts important information like name, email, phone, skills, experience, and education. Below is the exact flow I followed while building it.

 1. How I Planned the Flow

The first thing I considered was that the resume will come through a URL. My first thought was that the file might need to be downloaded. After checking different approaches, I realized that I do not need to download the file. I only need the data, not the actual file. So it was better to load the resume directly into a buffer.

Once the buffer was received, the next step was to find out the file type, because PDF and DOCX have different parsing methods. I detected the file type using the content-type from the response.

After identifying the format, I selected the correct parser:
- If it was a PDF, I used the PDF parsing library.
- If it was a DOCX file, I used the DOCX parsing library (like mammoth).

Then I passed the buffer to the parser to extract the raw text from the resume.

After getting the text, I extracted the main details such as name, email, phone number, skills, education, and work experience. Finally, I converted everything into a clean JSON format so it can be used easily by the frontend.

 2. Detailed Flow (Interview Explanation)

If I explain the flow in detail, step by step, this is how I thought about it:

1. The resume will come from a URL, so I first checked how to fetch it.
2. I initially thought that the resume must be downloaded, but then I found that I only need the data, not the file. So downloading was unnecessary. Loading it into a buffer was enough.
3. After getting the buffer, the next question was to identify the file type. PDF and DOCX parsing works differently, so knowing the type was important.
4. Once I detected the format, I selected the correct parser based on the type.
5. I passed the buffer to the parser and extracted the raw text.
6. Raw text is unstructured, so I extracted the important fields like name, email, phone, skills, education, and experience.
7. After extraction, I formatted everything into a clean JSON structure so that it can be used easily on the frontend.

This is the complete thought process and the full flow of how the resume parsing works from start to finish.
