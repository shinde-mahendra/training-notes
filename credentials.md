# Credentials in Jenkins

Credentials in Jenkins are used to securely store and manage authentication information for external systems and services that Jenkins interacts with, such as artifact repositories, cloud storage, and databases[  Credentials - Jenkins](https://www.jenkins.io/doc/book/security/credentials/). This ensures that sensitive information like usernames, passwords, API tokens, and SSH keys are not hard-coded into Jenkins pipelines, making the system more secure and easier to manage[  Credentials - Jenkins](https://www.jenkins.io/doc/book/security/credentials/).

### Types of Credentials
Jenkins supports several types of credentials:
- **Secret Text**: A token such as an API token[Using credentials - Jenkins](https://www.jenkins.io/doc/book/using/using-credentials/).
- **Username and Password**: Can be handled as separate components or as a colon-separated string[Using credentials - Jenkins](https://www.jenkins.io/doc/book/using/using-credentials/).
- **Secret File**: Secret content stored in a file[Using credentials - Jenkins](https://www.jenkins.io/doc/book/using/using-credentials/).
- **SSH Username with Private Key**: An SSH public/private key pair[Using credentials - Jenkins](https://www.jenkins.io/doc/book/using/using-credentials/).
- **Certificate**: A PKCS#12 certificate file and optional password[Using credentials - Jenkins](https://www.jenkins.io/doc/book/using/using-credentials/).
- **Docker Host Certificate Authentication**: Credentials for Docker host certificate authentication[Using credentials - Jenkins](https://www.jenkins.io/doc/book/using/using-credentials/).

### Credential Security
To maximize security, credentials in Jenkins are stored in an encrypted form on the Jenkins controller[ Using credentials - Jenkins](https://www.jenkins.io/doc/book/using/using-credentials/). They are only handled via their credential IDs in Pipeline projects, minimizing the risk of exposing actual credentials[ Using credentials - Jenkins](https://www.jenkins.io/doc/book/using/using-credentials/).

## Credential Manager in Jenkins

The Credential Manager in Jenkins is a centralized system for managing credentials[ Managing credentials in Jenkins - Octopus Deploy](https://octopus.com/blog/managing-jenkins-credentials). It allows Jenkins administrators to add, configure, and manage credentials that can be used across different projects and users[ Using credentials - Jenkins](https://www.jenkins.io/doc/book/using/using-credentials/).

### Managing Credentials
1. **Add Credentials**: Jenkins users with the "Credentials > Create" permission can add new credentials[ Using credentials - Jenkins](https://www.jenkins.io/doc/book/using/using-credentials/).
2. **Configure Credentials**: Credentials can be configured globally or for specific folders and projects[ Using credentials - Jenkins](https://www.jenkins.io/doc/book/using/using-credentials/).
3. **Use Credentials**: Credentials can be used in Pipeline projects to access external resources securely[ Using credentials - Jenkins](https://www.jenkins.io/doc/book/using/using-credentials/).

### Best Practices
- **Limit Access**: Only grant access to credentials to specific users, projects, and items that require it[  Credentials - Jenkins](https://www.jenkins.io/doc/book/security/credentials/).
- **Protect Secrets**: Store keys in a secure location and avoid including them in backups[  Credentials - Jenkins](https://www.jenkins.io/doc/book/security/credentials/).
- **Update Credentials**: Regularly update credentials to maintain security[  Credentials - Jenkins](https://www.jenkins.io/doc/book/security/credentials/).

By following these practices, Jenkins ensures that credentials are managed securely and efficiently, reducing the risk of unauthorized access and potential security breaches.
