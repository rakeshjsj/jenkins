pipeline {
    agent none

    parameters {
        string(name: 'NAME', defaultValue: '', description: 'Please tell me you name?')
        booleanParam(name: 'SKIP_TEST', description: 'Want to skip test runs to direct deploy')
        choice(name: 'BRANCH', choices: ['master','stagging','prod'], description: '')
    }

    environment{
          user_name = 'rakesh'
          password = 'kjsjjsjsjs'

    }
    
    stages {
        stage{
            agent { label 'slave2' }


            steps {
                catchError(buildResult: 'SUCCESS',stageResult: 'FAILURE') {
                    echo "NAME: ${params.NAME}"
                    echo "SKIP_TEST: ${params.SKIP_TEST}"
                    echo "BRANCH TO DEPLOY: ${params.BRANCH}"
                    echo "user_name: ${env.user_name}"
                    echo "password: ${password}"

                    sh '''
                        exit 1
                }
               echo "NAME: ${params.NAME}"
               echo "SKIP_TEST: ${params.SKIP_TEST}"
               echo "BRANCH TO DEPLOY: ${params.BRANCH}"
               echo "user_name: ${env.user_name}"
               echo "password: ${password}"

               sh '''
                    echo "NAME: ${NAME}"
                    echo "SKIP_TEST: ${SKIP_TEST}"
                    echo "BRANCH TO DEPLOY: ${BRANCH}"
                    echo "user_name: ${user_name}"
                    echo "password: ${password}"
               '''
            }
        }
        stage('STAGE1') {
            
            agent { label 'slave1' }

            steps {
               echo "NAME: ${params.NAME}"
               echo "SKIP_TEST: ${params.SKIP_TEST}"
               echo "BRANCH TO DEPLOY: ${params.BRANCH}"
               echo "user_name: ${env.user_name}"
               echo "password: ${password}"

               sh '''
                    echo "NAME: ${NAME}"
                    echo "SKIP_TEST: ${SKIP_TEST}"
                    echo "BRANCH TO DEPLOY: ${BRANCH}"
                    echo "user_name: ${user_name}"
                    echo "password: ${password}"
               '''
            }
        }

               sh '''
                    echo "NAME: ${NAME}"
                    echo "SKIP_TEST: ${SKIP_TEST}"
                    echo "BRANCH TO DEPLOY: ${BRANCH}"
                    echo "user_name: ${user_name}"
                    echo "password: ${password}"
               '''
            }
        }
        
    }
}