### What is CI/CD and how jenkins fit into that? 
### Continous Integration
Everytime a developer pushes code, there is a number of steps that needs to happen: 
 1. Pull the latest code
 2. Compile/build
 3. Run unit tests 
 4. Run static analysis/linters
 5. report

### Continously Delivery: 
After CI passes: 
1. Package the build (jar, Docker Image, e.t.c...)
2. Push to an artifact repo (Nexus, Artifactory, ECR)
3. Deploy automatically to a staging/test environment 
4. Run integration tests, smoke tests, perf tests. ()

### Environment variables: 
There are different types of environment variables that are available in Jenkins
Url to default environment variables: http://localhost:8080/env-vars.html/

Beside these, there are also other environment variables that we can define as well. 

environment {
    NEW_VERSION = '1.3.0'
}

### Build rentention: 
Build retention is Jenkins' policy for how long it keeps records of past builds before deleting them. Each build accumulates artifacts (archived files), console logs, metadata, e.t.c... on the Jenkins controller's disk. Without a retention policy, it grows forever. 

Example: 
```groovy

options {
    buildDiscarder(logRotator(numToKeepStr: '60', daysToKeepStr: '2'))
}

//Keep only the most 60 recent builds, and delete build older than 2 days
```

### Parameters
The parameters block declares the inputs the user must supply when triggering the build. In the Jenkins UI, this is what generates the "Build with Parameters" form -  each entry becomes a field operatios fill in before the job run. 