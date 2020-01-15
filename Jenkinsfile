node{
	stage('SCM Checkout'){
	git 'https://github.com/maulanadsgn/my-maven.git'
	}
	stage('Compile-Package'){
	sh 'mvn package'
	}
	stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }

}
