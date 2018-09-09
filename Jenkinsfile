node {

    try {
        stage('Pull sources') {
            checkout scm
        }

        stage('Run tests') {
            sh './junit clean test'
        }
    } catch (ex) {
        echo "Caught: ${ex}"
        currentBuild.result = 'UNSTABLE'
    }
}