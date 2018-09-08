pipeline {
         agent any
         stages {
                 stage('Stage 1') {
                 steps {
                     echo 'Hi, this is stage 1'
                 }
                 }
                 stage('Stage 2') {
                 steps {
                    input('Do you want to proceed?')
                 }
                 }
                 stage('Stage 3') {
                 when {
                       not {
                            branch "master"
                       }
                 }
                 steps {
                       echo "Hello"
                 }
                 }
                 stage('Unit Test') {
                 parallel { 
                            stage('SHARATHs Unit Test') {
                           steps {
                                echo "Running the unit test..."
                           }
                           }
                          
                          
                          
                            stage('SHARATHs Integration test') {
                          
                              steps {
                                echo "Running the integration test..."
                              }
                           }
                          
                          
                           }
                           }
              }
}
