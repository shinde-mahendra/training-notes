# Integration with GitHub using PAT

## Create PAT for GitHub

1. Login into Github.com
2. Visit `https://github.com/settings/tokens` and choose `Token (Classic)` in left side panel.
3. Click on `Generate new token` and then choose `Generate new token (classic)`
4. Enter name `T1` in `Notes` textfield, then in `Scopes` select two scopes : `repo` and `user`
5. Scroll down and click on `Generate Token` button.
6. Copy the generated token and paste it in new text file (notepad) for later use.

## Store GitHub credentials in Jenkins Credential store
1. Login into Jenkins (Admin User)
2. Goto `Manage Jenkins` -> `Credentials` -> choose `System` -> choose `Global Credentials` -> Click `Add Credential` button.
3. Choose `Kind` as `Username and Password`, In `Username`, enter your github account name (my account name was `shinde-mahendra`)
4. in `Password`, just use PAT created in earlier steps.
5. provide secret ID and Description.
6. Click `Create` button

## Demo

1. Login into Github.com and create a `private repository` with Readme file.
2. Copy repository url for use in jenkins job later.
3. In jenkins, create a new Freestyle Job, in `Source Code Management` choose `Git` and then use the private repository url.
4. Jenkins must generate an ERROR message (Due to private repo being used)
5. Select your github credentials in `Credentials` drop down box.
6. Click `Save` button and try building this new job.
