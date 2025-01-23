## Users
In Jenkins, **users** refer to individuals who interact with the Jenkins server. Users can log in to Jenkins, trigger builds, view build statuses, and manage various aspects of the CI/CD pipeline. Each user in Jenkins is represented by a unique user account, which may have specific permissions and roles.

## Authentication
**Authentication** in Jenkins is the process of verifying the identity of users trying to access the Jenkins server. Jenkins supports various authentication methods, including:
- **Built-in User Database:** Jenkins comes with a built-in user database where you can create and manage user accounts directly within Jenkins.
- **External Authentication:** Jenkins can integrate with external authentication systems such as LDAP, Active Directory, OAuth, SSO (Single Sign-On), and others.

## Authorization
**Authorization** in Jenkins is the process of determining what actions an authenticated user is allowed to perform within the Jenkins environment. Jenkins provides several authorization strategies, including:
- **Matrix-based Security:** Allows fine-grained control over user permissions by defining roles and assigning specific permissions to those roles.
- **Project-based Matrix Authorization:** Extends matrix-based security to individual projects, allowing different permissions for different projects.
- **Role-Based Strategy:** Uses roles to define permissions and assigns users or groups to those roles.

## Example Configuration in Jenkins
Here's an example of configuring matrix-based security in Jenkins:

```yaml
security:
  authorization:
    strategy: "Matrix Authorization Strategy"
    permissions:
      - user: "admin"
        permissions:
          - "Overall/Administer"
      - user: "user-1"
        permissions:
          - "Overall/Read"
          - "Job/Read"
          - "Job/Build"
      - user: "user-2"
        permissions:
          - "Overall/Read"
          - "Job/Read"
          
```

## Demo
1. Login with the admin user (First Admin User)
2. Goto "Manage Jenkins" > "Security" Or Visit "http://localhost:8080/manage/configureSecurity/"
3. Change "Authorization" from "Logged In Users can do Anything" to "Metrix Based Security"
4. Click on "Add User" button to add user current admin user (In my case it was `mahendra`)
5. Repeate same process to add Other users (User-1 and User-2)
6. For Admin user `mahendra` set "Overall/Administrator" permissions.
7. For User-2 and User-1 set "Overall/Read" permission.
8. Open a new `Private` or `Incognito` browser window and login with `User-1` or `User-2`

