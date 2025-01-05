# Frappe-Bench-Commands
This document provides a comprehensive list of Frappe Bench commands for setup, maintenance, development, database management, site management, performance, and advanced usage.  

## **Setup and Maintenance**  

### 1. Install and Setup  
- `bench init [folder_name]` - Initialize a new Frappe Bench environment.  
- `bench new-site [site_name]` - Create a new site.  
- `bench get-app [app_name]` - Get a new app from a Git repository.  
- `bench install-app [app_name]` - Install an app on a site.  
- `bench start` - Start the development server.  

### 2. Update and Upgrade  
- `bench update` - Pull updates for apps, run patches, and build assets.  
- `bench upgrade` - Upgrade to a newer version of Frappe or ERPNext.  

### 3. Environment  
- `bench setup requirements` - Install Python and Node.js dependencies.  
- `bench setup redis` - Setup Redis cache and queues.  
- `bench setup supervisor` - Setup Supervisor process manager.  
- `bench setup nginx` - Generate Nginx configuration.  
- `bench setup production` - Setup production environment (includes Supervisor and Nginx).  

---

## **Development**  

### 1. App Development  
- `bench new-app [app_name]` - Create a new Frappe app.  
- `bench make-app [app_name]` - Create a new app (alternative to `new-app`).  

### 2. Code Management  
- `bench build` - Build JS and CSS assets.  
- `bench watch` - Watch for changes in JS/CSS and build automatically.  
- `bench migrate` - Apply schema changes and patches.  

### 3. Debugging and Testing  
- `bench console` - Open a Python shell with Frappe loaded.  
- `bench execute [method_name]` - Execute a Python method.  
- `bench set-config [key] [value]` - Set a configuration value.  
- `bench run-tests` - Run tests in the app or site.  

---

## **Database Management**  

### 1. Backup and Restore  
- `bench backup` - Take a backup of the site.  
- `bench restore [backup_file_path]` - Restore a site from a backup.  

### 2. Database Utilities  
- `bench mariadb` - Access the MariaDB database shell.  
- `bench reload-doc [module] [doctype]` - Reload a specific DocType.  

---

## **Site Management**  

### 1. Site Operations  
- `bench use [site_name]` - Set the default site.  
- `bench drop-site [site_name]` - Drop a site and delete the database.  
- `bench reinstall` - Reinstall a site (deletes all data).  

### 2. Site Configuration  
- `bench set-mysql-root-password` - Set the MySQL root password.  
- `bench set-admin-password` - Set the admin password for a site.  
- `bench set-url-root` - Set the URL root for a site.  

### 3. Multi-tenancy  
- `bench enable-scheduler` - Enable the scheduler for a site.  
- `bench disable-scheduler` - Disable the scheduler for a site.  

---

## **Performance and Monitoring**  

### 1. Performance Tools  
- `bench profile` - Profile a site and show SQL queries and their time.  
- `bench doctor` - Check for any background jobs that are stuck.  

### 2. Queue Management  
- `bench restart` - Restart all services (Redis, Nginx, etc.).  
- `bench clear-cache` - Clear the cache for the site.  
- `bench clear-queue` - Clear all queued jobs.  

---

## **Custom Scripts and Utilities**  

### 1. Scripts  
- `bench run-patch [patch_name]` - Run a specific patch.  
- `bench execute [method_path]` - Execute a specific method.  

### 2. Localization  
- `bench get-translations` - Pull translations for a language.  
- `bench update-translations` - Update translations for a language.  

### 3. Logging and Monitoring  
- `bench log` - Tail logs for the Frappe Bench.  
- `bench worker` - Start a background worker process.  

---

## **Advanced**  

### 1. Advanced Bench Commands  
- `bench --help` - View help for Bench commands.  
- `bench retry-upgrade` - Retry an upgrade process.  
- `bench switch-to-branch [branch]` - Switch to a specific branch for apps.  

---

## Notes  
- Use these commands cautiously, especially in production environments.  
- Always backup your data before making significant changes.  
