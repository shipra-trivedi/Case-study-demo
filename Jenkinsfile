@Library('newlib@main')_
pipeline {
       agent any
       stages{
        stage("demo") {
             steps {
            sayHello 'Kirti'
                       }
                      }
        stage("readfile")
        {
            steps
            {
              
               readFilecode 'C:/Users/User/.jenkins/workspace/Case study/Hello.csv'
                                      
            }
        }
       }
       post {
        always {
           // emailext body: '${env.BUILD_URL} has result ${currentBuild.result}', subject: 'test email', to: 'shipratrivedi1234@gmail.com'
            mail to: 'shipratrivedi1234@gmail.com',
          subject: "Status of pipeline: ${currentBuild.fullDisplayName}",
          body: "${env.BUILD_URL} has result ${currentBuild.result}"
        }
    }
}
