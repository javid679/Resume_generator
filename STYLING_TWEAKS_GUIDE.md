# Resume Generator - Styling Tweaks Guide

## Quick Reference for Customizing Resume Appearance

All styling parameters are located at the **TOP of the `resume-generator.py` file** under the section:
```
# ============================================================================
# STYLING CONFIGURATION - Tweak these values to change document appearance
# ============================================================================
```

---

## Key Styling Parameters

### 1. **MARGINS** (in inches)
```python
MARGIN_TOP = 0.5        # Top margin
MARGIN_BOTTOM = 0.5     # Bottom margin
MARGIN_LEFT = 0.5       # Left margin (affects left edge)
MARGIN_RIGHT = 0.5      # Right margin (affects right edge)
```
**Tweak:** Increase to add more white space around edges, decrease to fit more content.

---

### 2. **PAPER SIZE** (A4 by default)
```python
PAPER_WIDTH = 8.27      # Width in inches
PAPER_HEIGHT = 11.69    # Height in inches
```
**Tweak:** Change to Letter (8.5" × 11") or other sizes if needed.

---

### 3. **DEFAULT FONT SETTINGS**
```python
DEFAULT_FONT = 'Times New Roman'  # Font family for entire document
DEFAULT_FONT_SIZE = 12            # Body text size (in points)
```
**Options for DEFAULT_FONT:**
- 'Times New Roman' (current)
- 'Calibri'
- 'Arial'
- 'Garamond'

---

### 4. **HEADER STYLING** (Name and Contact Info)
```python
HEADER_NAME_SIZE = 22             # Name font size in points
HEADER_NAME_BOLD = True           # Make name bold (True/False)
HEADER_CONTACT_SIZE = 11          # Contact info font size
HEADER_CONTACT_SPACE_BEFORE = 3   # Space above contact line
HEADER_CONTACT_SPACE_AFTER = 12   # Space below contact line
```
**Tweaks:**
- Increase `HEADER_NAME_SIZE` to make name bigger
- Increase `HEADER_CONTACT_SPACE_AFTER` to add more space below contact info

---

### 5. **SECTION TITLE STYLING**
```python
SECTION_TITLE_SIZE = 14           # Title font size (PROFESSIONAL SUMMARY, etc.)
SECTION_TITLE_BOLD = True         # Make titles bold
SECTION_TITLE_SPACE_BEFORE = 6    # Space BEFORE section title (YOU SPECIFIED 6pts)
SECTION_TITLE_SPACE_AFTER = 6     # Space AFTER section title
SECTION_TITLE_BORDER_COLOR = '000000'  # Border color (000000 = black)
```
**Tweaks:**
- Increase `SECTION_TITLE_SIZE` to make section titles bigger
- Modify `SECTION_TITLE_SPACE_BEFORE` to adjust gap before titles
- Change `SECTION_TITLE_BORDER_COLOR` (e.g., '0070C0' for blue)

---

### 6. **CONTENT SPACING**
```python
CONTENT_SPACE_AFTER = 6           # Space after job/project titles
BULLET_ITEM_SPACE = 0             # Space after each bullet point
```
**Tweaks:**
- Increase `CONTENT_SPACE_AFTER` to add more space between job entries
- Increase `BULLET_ITEM_SPACE` to spread out bullet points more

---

### 7. **ALIGNMENT**
```python
DEFAULT_ALIGNMENT = WD_ALIGN_PARAGRAPH.JUSTIFY  # Main body text alignment
HEADER_ALIGNMENT = WD_ALIGN_PARAGRAPH.CENTER    # Header alignment
```
**Options:**
- `WD_ALIGN_PARAGRAPH.JUSTIFY` - Text justified to both margins
- `WD_ALIGN_PARAGRAPH.LEFT` - Left-aligned
- `WD_ALIGN_PARAGRAPH.CENTER` - Centered
- `WD_ALIGN_PARAGRAPH.RIGHT` - Right-aligned

---

## Font Size Quick Reference

| Element | Current Size | Location in Code |
|---------|--------------|-----------------|
| Name | 22pt | `HEADER_NAME_SIZE` |
| Contact Info | 11pt | `HEADER_CONTACT_SIZE` |
| Section Titles | 14pt | `SECTION_TITLE_SIZE` |
| Body Text | 11pt | `DEFAULT_FONT_SIZE` |
| Job Titles | 11pt | Search for `Pt(11)` in `add_section()` |
| Bullet Points | 11pt | Search for `Pt(11)` in `add_section()` |

---

## Spacing Values Reference

| Element | Current Value | Purpose |
|---------|--------------|---------|
| Margins | 0.5" | Space around document edges |
| Before Titles | 6pt | Gap before "PROFESSIONAL SUMMARY" etc. |
| After Titles | 6pt | Gap after title line |
| After Contact | 12pt | Space below contact info |
| After Job Title | 6pt | Space between job title and bullet points |
| Between Bullets | 0pt | Space between bullet points |

---

## Common Customization Examples

### Make Everything Look More Spacious
```python
SECTION_TITLE_SPACE_BEFORE = 12  # Increase from 6 to 12
SECTION_TITLE_SPACE_AFTER = 12   # Increase from 6 to 12
CONTENT_SPACE_AFTER = 12         # Increase from 6 to 12
BULLET_ITEM_SPACE = 3            # Increase from 0 to 3
```

### Make Everything More Compact
```python
SECTION_TITLE_SPACE_BEFORE = 3   # Decrease from 6 to 3
SECTION_TITLE_SPACE_AFTER = 3    # Decrease from 6 to 3
CONTENT_SPACE_AFTER = 3          # Decrease from 6 to 3
```

### Larger Fonts
```python
DEFAULT_FONT_SIZE = 12           # Increase from 11
SECTION_TITLE_SIZE = 16          # Increase from 14
HEADER_NAME_SIZE = 24            # Increase from 22
```

### Different Font
```python
DEFAULT_FONT = 'Calibri'  # Change from 'Times New Roman'
```

---

## Where to Find More Tweaks in Code

Inside the methods, look for `# TWEAK:` comments:
- `add_section_title()` - Border styling
- `add_header()` - Name and contact formatting
- `add_section()` - Job titles, descriptions, bullet points
- `add_skills_section()` - Category/content split
- `add_education_table()` - School and degree formatting

---

## Tips for Adjusting

1. **Make small changes** - Change one value at a time and regenerate to see the effect
2. **Backup your files** - Keep a copy of your template before major changes
3. **Test with sample data** - Use the template first before finalizing
4. **Print and check** - PDF or print to verify spacing and alignment
5. **Use consistent spacing** - Keep similar spacing values for similar elements

---

## Regenerating After Changes

After modifying the styling parameters:
```powershell
# Test with template
python resume-generator.py resume_template.json

# Or use interactive mode
python resume-generator.py --interactive
```

The generated Word document will reflect your styling changes!
