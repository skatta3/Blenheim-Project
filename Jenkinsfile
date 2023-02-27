node {
    stage('Github')     {
      git branch: 'master', url: 'https://github.com/daticahealth/java-tomcat-maven-example.git'        
    }
    stage('Package')   {
        sh 'mvn package'       
    }
    stage('Archive') {
        archiveArtifacts artifacts: 'target\\java-tomcat-maven-example.war', followSymlinks: false
    }
    stage('Email') {
        mail bcc: '', body: 'My Build Job is Success', cc: '', from: '', replyTo: '', subject: 'Test Email', to: 'skatta3@yahoo.com'
    }
}