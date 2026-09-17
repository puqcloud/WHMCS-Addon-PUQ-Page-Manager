# WHMCS Module Installation and Update

### PUQ Page Manager module **[WHMCS](https://puqcloud.com/link.php?id=77)**
##### [Order now](https://puqcloud.com/whmcs-addon-puq-page-manager.php) | [Download](https://download.puqcloud.com/WHMCS/addons/PUQ_WHMCS-Page-Manager/) | [Community](https://community.puqcloud.com/)

## System requirements

| Requirement | Minimum |
|-------------|---------|
| **WHMCS** | 8.x+, 9.x+ |
| **PHP** | 7.4, 8.1, 8.2, 8.3, 8.4 |
| **ionCube Loader** | v15+ |

> **Note:** The module uses ionCube encoding. Make sure ionCube Loader is installed and active on your server.

---

## Download

The module can be ordered and downloaded from PUQ Cloud:

- **Order Module:** [https://puqcloud.com/whmcs-addon-puq-page-manager.php](https://puqcloud.com/whmcs-addon-puq-page-manager.php)
- **Documentation:** [https://doc.puq.info/books/page-manager-whmcs-addon](https://doc.puq.info/books/page-manager-whmcs-addon)
- **All Versions / Download:** [https://download.puqcloud.com/WHMCS/addons/PUQ_WHMCS-Page-Manager/](https://download.puqcloud.com/WHMCS/addons/PUQ_WHMCS-Page-Manager/)
- **Support:** [https://puqcloud.com/submitticket.php?step=2&deptid=1](https://puqcloud.com/submitticket.php?step=2&deptid=1)
- **Community:** [https://community.puqcloud.com/](https://community.puqcloud.com/)
- **Direct download link for the latest version:**

```bash
wget https://download.puqcloud.com/WHMCS/addons/PUQ_WHMCS-Page-Manager/PUQ_WHMCS-Page-Manager-latest.zip
```

> All versions can be found at this link:
> [https://download.puqcloud.com/WHMCS/addons/PUQ_WHMCS-Page-Manager/](https://download.puqcloud.com/WHMCS/addons/PUQ_WHMCS-Page-Manager/)

---

## Installation

### Step 1: Unzip the Archive
On your WHMCS server (or locally):
```bash
unzip PUQ_WHMCS-Page-Manager-latest.zip
```

### Step 2: Copy the Module Files
Copy the extracted module directory directly to your WHMCS directory:

```bash
# For addon modules:
cp -r PUQ_WHMCS-Page-Manager/puq_page_manager /var/www/html/whmcs/modules/addons/
```


### Step 3: Activate and Configure the Addon Module
1. Log in to the WHMCS admin area.
2. Navigate to **System Settings > Addon Modules** (or **Setup > Addon Modules** in older WHMCS versions).
3. Find **PUQ Page Manager** in the list and click **Activate**.
4. Click **Configure**, enter your **License Key**, and select the admin groups allowed to access the module.
5. Click **Save Changes**.

---

## File Structure

Structure of files after a successful installation:
```
whmcs/
├── modules/
│   └── addons/
│       └── puq_page_manager/           # Addon files
```

---

## Update Procedure

To update the module to a newer version:
1. **Deactivate** the addon module in **Setup > Addon Modules**.
2. Make a backup of your WHMCS files and database.
3. Download the latest version for your PHP version.
4. Extract the ZIP and overwrite the existing files in the `modules/` directories.
5. **Reactivate** the addon module in **Setup > Addon Modules** (this will trigger database migrations). All settings and client data are safe during this process.
