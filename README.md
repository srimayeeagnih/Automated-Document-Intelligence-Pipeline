# Automated-Document-Intelligence-Pipeline

**Overview**
An automated document processing system that classifies legal documents and extracts key metadata using pattern-based rules and LLM-assisted OCR analysis.
Features
Document Classification
Automatically categorizes documents into four types:

Contract - Legal agreements and contracts
Invoice - Billing documents and invoices
Email - Email correspondence
Other - Meeting minutes, memos, and miscellaneous documents

Metadata Extraction
Extracts critical information including:

Client names
Vendor information
Currency details
Important dates

**Technology Stack**

Pattern Matching: Regex-based extraction for structured documents
LLM Integration: Ollama for OCR analysis of scanned PDFs
Batch Processing: Processes entire folders using glob pattern matching
Output: Consolidated DataFrame for all processed documents

**How It Works**
1. Pattern-Based Classification
The system leverages firm-wide templates common in legal firms for efficient classification. Documents are analyzed using rule-based patterns to determine their type.
2. Metadata Extraction
The system searches for specific phrases to identify subjects:

"Thanks for tipping {subject_name}"
"Billing to {subject_name}"
Other contextual patterns for dates, currency, and vendor information

3. OCR Processing
For scanned PDF files, the system uses Ollama LLM to:

Perform optical character recognition
Extract metadata from image-based documents

4. Batch Processing
Processes all matching files in a directory using glob patterns and outputs results to a single DataFrame for easy analysis.
