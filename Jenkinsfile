pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               // bat "rmdir  /s /q time-tracker"
                // bat "git clone https://github.com/kishancs2020/time-tracker.git"
              // bat "mvn clean -f time-tracker"
                
              // ssh "rmdir  -rf time-tracker"
               ssh  "git clone https://github.com/Honeychaitanya/time-tracker.git"
               ssh "mvn clean -f time-tracker"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f time-tracker"
               // ssh "mvn install -f time-tracker"
            }
        }
        stage('test') {
            steps {
              bat "mvn test -f time-tracker"
                //ssh "mvn test -f time-tracker"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f time-tracker"
              //  ssh "mvn package -f time-tracker"
                
            }
        }
    }
}
