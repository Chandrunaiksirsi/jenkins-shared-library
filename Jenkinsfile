@Library('my-shared-lib') _

pipeline {
    agent any
    tools {
        maven 'maven'
        jdk 'java21whe'
    }
    stages {
        stage ('checkout') {
            steps {
                git branch: 'project-1', url: 'https://github.com/Chandrunaiksirsi/Amazon.git'
            }
        }
        stage ('Build') {
            steps {
                mavenBuild()
            }
        }
        stage ('post-build') {
            steps {
                echo "Build completed successfully"
            }
        }
    }
}

