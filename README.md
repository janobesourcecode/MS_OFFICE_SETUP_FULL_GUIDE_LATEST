Here is your **fixed and professionally formatted guide**, with clearer wording, correct structure, and improved readability:

---

# Microsoft Office Deployment Tool Setup Guide

This guide explains how to download, configure, and install Microsoft Office using the Office Deployment Tool (ODT) with a custom configuration XML file.

---

## Step 1: Create the Configuration File

Use the Microsoft Office Customization Tool:

**Configuration Tool:**
[https://config.office.com/deploymentsettings](https://config.office.com/deploymentsettings)

### Configuration Steps

1. **Select Architecture**
   Choose your preferred architecture:

   * **64-bit** (Recommended)
   * 32-bit

2. **Select Product**

   * Office Suites → **Office Professional Plus (Volume License)**

3. **Select Language**

   * Choose: **English**

4. **Export Configuration**

   * Click **Export**
   * Save the file as:

   ```
   Configuration.xml
   ```

   * Place it in your Office setup folder, for example:

   ```
   C:\MS OFFICE SETUP
   ```

---

## Step 2: Download Office Deployment Tool (ODT)

Download from Microsoft:

[https://www.microsoft.com/en-us/download/details.aspx?id=49117](https://www.microsoft.com/en-us/download/details.aspx?id=49117)

### After Downloading

1. Run the downloaded file
2. Extract the contents to your Office setup folder:

```
C:\MS OFFICE SETUP
```

Your folder should now contain:

```
C:\MS OFFICE SETUP
│-- setup.exe
│-- Configuration.xml
```

---

## Step 3: Run Commands in Command Prompt (Administrator)

Open **Command Prompt as Administrator**, then run the following commands:

---

### Step 3.1: Go to Drive C Root

```cmd
CD\
```

---

### Step 3.2: Go to Office Setup Folder

```cmd
CD "C:\MS OFFICE SETUP"
```

---

### Step 3.3: Download Office Installation Files (Offline Installer)

This downloads all required Office files based on your Configuration.xml:

```cmd
Setup.exe /download Configuration.xml
```

Notes:

* This creates an **Office** folder containing installation files
* Download time depends on your internet speed
* Do not close Command Prompt during download

Expected folder structure after download:

```
C:\MS OFFICE SETUP
│-- setup.exe
│-- Configuration.xml
│-- Office\
│   └── (installation files)
```

---

### Step 3.4: Install Microsoft Office (Silent Installation)

Run the install command:

```cmd
Setup.exe /configure Configuration.xml
```

This will install:

* Office Professional Plus (Volume License)
* English language
* Selected architecture (32-bit or 64-bit)
* Silent installation (no user interaction required)

---

## Important Notes

* Always run **Command Prompt as Administrator**
* Do not close CMD during download or installation
* Internet is required for the download step
* Installation runs silently in the background
* You can reuse the downloaded files for offline installation on other computers

---

## Optional: Example of Complete Folder Structure

```
C:\MS OFFICE SETUP
│-- setup.exe
│-- Configuration.xml
│-- Office
│   ├── Data
│   ├── Office
│   └── (other installation files)
```

--- 