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
            steps{
                tools {
                    jdk 'JDK_17_UBUNTU'
                }
            }
        }            
        stage('package'){
            steps{
                
            }
        }
            }
        }
    }

}