node('kubeslave') {
    stage('Checkout') {
        checkout scm
    }
    
    stage('Run tests') {
        try {
            withMaven(maven: 'Maven 3') {
                sh './mvnw clean compile'
            }
        } finally {
            archiveArtifacts 'target/**'
        }
    }
}
