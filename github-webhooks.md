# Github Webhooks to trigger Jenkins Job 

## Get the Fine-Grained Token for Access to GitHub

1. Log in to GitHub.com and visit [Personal Access Tokens](https://github.com/settings/personal-access-tokens).
2. Click **Generate new token**.
3. Enter a token name, e.g., `T1`.
   - **Repository Access**: Selected Repository `ci-servlet-demo`
   - **Repository Permissions**:
     - Commit Statuses: Read-Only
     - Contents: Read-Only
     - Webhooks: Read-Write (Try Read-Only)
   - Click **Generate Token**.
4. Copy the generated token and save it in a notepad (text document).

## Prepare Jenkins

1. Install the **GitHub** plugin:
   - Navigate to **Manage Jenkins** -> **Plugins** -> **Available Plugins**.
   - Search for **GitHub** and install it.
2. Go to **Manage Jenkins** -> **System**.
3. Scroll down to the **GitHub Server** section.
4. Click **Add GitHub Server**, enter a name like `github1`, and create a new **Secret Text** using the fine-grained token as the secret.
5. Click **Test Connection**.

## GitHub WebHook

1. Go to your GitHub repository.
2. Click on **Settings** -> **WebHooks**.
3. Click **Add Webhook**.
   - Provide the **Payload URL**: `http://20.197.17.42/github-webhook/`
   - Click **Add Webhook**.

## Modify Jenkins Project

1. Go to the Jenkins job and click **Configure**.
2. Set the build trigger to **GitHub Hook trigger for GITScm polling**.
3. Save the project.

## Test

1. Go to the repository on GitHub, make a change, and commit to the master branch.
2. **Expected**: The Jenkins project should start a new build.

