# DevOps Workflows

## Key Differences

| Aspect                  | Continuous Integration (CI)                      | Continuous Deployment (CD)                          |
|-------------------------|--------------------------------------------------|----------------------------------------------------|
| **Focus**               | Merging code changes frequently                  | Deploying code changes to production automatically |
| **Automation**          | Automated builds and tests on code commits       | Automated deployment to production after testing   |
| **Goal**                | Maintain a deployable codebase                   | Frequent and reliable software releases            |
| **Benefits**            | Early detection of integration issues, improved code quality | Faster feature delivery, reduced manual efforts, minimized risk of human error |

## Continuous Integration
   - To integrate changes made by dev-team into the central code repository.
   - Every time any of Developer makes any changes, we must execute this workflow to validate those changes.
   - Usual Steps :
     1. Get Source Code (Checkout)
     2. Fetch Dependencies
     3. Compile / Build
     4. Run Unit Tests
     5. Package the application
        
## Continuous Deployment
   - To collect the package (Built by CI Workflow)
   - Deploy in an "Environment" (stage)
   - Run few Tests
   - If Tests succeed, then deploy to Next Env
   - Run other of Tests
   - Repeat till Prod enviornment

