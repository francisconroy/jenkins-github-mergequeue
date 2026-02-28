# jenkins-github-mergequeue
A repository to capture experiments and results about using jenkins with a github merge queue

## Jenkinsfile Configuration

The repository includes a `Jenkinsfile` that:
- Runs on change requests (pull requests) and branches
- Does NOT run on the `main` branch (skips execution after merge to main)
- Executes on Linux agents
- Includes a simple echo command for demonstration purposes

The pipeline uses a `when` condition with `not { branch 'main' }` to ensure the build step only executes for non-main branches, making it suitable for CI validation before merging.
