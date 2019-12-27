node('master') {
    stage('Checkout') {
        checkout scm
    }
    
    stage('Clean and Compile') {
        try {
            sh './mvnw clean compile'
        } finally {
            archiveArtifacts 'target/**'
        }
    }
}
