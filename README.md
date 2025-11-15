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

**First, set up the domain in GitHub:**
1. In the same **Pages** settings, scroll to **Custom domain**
2. Enter `equipindia.in` and click **Save**
3. GitHub will create a `CNAME` file in your repository
4. **Note your GitHub Pages URL** - it will be something like `YOUR_USERNAME.github.io` (you'll need this for GoDaddy)

**Then, configure DNS in GoDaddy:**

#### GoDaddy DNS Configuration (Step-by-Step)

**What is DNS?** Think of it as a phone book that tells the internet where to find your website. When someone types `equipindia.in`, DNS points them to GitHub Pages where your site is hosted.

**Steps in GoDaddy Dashboard:**

1. **Log in to GoDaddy**
   - Go to [godaddy.com](https://godaddy.com) and sign in
   - Click on your account/name in the top right
   - Select "My Products"

2. **Find Your Domain**
   - Look for `equipindia.in` in your list of domains
   - Click on the **DNS** button (or "Manage DNS") next to your domain

3. **Add A Records (for equipindia.in)**
   - Scroll down to the **Records** section
   - You'll see a table with existing records
   - Click the **Add** button (usually at the top right of the records table)
   - Select **A** from the Type dropdown
   - For **Name/Host**: Enter `@` (this means your main domain)
   - For **Value/Points to**: Enter `185.199.108.153`
   - Leave **TTL** as default (usually 600 seconds or 1 hour)
   - Click **Save**
   
   **Repeat this 3 more times** to add the other 3 A records:
   - Second A record: Name `@`, Value `185.199.109.153`
   - Third A record: Name `@`, Value `185.199.110.153`
   - Fourth A record: Name `@`, Value `185.199.111.153`

4. **Update CNAME Record (for www.equipindia.in) - Optional but Recommended**
   
   **IMPORTANT:** If you already have a CNAME record with Name `www`, you need to **UPDATE** it, not create a new one!
   
   - Look for an existing CNAME record with Name `www` in your records table
   - If it exists and points to `equipindia.in` or something else, click the **three dots (...)** or **Edit** button next to it
   - Change the **Value/Points to** to: `cliffordrichiefam-commits.github.io` (just the domain, NO path like `/equipindia.in`)
   - Click **Save**
   
   **If you DON'T have a www CNAME record yet:**
   - Click the **Add** button
   - Select **CNAME** from the Type dropdown
   - For **Name/Host**: Enter `www`
   - For **Value/Points to**: Enter `cliffordrichiefam-commits.github.io` (just the domain, NO path)
   - Leave **TTL** as default
   - Click **Save**

5. **Remove Conflicting Records (if any)**
   - If you see any existing A records pointing to other IP addresses (like GoDaddy parking pages), you can delete them
   - Look for A records with Name `@` that have different values than the GitHub IPs above
   - Click the three dots (...) next to them and select Delete
   - **Note:** You can only have ONE CNAME record with the name `www`, so make sure you updated the existing one rather than trying to add a duplicate

**Important Notes:**
- DNS changes can take 1-48 hours to propagate (usually 1-2 hours)
- You can check if it's working by visiting `equipindia.in` in your browser
- Once DNS is working, go back to GitHub Pages settings and check "Enforce HTTPS" (this option appears after DNS is properly configured)

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

