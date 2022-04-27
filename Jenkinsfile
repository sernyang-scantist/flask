
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
                script {
                    if (env.BRANCH_NAME == null) {
                        env.BRANCH_NAME = "N.A."
                    }
                    if (env.TAG_NAME == null) {
                        env.TAG_NAME = "ANOTHER DIFFERENT THING"
                    }
                    if (env.GUARANTEED_NOT_TO_EXIST == null) {
                        env.GUARANTEED_NOT_TO_EXIST = "1111pajfpjsapjzvl"
                    }
                    if (env.GIT_COMMIT == null) {
                        env.GIT_COMMIT = "Whoopdeod"
                    }
                }
                echo "BRANCH_NAME = ${env.BRANCH_NAME}"
                
                echo "TAG_NAME = ${env.TAG_NAME}"
                
                //sh 'export BRANCH=${BRANCH_NAME:-\"N.A.\"}'
                //sh 'echo "$env.BRANCH"'
                echo "This is the git commit ${env.GIT_COMMIT}"
            }
        }
    }
}
