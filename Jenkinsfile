node {  
    stage('clone code') {
        git 'https://github.com/vamshi-psy/test.git'
    }
    stage('build') { 
        bat 'mvn clean install package'
    }
    stage('Deploy') { 
        deploy adapters: [tomcat8(credentialsId: 'tomcat', path: '', url: 'http://localhost:8090/')], contextPath: null, war: '**/*.war'
    }
}
