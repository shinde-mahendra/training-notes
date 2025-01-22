# Build Maven (Java) Project using Freestyle Project

## Basic Configuration

```yaml
General:
  Description: Sample Java Project
Source-Code-Management:
  Git:
    Repository: https://github.com/YOUR_GITHUB_ACC/ci-servlet-demo
Build-Triggers:
  Poll-SCM:
    Schedule: H/2 * * * *
Build-Steps:
  Invoke-Top-Level-Maven-Target:
    Maven-Version: M2
    Goals: package -DSkipTests
```
Save the configuration and just wait for 2 minutes for build to trigger
Once build is finished, check `Console Output` and `Workspace`

## Collect The artifacts

```yaml
General:
  Description: Sample Java Project
Source-Code-Management:
  Git:
    Repository: https://github.com/YOUR_GITHUB_ACC/ci-servlet-demo
Build-Triggers:
  Poll-SCM:
    Schedule: H/2 * * * *

Build-Environment: Delete workspace before build starts
  
Build-Steps:
  Invoke-Top-Level-Maven-Target:
    Maven-Version: M2
    Goals: package -DSkipTests

Post-Build-Steps:
  Archive-the-Artifacts:
    Files: target/*.war
```
