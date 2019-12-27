node('master') {
    stage('Checkout') {
        checkout scm
    }
    
    stage('Run tests') {
        try {
            sh 'ls -lR'
            echo 'Clean and compile...'
            sh './mvnw clean compile'
            echo 'Clean and compile executed'
            sh 'ls -lR'
        } finally {
            archiveArtifacts 'target/**'
        }
    }
}
