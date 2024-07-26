To approach this cybersecurity project at 4Geeks Academy, I would follow a methodical and structured approach to identify and resolve the issue with the malicious user. Here is a detailed step-by-step plan:

### 1. Review Current Permissions

- Check the permissions of each user in detail, including shared directories and files.

```bash
ls -l /home/alejandro 
ls -l /home/daniela 
```

### 2. Analyze Logs and Movements

- Look for suspicious activities in the authentication and system logs to identify unusual behavior patterns. Use getfacl to review ACL (Access Control List) permissions on common directories and files for each user. Example:

```bash
sudo getfacl /daniela
sudo getfacl /analista
```
- Correlate the suspicious activities found in the logs with the users who have inappropriate permissions. This could help identify the user attempting malicious activities.


### 3. Identify Malicious Actions

- Review the commands executed by users to understand their intentions. You can use the history command to see each user's command history. Example:

```bash
sudo -u vanessa history
```

### 4. Revoke Permissions and Report Evidence

- Once you identify the malicious user, revoke their root permissions using chmod and chown. Example:

```bash
sudo chmod 700 /home/analista
sudo chown analista:analista /home/analista
```

- Gather the evidence against the malicious user and protect the files with the special `sticky bit` permission so that the malicious user cannot modify them.


### Conclusion

With this methodical approach, we can identify the malicious user, analyze their movements, understand their intentions, and take corrective actions to ensure the system is secure and permissions are properly managed. This process also helps strengthen the team's security posture and prevent future incidents.
