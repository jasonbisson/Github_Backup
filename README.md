# Git Backup Script

## Purpose

- Creates local copies of public repos: The script backup public git repositories onto your computer where they can be copied to cloud service like Google Drive or One Drive for long term backup.
- Accidental deletion: If you accidentally delete something on GitHub, you'll have a local copy to restore from.
- Account issues: If you lose access to your GitHub account, you won't lose your code.
- GitHub service disruptions: Even if GitHub goes down, you can still work with your code locally.

## Requirements

- Bash: The script is written in Bash, a common Unix shell.
- git: Ensure Git is installed on your system.
- jq: Required for parsing JSON responses from the GitHub API.
## Usage

- Download the script:
Clone this repository or download the github-backup.sh file.

- Execute the script with the following command:
```
./github-backup.sh <username>
```
Replace <username> with the GitHub username whose repositories you want to backup.

## Output

The script creates 
- A directory github_backup_username_date 
- A tar file github_backup_username_date.tar 

To complete the backup upload the tar file to either Google Drive, One Drive, or worst case a thumb drive.

## Features

Fetches a list of public repositories for the specified user.
Clones each repository into the designated backup directory.
Handles errors gracefully, providing informative messages.
## Customization

Backup directory: Modify the backup_directory variable within the script to change the default backup location.
Error handling: Adjust the check_exit function to refine error handling behavior.
Additional features: Explore adding options for custom backup directories, progress indicators, or rate limiting.
## Troubleshooting

Network issues: Ensure a stable internet connection.
GitHub API rate limits: If you encounter rate limits, consider adjusting the script's frequency or using authentication for increased limits.
Error messages: Review the terminal output for specific error messages and consult online resources or communities for assistance.
## Disclaimer

This script is provided for informational purposes only. Use it at your own risk.
It's not affiliated with GitHub in any way.
Consider implementing additional security measures and error handling for production environments.
## License

This script is licensed under the MIT License. See the LICENSE file for details.

## Contributing

Refer to the [contribution guidelines](./CONTRIBUTING.md) for
information on contributing to this module.

## Security Disclosures

Please see our [security disclosure process](./SECURITY.md).
