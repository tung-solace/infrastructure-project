# Jenkins — Things to Learn

## Fundamentals
- [ ] What Jenkins is and how it fits into CI/CD
- [ ] Jenkins architecture: controller (master) vs agents (nodes)
- [ ] Installation and initial setup (war file, Docker, package managers)
- [ ] Navigating the Jenkins UI and dashboard
- [ ] Managing users, roles, and permissions (matrix-based security, RBAC)

## Jobs and Builds
- [ ] Freestyle projects vs Pipeline projects vs Multibranch Pipelines
- [ ] Build triggers: SCM polling, webhooks, cron, upstream/downstream
- [ ] Parameterized builds
- [ ] Build artifacts and archiving
- [ ] Workspace management

## Pipelines (Jenkinsfile)
- [ ] Declarative vs Scripted pipeline syntax
- [ ] `stages`, `steps`, `agent`, `environment`, `post` blocks
- [ ] Shared libraries for reusable pipeline code
- [ ] Parallel stages and matrix builds
- [ ] `when` conditions and input steps
- [ ] Error handling: `try/catch`, `retry`, `timeout`
- [ ] Using `credentials()` and secret handling

## Distributed Builds
- [ ] Setting up agents (SSH, JNLP, Docker, Kubernetes)
- [ ] Labels and node selection
- [ ] Cloud agents (EC2, Kubernetes plugin)

## Plugins
- [ ] Plugin manager and updates
- [ ] Essential plugins: Git, Pipeline, Blue Ocean, Credentials, Docker, Slack
- [ ] Test reporting plugins: JUnit, Allure, HTML Publisher
- [ ] Code coverage plugins: JaCoCo, Cobertura

## Integrations
- [ ] Source control: Git, GitHub, GitLab, Bitbucket
- [ ] Artifact repositories: Nexus, Artifactory
- [ ] Container builds: Docker, Kubernetes
- [ ] Notifications: Slack, email, MS Teams
- [ ] Static analysis: SonarQube

## Security
- [ ] Credentials store and credential scopes
- [ ] Securing the controller (CSRF, agent-to-controller access control)
- [ ] Script approval and sandbox
- [ ] Auditing and access logs

## Operations & Scaling
- [ ] Backup strategies (JENKINS_HOME, ThinBackup plugin)
- [ ] Upgrading Jenkins and plugins safely
- [ ] Monitoring: build metrics, JVM tuning, disk usage
- [ ] Configuration as Code (JCasC)
- [ ] Jenkins on Kubernetes (Helm chart, dynamic agents)

## Advanced Topics
- [ ] Writing custom shared library steps in Groovy
- [ ] Creating custom plugins
- [ ] REST API and `jenkins-cli`
- [ ] Multibranch + PR validation workflows
- [ ] Migrating from freestyle to pipelines

## Practical Exercises
- [ ] Build a Jenkinsfile for a sample project end-to-end
- [ ] Set up a multibranch pipeline with PR builds
- [ ] Configure a distributed build with at least one agent
- [ ] Implement a shared library and consume it from a pipeline
- [ ] Set up JCasC to define Jenkins config in a YAML file
