# 📄 AI Resume Generator

A Python utility that converts structured **JSON resume data** into a clean, professional, **ATS-friendly Word document (`.docx`)**. Store your resume as data once, then generate tailored versions in seconds.

---

## ⚡ Quick Start

1. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

2. **Edit your resume data**
   - Update `my_resume_data.json`

3. **Generate your resume**
   ```bash
   python resume-generator.py my_resume_data.json
   ```

---

## 🚀 Key Features

- **JSON → DOCX:** Keep content in JSON, let the script handle Word formatting.
- **JSON-driven generation:** Generate resumes directly from structured JSON inputs.
- **Sample resume generation:** Run without a JSON file to generate sample resumes (if supported by the script).
- **Interactive mode:** Build your resume step-by-step via terminal prompts using `--interactive`.
- **Easy styling edits:** Adjust margins, fonts, and spacing from one configuration section.
- **Dynamic filenames:** Generates professional filenames using your name and target company.
- **Smart versioning:** Prevents overwrites by appending a counter (e.g., `_1`, `_2`) if a file already exists.
- **A4 optimized:** A4 dimensions with configurable margins and fonts.

---

## 📁 Project Structure

```text
Resume_generator/
├── resume-generator.py     # Core engine + styling configuration
├── my_resume_data.json     # Your resume data (edit this!)
├── requirements.txt        # Python dependencies
├── .gitignore              # Git exclusions
├── README.md               # Documentation
├── output/                 # Generated resumes output
└── .venv/                  # Virtual environment (local)
```

---

## ✅ Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/javid679/Resume_generator.git
   cd Resume_generator
   ```

2. **(Recommended) Create and activate a virtual environment**

   **Windows**
   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   ```

   **macOS / Linux**
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

---

## 💻 Usage

### Option 1: Load from JSON (Recommended)

Edit `my_resume_data.json`, then run:

```bash
python resume-generator.py my_resume_data.json
```

### Option 2: Interactive Mode

Generate a resume through a guided terminal workflow:

```bash
python resume-generator.py --interactive
```

### Option 3: Sample Generation

If your script supports it, running without arguments generates sample output:

```bash
python resume-generator.py
```

---

## 📄 Filename Generation Logic

The script generates a standardized filename using your resume data.

**Format**
- `Firstname_Lastname_Resume_CompanyName.docx`

**Example**
- `Javeed_Mohammad_Resume_Google.docx`

If the filename already exists, the script may append a counter:
- `Javeed_Mohammad_Resume_Google_1.docx`

---

## 📊 JSON Data Format (Example)

Below is an example structure. Your script may support more fields; keep the keys aligned with what `resume-generator.py` expects.

```json
{
  "personal": {
    "name": "Javeed Mohammad",
    "email": "javeed@example.com",
    "phone": "(555) 123-4567",
    "location": "City, State",
    "company_name": "Google"
  },
  "summary": "Results-driven developer...",
  "experience": [],
  "skills": [],
  "education": []
}
```

---

## 🎨 Customization & Styling

You can customize document appearance by editing the constants near the top of `resume-generator.py`, such as:

- `MARGIN_TOP`, `MARGIN_BOTTOM`, `MARGIN_LEFT`, `MARGIN_RIGHT`
- `DEFAULT_FONT`
- Section title font sizes (e.g., EXPERIENCE, EDUCATION)
- Optional table border settings (if included)

---

## 📝 License

This project is licensed under the **MIT License**.

Developed by **Javeed Mohammad**.
