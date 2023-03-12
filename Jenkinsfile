pipeline{
    agent{ label('bucket')}
    triggers{
        pollSCM(' * * * * * ')
    }
    stages{ 
        stage('vcs'){
            steps {
                git branch: 'studentdocker',
                    url: 'https://github.com/archanaraj-m/StudentCoursesRestAPI.git'
            }        
        }
        stage('build'){
            steps {    
                sh 'docker image build -t archanaraj/spc:latest .'     
            }
        }    
        stage('scan and push'){
            steps{
               sh 'echo docker image scan archanaraj/spc:latest'
               sh 'echo docker image push archanaraj/spc:latest'
            }
        }
    }    
}

