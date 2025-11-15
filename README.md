# EquipIndia - Coming Soon Website

A simple, elegant "Coming Soon" static website for EquipIndia charity organization.

## Features

- Clean, modern design suitable for a charity organization
- Responsive layout that works on all devices
- Hero section with "Coming Soon" message
- Mission statement section
- Image gallery section
- Smooth animations and transitions
- Easy to customize

## Setup Instructions

### 1. Adding Your Images

1. Place your images in the `images/` folder
2. Update the image sources in `index.html`:
   - Find the gallery section (around line 50)
   - Replace `images/image1.jpg`, `images/image2.jpg`, `images/image3.jpg` with your actual image filenames
   - Update the `alt` attributes with descriptive text for accessibility

Example:
```html
<img src="images/your-image-1.jpg" alt="Description of your image" class="gallery-image" loading="lazy">
```

### 2. Customizing the Mission Statement

1. Open `index.html`
2. Find the mission section (around line 30)
3. Edit the text inside the `<p class="mission-text">` tags with your actual mission statement

### 3. Customizing Colors

1. Open `styles.css`
2. Find the `:root` section at the top (around line 2)
3. Modify the CSS variables to match your brand colors:
   - `--primary-color`: Main brand color
   - `--secondary-color`: Secondary brand color
   - `--accent-color`: Accent/highlight color

### 4. Updating Contact Information

1. Open `index.html`
2. Find the footer section (around line 70)
3. Update the email address in the contact link

## GitHub Pages Deployment

### Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and create a new repository
2. Name it (e.g., `equipindia-website` or `equipindia.in`)
3. Make it public (required for free GitHub Pages)
4. Don't initialize with README (since you already have files)

### Step 2: Push Your Code

```bash
# Initialize git repository (if not already done)
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit: Coming soon page"

# Add your GitHub repository as remote
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on **Settings** tab
3. Scroll down to **Pages** section (in the left sidebar)
4. Under **Source**, select **Deploy from a branch**
5. Choose **main** branch and **/ (root)** folder
6. Click **Save**
7. Your site will be available at: `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`

### Step 4: Connect Your Custom Domain (equipindia.in)

1. In the same **Pages** settings, scroll to **Custom domain**
2. Enter `equipindia.in` and click **Save**
3. GitHub will create a `CNAME` file in your repository

#### DNS Configuration

You need to configure DNS records with your domain registrar:

**Option 1: Apex Domain (equipindia.in)**
- Add these A records:
  - `185.199.108.153`
  - `185.199.109.153`
  - `185.199.110.153`
  - `185.199.111.153`

**Option 2: Subdomain (www.equipindia.in)**
- Add a CNAME record:
  - Name: `www`
  - Value: `YOUR_USERNAME.github.io`

**Option 3: Both (Recommended)**
- Add the A records for apex domain
- Add CNAME for www subdomain
- In GitHub Pages settings, check "Enforce HTTPS" (available after DNS propagates)

### Step 5: Verify

1. Wait for DNS propagation (can take up to 48 hours, usually much faster)
2. Visit `http://equipindia.in` (or `https://equipindia.in` once HTTPS is enabled)
3. Your site should be live!

## File Structure

```
equipindia.in/
├── index.html          # Main HTML file
├── styles.css          # Stylesheet
├── script.js           # JavaScript for interactions
├── images/             # Image directory (add your images here)
├── .gitignore          # Git ignore file
└── README.md           # This file
```

## Customization Tips

- **Fonts**: To change fonts, update the `font-family` in `styles.css` (body selector)
- **Spacing**: Adjust padding values in section styles (`.mission`, `.gallery`)
- **Gallery Items**: Add or remove gallery items by copying the `.gallery-item` div structure
- **Hero Background**: Modify the gradient in `.hero` selector in `styles.css`

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## License

This project is for EquipIndia charity organization.

## Support

For questions or issues, please contact: info@equipindia.in

