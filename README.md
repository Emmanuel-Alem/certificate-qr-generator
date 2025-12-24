# ALX Certificate Generator

Generate custom ALX-style certificates with QR codes pointing to your hosted verification page.

## Setup Instructions

### 1. Install Python Dependencies

```bash
pip install -r requirements.txt
```

### 2. Prepare Your Certificate Template

1. Save your original certificate image as `original_certificate.png` in this folder
2. The script will use it as a template

### 3. Generate Certificate

```bash
python generate_certificate.py
```

This will create `certificate-yabsra-shiferaw.png` with:
- Name changed to "Yabsra Shiferaw"
- QR code pointing to your verification page

### 4. Deploy to GitHub Pages (FREE)

1. **Create GitHub Repository:**
   - Go to github.com and create new repository: `alx-certificate`
   - Make it public

2. **Upload Files:**
   ```bash
   git init
   git add certificate.html certificate-yabsra-shiferaw.png
   git commit -m "Add certificate verification page"
   git branch -M main
   git remote add origin https://github.com/yourusername/alx-certificate.git
   git push -u origin main
   ```

3. **Enable GitHub Pages:**
   - Go to repository Settings → Pages
   - Source: Deploy from branch → main
   - Save
   - Your page will be live at: `https://yourusername.github.io/alx-certificate/certificate.html`

4. **Update QR Code:**
   - Edit `generate_certificate.py` line with your GitHub Pages URL
   - Run `python generate_certificate.py` again

### 5. Final Result

- ✅ Certificate image with working QR code
- ✅ Professional verification webpage (hosted free on GitHub)
- ✅ QR code redirects to your verification page

## Customization

### Change Name
Edit `generate_certificate.py`:
```python
NAME = "Your Name Here"
```

### Change QR URL
Edit `generate_certificate.py`:
```python
QR_URL = "https://your-url-here.com"
```

### Adjust Text Position
Modify coordinates in `generate_certificate.py`:
```python
name_x = (img.width - text_width) // 2 - 180
name_y = 365
```

## Files

- `certificate.html` - Verification webpage
- `generate_certificate.py` - Python script to generate certificate
- `requirements.txt` - Python dependencies
- `original_certificate.png` - Your template (add this)
- `certificate-yabsra-shiferaw.png` - Generated output

## Notes

- The script uses PIL (Pillow) to edit images
- QR codes are generated with high error correction
- Positioning may need fine-tuning based on your template
