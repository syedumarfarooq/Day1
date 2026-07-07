pipeline {
    agent any

    stages {
        stage('Clean') {
            steps {
                deleteDir()
            }
        }
        stage('Build') {
            
            steps {
                // Get some code from a GitHub repository
git branch: 'main', url: 'https://github.com/syedumarfarooq/Day1'
                // Run the build on a Unix agent. You must have Maven installed.
                

                // To run Maven on a Windows agent, use
                // bat 'mvn -Dmaven.test.failure.ignore=true clean package'
            }

            post {
                // If Maven was able to run the tests, even if some of the test
                // failed, record the test results and archive the jar file.
                success {
                    archiveArtifacts artifacts: '**/*', followSymlinks: false
                }
            }
        }
    }
}
