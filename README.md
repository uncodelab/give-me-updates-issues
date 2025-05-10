# Give Me Updates - Digital Product Delivery System 🚀
[![License: Restricted](https://img.shields.io/badge/License-Proprietary-red)](LICENSE) 
![PHP Version](https://img.shields.io/badge/PHP-8.4%2B-purple) 
![Laravel Version](https://img.shields.io/badge/Laravel-12%2B-red) 
[![GitHub Issues](https://img.shields.io/github/issues/uncodelab/give-me-updates-issues?label=Public%20Issues)](https://github.com/uncodelab/give-me-updates-issues) 

A robust solution for creators to manage and deliver digital product updates to customers who purchased through Ko-fi and BuyMeACoffee platforms.

### Traditional Method Pain Points
1. Manual email updates
2. Version confusion
3. Security risks with permanent links
4. No download tracking

### Our Advantages
✅ **Automatic Customer Sync**  
✅ **Centralized Version Control**  
✅ **Usage Analytics Dashboard**  
✅ **Military-Grade Security**  
✅ **Platform Agnostic Architecture**

**Upgrade Your Digital Business**  
Stop wasting time on manual deliveries - automate like a pro!

---

## Requirements 📋

- PHP 8.4+ with extensions
- MySQL 5.7+/PostgreSQL
- Composer 2.0+
- GitHub Personal Access Token

---

## Installation 🛠️

1. **Initial Setup**:
```bash
# Extract the ZIP
unzip give-me-updates-<version>.zip -d your-project-folder
cd your-project-folder

# Install PHP dependencies
composer install --no-dev

# Create environment file
cp .env.example .env

# Generate application key
php artisan key:generate
```

2. **Environment Configuration**:
```bash
# Edit environment file
nano .env

# Update these values
APP_NAME="Coffee hook"
APP_URL=http://yourdomain.com

DB_CONNECTION=mysql
DB_DATABASE=your_database_name
DB_USERNAME=your_db_username
DB_PASSWORD=your_db_password

MAIL_MAILER=smtp
MAIL_SCHEME=smtps
MAIL_HOST=your_mail_server.com
MAIL_PORT=465
MAIL_USERNAME=your_mail_username
MAIL_PASSWORD=your_mail_password
MAIL_FROM_ADDRESS="your_noreply@yourdomain.com"

BMC_WEBHOOK_SECRET=your_bmc_webhook_secret_here
KOFI_WEBHOOK_TOKEN=your_kofi_verification_token_here
GITHUB_TOKEN=your_github_personal_access_token_here
ADMIN_USERNAME=your_admin_username
ADMIN_PASSWORD=your_admin_password
USE_CLOUDFLARE=true
```

3. **Database Migration**:
```bash
# Run migrations (creates tables)
php artisan migrate
```

4. **Frontend Assets**:
```bash
# Install Node.js dependencies
npm install

# Build assets
npm run build
```

5. **Permissions**:
```bash
# Set proper storage permissions
chmod -R 775 storage/
chmod -R 775 bootstrap/cache/
```

6. **Configure Webhooks**:
- **BuyMeACoffee**:  
  Platform URL: `https://studio.buymeacoffee.com/webhooks`  
  Your Endpoint: `https://yourdomain.com/webhook/bmc`
- **Ko-fi**:  
  Platform URL: `https://ko-fi.com/manage/webhooks`  
  Your Endpoint: `https://yourdomain.com/webhook/kofi`

---

## Updates ⬆️

To get the latest version of Give Me Updates:
1. **Visit the Updates Portal**:
   - Go to [givemeupdates.uncodelab.com](https://givemeupdates.uncodelab.com).
2. **Enter Purchase Key**:
   - Input your BuyMeACoffee or Ko-fi purchase key (received after buying the app).
3. **Receive Download Link**:
   - A download link for the latest `give-me-updates-<version>.zip` will be emailed to you.
4. **Update Your Installation**:
   - Replace your existing files with the new:
     - **Backup Your Current Installation**: Save a copy of your existing project folder and database to prevent data loss. Ensure your database is fully backed up before proceeding.
     - **Extract the ZIP File**: Unzip the downloaded give-me-updates-<version>.zip to a temporary location.
     - **Replace Files**: Copy the extracted files to your project directory, overwriting the old files.
     - **Run Database Migrations**: If the update includes database changes, run php artisan migrate from your project directory to update the database schema.
     - **Clear Cache**: If your application uses caching, run php artisan cache:clear to ensure new features work correctly.
     - **Test the Update**: Verify that the application runs as expected after the update.

**Note**: Check [givemeupdates.uncodelab.com](https://givemeupdates.uncodelab.com) periodically for new features and bug fixes.

---

## Features ✨

### Seller-Centric Management
- **Dual Platform Integration**  
  - Auto-sync with Ko-fi and BuyMeACoffee webhooks
- **Flexible Delivery Options**  
  - Upload files directly or link GitHub repositories
- **Smart Version Control**  
  - Automatic GitHub release packaging (latest release or main branch)

### Secure Customer Access
- **Temporary Access Links**  
  - Limited time valid download tokens with usage tracking
- **Anti-Abuse Protection**  
  - Rate limiting and IP tracking
- **Secure Delivery**  
  - Masked email confirmation and download validation

### Intelligent Tracking
- Real-time download analytics
- Customer request history
- Token usage monitoring

---

## Usage 💻

### Linking GitHub Repositories
1. Navigate to Purchased Items
2. Enter `username/repo` format
3. System auto-validates repository access

### Customer Flow
1. Purchase on supported platform
2. Receive purchase ID via email
3. Request download links at `http://yourdomain.com`
4. Receive secure email with limited time access

---

## Changelog 📜
See the [CHANGELOG.md](https://github.com/uncodelab/give-me-updates-issues/blob/main/CHANGELOG.md) file for a detailed history of updates and changes to Give Me Updates.

---

## Issue Tracker 🐞
[![GitHub Issues](https://img.shields.io/github/issues/uncodelab/give-me-updates-issues?label=Public%20Issues)](https://github.com/uncodelab/give-me-updates-issues)

All bug reports and feature requests are managed through our public issue tracker.

Encounter a bug or have a feature idea? File it at [Give Me Updates Issues](https://github.com/uncodelab/give-me-updates-issues):
- **Bugs**: Provide steps to reproduce, expected vs. actual behavior, and system details.
- **Features**: Describe the feature and its benefits.

**Tip**: Check existing issues to avoid duplicates.

---

## Project Status 🏗️

Actively maintained with regular updates.

---

## License 📝
[![License: Restricted](https://img.shields.io/badge/License-Proprietary-red)](LICENSE)

**This is NOT open-source software.**  
**See full [LICENSE](LICENSE) for legal terms of use.**  
**Unauthorized distribution violates copyright laws.**

---

*Copyright (c) 2025 uncodelab. All rights reserved.*