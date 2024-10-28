# devops-livecoding

base for GitHub Actions

# Questions

#### What are test containers ?

Java libraries that enable integration testing with lightweight, disposable Docker containers, allowing isolated, reliable tests for dependencies like databases and message queues.

#### Document your GitHub Actions configurations

1. **Workflow Name**: `CI devops 2024`
    - The workflow name is displayed in GitHub Actions for easy identification.

2. **Trigger Conditions** (`on`):
    - **Push Events**: The workflow is triggered on pushes to the `main` and `develop` branches.
    - **Pull Requests**: It also runs on every pull request to ensure the code is up to quality standards before merging.

3. **Job Definition** (`jobs`):
    - **Job Name**: `test-backend`
        - **Runs-On**: The job runs on an `ubuntu-22.04` environment.

4. **Job Steps** (`steps`):
    - **Checkout Repository**: Uses `actions/checkout@v2.5.0` to clone the repository, making the code accessible within the workflow.
    - **Set Up JDK 17**: Uses the `actions/setup-java@v3` action to install JDK 17 with the Amazon Corretto distribution, which is compatible with many Java applications.
    - **Build and Test with Maven**: Executes `mvn clean verify` in the `simple-api` directory to build the project and run tests.


#### For what purpose do we need to push docker images ?

Pushing Docker images allows for easy deployment across environments, ensures version control, and facilitates collaboration among team members by providing a consistent application environment.

#### Document your quality gate configuration

![img.png](img.png)

## Quality Gate Status

| Metric           | Status       | Details                           |
|------------------|--------------|-----------------------------------|
| **Quality Gate** | Passed ✅    | Meets configured quality criteria |

## Code Quality Metrics

- **Security**:
   - **2** Open issues
   - **3** Security hotspots

- **Reliability**:
   - **0** Open issues
   - **Rating**: D

- **Maintainability**:
   - **2** Open issues
   - **Rating**: A

- **Coverage**:
   - **53.6%** of code covered by tests
   - **123** lines are set for coverage conditions

- **Duplications**:
   - **0.0%** code duplication
   - **583** lines analyzed for duplication
  

