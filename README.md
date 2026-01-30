# Resume Generator

A Python tool that generates professional Word documents (.docx) from resume data stored in JSON format.

## Features

- Generate professional resumes from JSON data
- Customizable formatting and styling
- Automatic filename generation based on name and company
- Version control for multiple resume iterations
- Clean, organized output folder

## Project Structure

```
Resume_generator/
├── resume-generator.py      # Main script
├── my_resume_data.json      # Your resume data (edit this)
├── .gitignore              # Git configuration
├── README.md               # This file
├── output/                 # Generated resumes
└── .venv/                  # Virtual environment
```

## Setup

1. Clone the repository:
```bash
git clone <your-repo-url>
cd Resume_generator
```

2. Create and activate virtual environment:
```bash
python -m venv .venv
.venv\Scripts\activate  # Windows
source .venv/bin/activate  # macOS/Linux
```

3. Install dependencies:
```bash
pip install python-docx
```

## Usage

1. Edit `my_resume_data.json` with your resume information
2. Update the `company_name` field for the company you're applying to
3. Run the script:
```bash
python resume-generator.py my_resume_data.json
```

4. Your resume will be generated in the `output/` folder as:
```
Javeed_mohammad_Resume_CompanyName.docx
```

## JSON Structure

```json
{
  "personal": {
    "name": "Your Name",
    "email": "your.email@example.com",
    "phone": "(XXX) XXX-XXXX",
    "location": "City, State",
    "company_name": "Company_Name"
  },
  "summary": [...],
  "experience": [...],
  "projects": [...],
  "skills": [...],
  "education": [...]
}
```

## Customization

Edit the styling configuration at the top of `resume-generator.py`:
- Margins
- Font sizes
- Section spacing
- Colors

## Requirements

- Python 3.6+
- python-docx

## License

MIT
