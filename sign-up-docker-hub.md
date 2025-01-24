# Sign up for Free Docker Registry 

1. Visit `https://app.docker.com/signup`, provide your email address (Personal email, same one used in GitHub). then provide a unique `username` and password.
2. If `username` entered by you is unavailable (Already taken by some other user) try using a different name.
3. Click `Sign Up`
4. Check your inbox for Docker Activation email (Might be tagged as spam or clutter by your mail provider)
5. Click on the `link` to activate your Docker Hub account.
6. Note down your dockeriid and password
    > Example: docker-id => mahendra2515, password => Password123
7. Login into Jenkins server at `http://20.197.17.42/` with credentials `mahendra/Password@1234`
8. Goto `Jenkins Manager` -> `Credentials` -> `System` -> `Global` -> Click `New Credentials`
9. Use name `my-docker-id` as credential id, then select `Kind` as `Username and password. Use the credentials of your newly created docker hub account.
10. Click on `Create` or `Save`
