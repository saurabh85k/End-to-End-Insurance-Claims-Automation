# End-to-End Insurance Claims Automation

A web application that automates insurance claim processing. A user uploads a claim document, the system extracts text using OCR, parses key fields, validates them against policy data, and marks the claim as Approve, Reject or Flag with a reason.

## Tech Stack
- Backend: Java, Spring Boot, Spring Data JPA
- Database: PostgreSQL
- OCR service: Python (FastAPI), Tesseract, PyMuPDF
- Frontend: React

## How it works
1. Claim document (PDF/image) is uploaded through the REST API.
2. The backend sends it to the Python OCR service and receives the extracted text.
3. Key fields (policy number, name, amount, date) are parsed from the text.
4. Rule-based checks compare them with policy data stored in PostgreSQL.
5. The claim is saved with a status (Approve / Reject / Flag) and a reason.

## Future Scope
- LLM-generated explanations for each decision
- Fraud detection
- Authentication with Spring Security and JWT
