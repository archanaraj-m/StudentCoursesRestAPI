pipeline{
    agent{ label('bucket')}
    trigger{
        POLLSCM(' * * * * * ')
    }
    stages{ 
        stage('vcs'){
            steps {
                git url: 'https://github.com/archanaraj-m/StudentCoursesRestAPI.git', 
                    branch: 'studentdocker'
            }
        }
        stage('build'){
            tools {
                jdk 'JDK_17_UBUNTU'
            }
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

