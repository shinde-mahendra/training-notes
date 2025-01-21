# Local first

1. Create a local repository using Windows Command prompt

   ```cmd
   cd \repos
   git init local-first
   cd local-first
   git status 
   ```
3. Create two text files inside the repository (Use notepad or VSCode)
4. Commit all the changes to local repository.
   
   ```cmd
   git add .
   git commit -m "Two files added"
   ```
6. Signin into Github using web browser
7. Create a new `public` Repository with name "local-first"
8. GitHub should display instructions on how to push local repository
   Choose "Second" option" It should contain lines like this one:

   ```cmd
   git remote add origin https://github.com/...../local-first.git
   git branch -M main
   git push -u origin main
   ```
10. Git CMD would ask for Credentials (Use GitHub Account and PAT)  
