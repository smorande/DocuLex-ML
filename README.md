# Legal Contract Automation System

**autocon.py**

This script automates the process of generating, reviewing, and finalizing legal contracts using AI technology. Here's what you need to know:

## Overview

- **Purpose**: To streamline the creation of legal contracts by automating template selection, content population, risk assessment, and finalization.
- **Technology**: Utilizes Streamlit for the user interface, OpenAI's API for AI-driven tasks, and Python libraries for document processing.

## Features

- **Template Generation**: Automatically generates contract templates based on the type of business proposal provided.
- **Template Population**: Fills in templates with relevant information from the proposal.
- **Risk and Compliance Analysis**: Performs a detailed risk and compliance check on the generated contract.
- **Contract Finalization**: Reviews and finalizes the contract for consistency and compliance.
- **Document Export**: Saves the final contract in both Word and PDF formats.

## Setup Instructions

1. **Environment Variables**: Ensure you have set the `OPENAI_API_KEY` in your environment variables.
   ```bash
   export OPENAI_API_KEY=your_api_key_here
   ```

2. **Dependencies**: Install the required Python packages:
   ```bash
   pip install streamlit PyPDF2 reportlab python-docx openai
   ```

3. **Run the Script**: 
   ```bash
   streamlit run autocon.py
   ```

## Usage

- **Input**: Users can input their business proposal either as text or by uploading a file (PDF or TXT).
- **Processing**: Click the "Process Proposal" button to generate a contract based on the input.
- **Review**: Review and edit the generated contract, run additional analysis if needed.
- **Download**: Download the final contract in Word or PDF format.

## Key Functions

- **`load_templates()`**: Loads contract templates from a specified directory or generates a default template if none exist.
- **`generate_template(template_type)`**: Uses OpenAI to generate a new contract template based on the type specified.
- **`extract_text_from_pdf(pdf_file)`**: Extracts text from PDF files for processing.
- **`classify_template(text)`**: Classifies the type of contract needed based on the proposal text.
- **`populate_template(template, proposal)`**: Fills in the template with details from the proposal.
- **`risk_compliance_check(contract)`**: Analyzes the contract for potential risks and compliance issues.
- **`generate_final_contract(contract)`**: Finalizes the contract ensuring consistency and compliance.
- **`save_as_word(contract)`** and **`save_as_pdf(contract)`**: Saves the contract in Word and PDF formats respectively.

## Limitations

- **API Dependency**: The script relies on OpenAI's API, which requires an API key and may have usage limits or costs associated.
- **Accuracy**: The quality of the generated contract depends on the accuracy of the AI model and the clarity of the input proposal.

## Contributing

Contributions are welcome! Please fork the repository and submit pull requests for any enhancements or bug fixes.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
 
