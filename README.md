
**Scripts Repository**

This repository contains various shell scripts for managing Digital Ocean cloud resources and operations. Below is a brief description of each script.

Scripts

1. **create_firewall_script.txt**

This script is used to create firewall rules. It can be customized to specify the rules and conditions required for your specific use case. It supports specifying:

        IP ranges
        Allowed protocols and ports
        Rule names and descriptions

You can tailor it to your specific network security requirements.

2. **create_snapshot_api.txt**

This script allows the creation of snapshots via API calls. It's useful for automating the backup process of your cloud resources. Key features include:

        Specifying resource IDs for snapshots
        Configurable snapshot naming conventions
        Scheduling options for automated snapshots

3. **delete_DOCR_images.txt**

This script is designed to delete images from the DigitalOcean Container Registry (DOCR). It's helpful for maintaining and cleaning up unused container images. It provides:

        Filtering criteria to select images for deletion
        Safe deletion with confirmation prompts
        Logging of deleted images for auditing purposes


4. **delete_snapshot_api.txt**

This script facilitates the deletion of snapshots through API calls, aiding in the management and cleanup of old or unnecessary snapshots. It includes:

        Listing existing snapshots
        Filtering options to target specific snapshots
        Deletion with error handling

**Usage**

**Clone the repository:**

        git clone https://github.com/zasghar26/Scripts.git
        cd Scripts

**Convert .txt to .sh:**

Before running the script read the script and change it as per your specific needs then convert the “.txt” files to “.sh” using the below command:

        mv <script_name>.txt <script_name>.sh

**Setting Up a Cron Job for Daily Snapshots**

To set up a cron job that runs the create_snapshot_api.sh script daily, follow these steps:

Open the crontab file:

        crontab -e

Add the following line to schedule the snapshot script to run daily at a specific time (e.g., 2 AM):

    0 2 * * * /path/to/create_snapshot_api.sh

Replace /path/to/create_snapshot_api.sh with the actual path to your script.

Save and close the crontab file.

The script will now run daily at the specified time.
