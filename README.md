# V Team Fitness Hub - Gym Management System

Professional gym membership management website with real-time database sync, admin authentication, and responsive design.

## Features ✨

- **Admin Authentication**: Secure login with Firebase Authentication
- **Member Management**: Add, edit, delete members with real-time updates
- **Analytics Dashboard**: Real-time member statistics
- **Search & Filter**: Search members by name/phone, filter by status
- **WhatsApp Integration**: Send renewal reminders via WhatsApp
- **Responsive Design**: Works perfectly on mobile, tablet, and desktop
- **Dark/Light Theme**: Toggle between themes
- **Real-time Sync**: Changes sync instantly across all devices

## File Structure 📁

```
project/
├── index.html                 # Landing page
├── login.html                 # Admin login page
├── dashboard.html             # Analytics dashboard
├── members.html               # Member management
├── css/
│   ├── styles.css             # Main styles
│   └── responsive.css         # Mobile/tablet responsive styles
├── js/
│   ├── firebase-config.js     # Firebase setup (embedded in HTML)
│   ├── utils.js               # Utility functions
│   ├── auth.js                # Authentication logic
│   ├── members.js             # Member CRUD operations
│   ├── ui.js                  # UI interactions
│   ├── app.js                 # Landing page logic
│   ├── dashboard.js           # Dashboard logic
│   └── members-page.js        # Members page logic
└── README.md                  # This file
```

## Technologies Used 🛠️

- **Frontend**: HTML5, CSS3, Vanilla JavaScript (ES6+)
- **Backend**: Firebase Realtime Database
- **Authentication**: Firebase Authentication
- **Hosting**: GitHub Pages / Cloudflare Pages
- **Deployment**: No build process needed

## Getting Started 🚀

### Prerequisites

- Firebase account (free tier)
- GitHub account (for hosting on GitHub Pages)
- Modern web browser

### Firebase Setup (Already Done!)

Your Firebase configuration is already set up:

```javascript
const firebaseConfig = {
    apiKey: "AIzaSyBD--itijs4RziHUWMdQA3jAvZ9hgNhzBo",
    authDomain: "vteam-fitness.firebaseapp.com",
    databaseURL: "https://vteam-fitness-default-rtdb.asia-southeast1.firebasedatabase.app",
    projectId: "vteam-fitness",
    storageBucket: "vteam-fitness.firebasestorage.app",
    messagingSenderId: "1019346733178",
    appId: "1:1019346733178:web:59d3a64d8dd838aa5c13c3"
};
```

**Admin Credentials:**
- Email: `vteam@vteamfitness.com`
- Password: `Bilal`

### Local Testing 🧪

1. **Download all files** from the project folder
2. **Open `index.html`** in your web browser
3. **Click "Get Started"** to navigate to login
4. **Login with credentials above**
5. **Start managing members!**

### Deploy to GitHub Pages 📤

#### Step 1: Create GitHub Repository

1. Go to https://github.com/new
2. Repository name: `vteam-fitness-hub`
3. Description: `V Team Fitness Hub - Gym Management System`
4. Choose **Public**
5. Click **Create repository**

#### Step 2: Upload Files to GitHub

**Using GitHub Web UI (Easiest):**

1. In your new repository, click **Add file** → **Upload files**
2. Drag and drop all project files and folders
3. Make sure folder structure is preserved:
   ```
   - index.html
   - login.html
   - dashboard.html
   - members.html
   - css/
   - js/
   ```
4. Click **Commit changes**

**Using Git Command Line:**

```bash
# Navigate to your project folder
cd path/to/vteam-fitness-hub

# Initialize git
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit: V Team Fitness Hub"

# Add remote (replace YOUR_USERNAME)
git remote add origin https://github.com/YOUR_USERNAME/vteam-fitness-hub.git

# Push to GitHub
git push -u origin main
```

#### Step 3: Enable GitHub Pages

1. Go to repository settings → **Pages**
2. Under "Source", select **main** branch
3. Folder: **root**
4. Click **Save**
5. Wait 1-2 minutes for deployment
6. Your site is now live at: `https://YOUR_USERNAME.github.io/vteam-fitness-hub`

### Deploy to Cloudflare Pages 🌐

#### Step 1: Connect GitHub to Cloudflare

1. Go to https://pages.cloudflare.com
2. Click **Connect to Git**
3. Authorize GitHub
4. Select repository: `vteam-fitness-hub`
5. Click **Begin setup**

#### Step 2: Configure Build Settings

1. **Framework preset**: None (static site)
2. **Build command**: (leave empty)
3. **Build output directory**: (leave empty)
4. Click **Save and Deploy**
5. Your site is live at: `https://vteam-fitness-hub.pages.dev` (or custom domain)

## How to Use 📖

### Landing Page
- Displays features and benefits
- "Get Started" button links to login
- Theme toggle (dark/light mode)

### Login Page
- Enter credentials: `vteam@vteamfitness.com` / `Bilal`
- Password visibility toggle
- "Back to Home" link

### Dashboard
- **Total Members**: Total count of all members
- **Active Members**: Members whose membership hasn't expired
- **Expiring in 10 Days**: Members expiring within 10 days
- **Expired in 30 Days**: Recently expired members (last 30 days)
- Click any card to filter members
- Recent activity log showing latest additions/updates

### Members Management
- **Search**: Real-time search by name or phone
- **Filter**: Filter by All/Active/Expired/Expiring Soon
- **Add Member**: Click "Add Member" button to open form
- **Edit Member**: Click "Edit" button on member card
- **Delete Member**: Click "Delete" button (requires confirmation)
- **Message**: Click "Message" to send WhatsApp reminder
- **Refresh**: Manual refresh button for immediate updates

### Form Fields

When adding/editing a member:

- **Name** (required): Full name
- **Phone** (required): Indian phone number (+919XXXXXXXXX)
- **Gender** (required): Male, Female, or Other
- **Membership Type** (required): Monthly, Quarterly, or Yearly
- **Duration** (required): Based on membership type
- **Join Date** (required): Member's start date
- **Expiry Date** (auto-calculated): Can be manually edited

## Features Explained 💡

### Real-time Updates
All changes sync instantly to Firebase and appear on all connected devices without page refresh.

### WhatsApp Integration
- Click "Message" button on any member
- Opens WhatsApp with pre-filled renewal reminder
- Works on mobile and desktop

### Member Status
- **Active** (Green): Membership valid, expires in > 30 days
- **Expiring Soon** (Yellow): Expires in 10-30 days
- **Expired** (Red): Membership expired

### Analytics Cards
- Click any card to navigate to members page with pre-applied filter
- Numbers update in real-time as members are added/deleted

### Theme Toggle
- Click moon/sun icon to switch dark/light theme
- Preference saved in browser
- Applies to entire site

## Troubleshooting 🔧

### Members not showing?
1. Check if logged in
2. Make sure Firebase database has members data
3. Click refresh button
4. Check browser console for errors

### Can't login?
1. Verify credentials: `vteam@vteamfitness.com` / `Bilal`
2. Check Firebase authentication setup
3. Clear browser cache and try again

### WhatsApp not opening?
1. Use only Indian phone numbers
2. Include country code (+91)
3. On mobile, WhatsApp app must be installed
4. On desktop, browser must support WhatsApp Web

### Changes not syncing?
1. Check internet connection
2. Verify Firebase is initialized
3. Check browser console for Firebase errors
4. Try refreshing page

## Firebase Database Structure 📊

```json
{
  "members": {
    "member_timestamp_random": {
      "id": "member_id",
      "name": "John Doe",
      "phone": "+919876543210",
      "gender": "MALE",
      "membershipType": "MONTHLY",
      "duration": "1 month",
      "joinDate": "2026-05-01",
      "expiryDate": "2026-05-30",
      "status": "Active",
      "createdAt": 1704067200000,
      "updatedAt": 1704067200000
    }
  }
}
```

## Performance Tips ⚡

1. **Optimize images**: Keep image sizes small
2. **Cache Firebase SDK**: Browser caches it automatically
3. **Minimize API calls**: Use real-time listeners instead of repeated queries
4. **Database indexes**: Not needed for < 1000 members

## Security Notes 🔒

- Admin credentials stored in Firebase Authentication (hashed)
- Database rules restrict access to authenticated users
- API keys in config are safe (Firebase rules protect data)
- HTTPS enforced by GitHub Pages/Cloudflare
- No sensitive data stored in localStorage

## Limitations ⚠️

- Firebase free tier: 1GB storage, 100 simultaneous connections
- GitHub Pages: No server-side code, only static files
- Real-time updates depend on active internet connection
- Maximum recommended members: 10,000 (Firebase limit)

## Future Enhancements 🎯

- Export members to CSV/Excel
- Member payment history
- Attendance tracking
- Email notifications
- SMS integration
- Custom membership plans
- Multi-language support
- Admin role management

## Support & Help 📞

For issues or questions:
1. Check Firebase console for errors
2. Open browser developer console (F12)
3. Check Firebase Realtime Database data
4. Verify authentication rules in Firebase

## License 📄

This project is created for V Team Fitness Hub. All rights reserved.

---

**Created with ❤️ for V Team Fitness Hub**

Last Updated: May 2, 2026
Version: 1.0.0
