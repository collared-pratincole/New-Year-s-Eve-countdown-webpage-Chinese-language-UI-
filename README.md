# NYE Carnival Countdown Webpage (Year-Universal Version)
## （中文readme见B站“搞机的初中生一枚”）
## 📌 Project Overview
A universal New Year's Eve interactive countdown webpage with Simplified Chinese UI, integrating immersive visual effects, real-time visitor statistics and online chat functions. It supports static + backend linkage deployment, no complex configuration required, and is compatible with any Gregorian New Year.


## ✨ Core Features
- **Dynamic Visual Effects**: Smooth gradient background, real-time fireworks animation, and Chinese New Year-style red packet rain effect
- **Real-time Online Count**: Unique visitor statistics based on Session ID technology, no duplicate counting, no privacy data collection
- **Interactive Chat Room**: Online chat function supported by PHP + Node.js backend (minor lag during peak hours)
- **Precise Countdown**: Millisecond-level synchronization with New Year's midnight, automatic trigger of full-screen stunning fireworks and red packet rain effects
- **Full-device Adaptation**: Responsive design, compatible with mobile phones, tablets, computers and all other terminals
- **Festive Elements**: Integrated Andy Lau-themed visual elements to enhance the New Year's Eve atmosphere


## 🚀 Complete Deployment Guide

### Deployment Prerequisites
1. A server supporting **PHP + MySQL** (virtual host or cloud server)
2. A GitHub account (for static resource deployment)
3. A database management tool (Navicat, phpMyAdmin, etc.)
### Final Deployment File Structure (Mandatory for Normal Functioning)

Deployment Root Directory (all files/folders at the same level, upload directly to GitHub/server root)
├── LICENSE # MIT License file
├── README.md # Project documentation
├── media/ # Media resource folder (copy directly, no modification)
├── music/ # Audio resource folder (copy directly, no modification)
├── index.html # Frontend main page (only need to modify countdown year)
├── config.php # Core database configuration file (MUST modify manually)
├── [Other Frontend/Backend Files] # All HTML/PHP/JS/CSS files (place directly, no changes)

### Step 1: File Preparation & Placement
1. Copy the `media/` and `music/` zip folders directly to the deployment root directory, **REMEMBER TO UNZIP THEM**;
2. Place all frontend/backend code files (from HTML.zip PHP.zip SQL.zip) directly in the root directory, **REMEMBER TO UNZIP THEM**, **do not nest in any folders**;
3. Put `config.php`, `LICENSE` and `README.md` in the root directory to match the above structure exactly.
   
### Step 2: Database Configuration (Critical! MUST Modify)
1. Open `config.php` in the root directory, replace the following database information with your actual details (no other changes needed):
   <?php
   // Database Configuration - Replace with your information
   $db_host = "localhost";    // Database address, default localhost no modification needed
   $db_name = "your_db_name"; // Your custom database name
   $db_user = "your_db_user"; // Database login username
   $db_pass = "your_db_pwd";   // Database login password
   ?>
2. Open the SQL script file in the project, copy all SQL code;
3. Connect to your MySQL server with a management tool, create a database with the same name as in config.php, paste the SQL code and execute to create data tables.

### Step 3: Universal Server Deployment (For Own Server/Virtual Host/GitHub Pages)
#### Option 1: Deploy to **Own Server/Virtual Host** (Recommended, Full Functions)
1. Upload all files/folders in the deployment root directory to the server's web root (e.g., `wwwroot/`, `public_html/`) via FTP/BT Panel/SSH
2. Ensure the server has `PHP+MySQL` enabled and the database configuration is completed (refer to Step 3.2)
3. Access directly via the server's domain/IP, no additional configuration required, all functions available
#### Option 2: Deploy to **GitHub Pages** (Static Display, Chat/Stats Need Backend Support)
1. Upload all files/folders in the deployment root directory to your GitHub repository
   - Recommended repo name: `[Year]-nye-countdown-webpage` (e.g., `2027-nye-countdown-webpage`)
2. Go to Repository → Click **Settings** → Scroll down to **Pages** section
3. Select `main` branch + `/(root)` directory in **Source**, click **Save**
4. Wait 1-3 minutes, access via: `https://<Your-GitHub-Username>.github.io/<Your-Repository-Name>`

### Step 4: Year Adaptation (Only 1 Step)
Open index.html in the root directory, find the countdown target time configuration, replace the year with your target New Year (e.g., 2027), and save.


## 🔧 Key Technical Notes
- **Configuration File**: Only config.php needs to be modified for database settings; all other PHP files automatically read this configuration;
- **Resource Folders**: The paths of media/ and music/ are hardcoded in the code, copy directly without modifying internal paths;
- **Tech Stack**: Native frontend (HTML5/CSS3/JS) + PHP backend + MySQL database + Canvas effects;
- **Chat Function**: Built on Node.js public source, minor message delay may occur during peak hours, no impact on core countdown experience.


## 📌 Important Notes
1. Strictly follow the deployment file structure; nested folders will cause resource loading failures and function errors;
2. Database information in config.php must be accurate, otherwise real-time statistics and chat functions will not work;
3. Modern browsers (Chrome/Edge/Firefox) are recommended for optimal effect display;
4. This is a static + backend linked project with no further updates; simply replace the countdown year for annual reuse.


## 📜 License
**This project is licensed under the MIT License**
