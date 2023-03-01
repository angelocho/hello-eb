pipeline {
    agent any
    options{
        timestamps()
        ansiColor('xterm')
    }
    stages {
        stage('Building Elastic Beanstalk') {
            steps {
               withAWS(credentials:'clave-aws') {
                   dir("elasticfolder"){
                     sh 'eb create dev-env'
                    }
               }
            }
        }
    }
}
