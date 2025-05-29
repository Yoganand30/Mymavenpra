pipline{
  agent any
    tools{
      maven 'MAVEN'
    }
    stages{
      stage('cheackout'){
        steps{
          git branch:'master',url:'https://github.com/Yoganand30/Mymavenpra.git'
        }
      }
        stage('Build"){
          steps{
            sh 'mvn compile package'
          }
              }
              stage('test'){
                steps{
                  sh 'mvn test'
                }
              }
                    stage('run application'){
                      steps{
                        sh 'java -jar target/Mymavneapp-1.0-SNAPSHOT.jar'
                      }
                    }
              }
                    post{
                         success{
                           echo 'build &deploye successsfully'
                         }
                      failure{
                        echo 'failed'
                      }
                    }
                    }
                         
