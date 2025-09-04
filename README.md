# DocAnalyzer & Terminology Manager

A powerful web-based tool for technical writers to analyze documentation, extract terminology, and ensure glossary compliance. Built with Julia and Genie Framework for high-performance text processing.

## Features

- **Automated Terminology Extraction**: Identifies potential technical terms using NLP algorithms
- **Glossary Compliance Checking**: Verifies terminology usage against approved glossaries
- **Readability Analysis**: Calculates readability scores and metrics
- **Web-based Interface**: Easy-to-use GUI accessible from any browser

## Quick Start

### Prerequisites

- Julia 1.9 or higher

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/DocAnalyzer.git
cd DocAnalyzer
```
2. **Install dependencies**
```julia
using Pkg
Pkg.activate(".")
Pkg.instantiate()
```
3. **Run the application**
```bash
julia bin/server.jl
```
4. **Open your browser**. Navigate to `http://localhost:8000`

## Usage

- Upload a document (TXT or MD format)
- Optional: Upload a CSV glossary file
- Click Analyze to process your document
- Review results: terminology suggestions and readability metrics

## Glossary Format

Create a CSV file with terms:

```csv
term,definition
API,Application Programming Interface
GUI,Graphical User Interface
```

## Project Structure

```text
DocAnalyzer/
├── src/
│   ├── analysis/
│   │   ├── terminology.jl     # Terminology extraction logic
│   │   ├── readability.jl     # Readability metrics
│   │   └── text_processing.jl # Core text processing
│   └── routes.jl              # URL routing
├── app/
│   └── resources/
│       └── documents/         # MVC components
├── data/                      # Sample data and glossaries
├── public/                    # Static assets
└── bin/
    └── server.jl              # Application entry point
```

---

## Running Tests

```julia
julia> using Pkg
julia> Pkg.test("DocAnalyzer")
```