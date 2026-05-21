# Privacy Policy for Potopopi CamSync

**Last Updated: May 21, 2026**

Potopopi CamSync ("we," "us," or "our") is dedicated to protecting the privacy of our users. This Privacy Policy outlines how we handle data within the Potopopi CamSync mobile application (the "App") and our website.

### 1. Privacy-First & Local-Only Design
Potopopi CamSync is designed from the ground up as a direct, client-side synchronization utility. **We do not host any backend servers, track analytics, or collect user data.**
- All file synchronization workflows run purely on your local device.
- All media files, authentication tokens, and server addresses are transmitted directly to your chosen endpoints.
- We never intercept, read, store, or share your media or credentials.

### 2. High-Privilege Permissions and Rationale
To function as a direct digital camera backup client, Potopopi CamSync requires specific hardware and file access permissions. We only invoke these permissions for user-directed tasks:

*   **All Files Access (`MANAGE_EXTERNAL_STORAGE`):**
    Required to inspect, manage, and back up media from user-selected local folders, external storage volumes, and physical MicroSD cards. Since the App serves as a robust file backup and restore client, broad file access is necessary to copy large RAW files, catalog assets, and perform automated local file pruning safely.
*   **Storage Access (`READ_EXTERNAL_STORAGE` / `WRITE_EXTERNAL_STORAGE`):**
    Requested on older Android versions (API 32 and below) to facilitate local storage read and write tasks.
*   **Media Access (`READ_MEDIA_IMAGES` / `READ_MEDIA_VIDEO`):**
    Requested on Android 13+ to selectively read photos and videos from the system gallery for background backup routing.
*   **USB Host Communication (`android.hardware.usb.host` / `USB_PERMISSION`):**
    Required to establish direct physical OTG/MTP links with digital cameras and external SD card readers.
*   **Network & Internet Access (`INTERNET` / `ACCESS_NETWORK_STATE`):**
    Required to establish direct, encrypted HTTPS connections with your Google Drive, Nextcloud, and Immich endpoints.
*   **Foreground Sync Services (`FOREGROUND_SERVICE` / `FOREGROUND_SERVICE_DATA_SYNC`):**
    Required to perform active file transfers in the background without the operating system interrupting or terminating the synchronization process.

### 3. Secure Credential Storage
Your authentication credentials never leave your device, except to authenticate directly with your selected providers:
*   **Encrypted Storage:** All Google OAuth2 tokens, Nextcloud WebDAV passwords, and Immich API keys are stored securely using Android's native **EncryptedSharedPreferences** framework. This secures them against unauthorized reads by other applications or physical extractions.
*   **No Third-Party Transmission:** We never collect or transmit your credentials. Communication with your storage providers occurs strictly over secure HTTPS connections.

### 4. Google Drive Data Scope Compliance
Our use and transfer of information received from Google APIs to any other app will adhere to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the Limited Use requirements.
*   **Requested Scope:** `https://www.googleapis.com/auth/drive.file`
*   **Limited Scope Access:** The App only reads, writes, and manages files and folders that were explicitly created by Potopopi CamSync. We cannot see or modify other files in your Google Drive.

### 5. Support and Inquiries
For any questions regarding your privacy, please contact:
*   **Email:** purnadika@proton.me
