pipeline{
    tools{
        jdk 'JAVA_HOME'
        maven 'M2_HOME'
    }
    agent { label 'windows'}
    
    stages{
        
        stage("checkout"){
            steps{
                git 'https://github.com/Bishnuprasadswain/jenkins-repo.git'
            }
        }
        stage("compile"){
            steps{
                bat 'mvn compile'
            }
        }
        stage("test"){
            steps {
                bat 'mvn test'
            }
        }
		stage("package") {
            steps {
                bat 'mvn package'
            }
        }
    }
}
