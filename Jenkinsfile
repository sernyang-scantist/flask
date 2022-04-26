
// declarative

pipeline {
    agent {
        label 'slave'
    }

/* 
POSTREF just realised there's an entire commented section 
in the file that seems to be the answer...?
*/

    stages {
        stage('Install black'){
            // assume pip installed and updated? or attempt to update pip
            // POSTREF changed pip to pip3
            steps{
                sh 'pip3 install black'
            }
        }

        stage('Run black'){
            // run on.. what?
            // POSTREF does jenkinsfile run "in" the repository it's placed in?
            // POSTREF but then how do you run shell commands?
            // need docker build push?
            // my own github fork of flask i suppose?
            steps{
                sh 'black .'
            }
        }
        stage("Env Variables"){
            steps{
                sh "printenv"
                echo "This is the branch ${BRANCH_NAME:-N.A.}"
                echo "This is the tag ${TAG_NAME:-N.A.}"
                echo "This is the git commit ${GIT_COMMIT:-N.A.}"
                echo "This is the build ID ${BUILD_ID:-N.A.}"                                               
            }
        }
    }
}
