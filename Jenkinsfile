PASTEBIN
API
TOOLS
FAQ
paste
Search...

LOGIN SIGN UP
Advertisement

SHARE
TWEET
Guest User
Untitled
A GUEST
JUN 6TH, 2023
10
0
NEVER
ADD COMMENT
Not a member of Pastebin yet? Sign Up, it unlocks many cool features!
 2.13 KB | None |  
     
/* groovylint-disable DuplicateStringLiteral, NoDef */
// HELPERS AND CONSTANTS
/*def suiteMap = []
def getHashmapKeys(map) {
    def list = []
    map.keySet().each {
        list << it
    }
    return list
}
 
def getPlansNames(map) {
    def list = []
    map.keySet().each {
        list << "${it} Automation"
    }
    return list
}
def getTestsSummary(file="results/${REPORT_ID}-test-output.xml") {
    def awkCommand = { position -> "awk -F \'\"\' \'NR==2 {print \$${position}}\' ${file}" }
    def failuresCount = sh(script:"${awkCommand(8)}", returnStdout:true)
    def totalCount = sh(script:"${awkCommand(6)}", returnStdout:true)
    def passedCount = sh(script:"echo \$((${totalCount}-${failuresCount}))", returnStdout:true)
    return [totalCount: totalCount, failuresCount: failuresCount, passedCount: passedCount]
}
 
def secrets = []
 
def plansList = getPlansNames(suiteMap)
 
// ENVIRONMENT VARIABLES BLOCK FOR TESTRAIL
    env.TESTLINK_SUITE_ID = suiteMap."${params.TESTLINK_SUITE_NAME}"
    env.TESTLINK_ENABLED = params.TESTLINK_ENABLED
    env.TESTLINK_PROJECT_NAME = "TestProject"
    env.TESTLINK_PLAN_NAME = params.TESTLINK_PLAN_NAME
*/
//
 
 
pipeline {
    agent any
    environment {
        DOCKER_IMAGE_TAG = "${env.BRANCH_NAME}-${env.BUILD_NUMBER}"
    }
    stages {
        // build
        stage('Initial stage') {
            steps {
                dir('docker_introduction/docker-compose/') {
                    script {
                        sh("docker-compose build --build-arg DOCKER_IMAGE_TAG=${DOCKER_IMAGE_TAG}")
                    }
                }   
 
            }
        }
 
        // launch app
        stage('Launch application') {
            steps {
                dir('docker_introduction/docker-compose/') {
                    script {
                        sh("docker-compose up -d")
                    }
            }   
 
            }
        }
 
        // run tests
 
        stage('Run tests') {
            steps {
                script {
                    sh("echo 'hello'")
 
                }
 
            }
        }
    }
    post {
        always {
                 dir('docker_introduction/docker-compose/') {
                    script {
                        sh("docker-compose down")
                }
            }
        }
    }
}
 
Advertisement

Add Comment
Please, Sign In to add comment
Advertisement
Public Pastes
Untitled
JavaScript | 2 min ago | 9.72 KB
Query 4 - Update table, delete records, tempo...
SQL | 18 min ago | 0.97 KB
SQL QUERY
MySQL | 18 min ago | 6.68 KB
BTC Wallet Credentials have been reset
GetText | 26 min ago | 0.23 KB
Simple Tic-Tac-Toe (Java)
Java | 35 min ago | 4.83 KB
testwaz
PowerShell | 42 min ago | 0.30 KB
Query 3 - Filters (=, LIKE, IN, %, AND, BETWE...
SQL | 1 hour ago | 1.96 KB
data595
JSON | 1 hour ago | 0.64 KB
Advertisement
create new paste  /  syntax languages  /  archive  /  faq  /  tools  /  night mode  /  api  /  scraping api  /  news  /  pro
privacy statement  /  cookies policy  /  terms of serviceupdated  /  security disclosure  /  dmca  /  report abuse  /  contact

By using Pastebin.com you agree to our cookies policy to enhance your experience.
Site design & logo © 2023 Pastebin
We use cookies for various purposes including analytics. By continuing to use Pastebin, you agree to our use of cookies as described in the Cookies Policy.  OK, I Understand
Not a member of Pastebin yet?
Sign Up, it unlocks many cool features! 
