node{
	stage('SCM Checkout'){
	git 'https://github.com/maulanadsgn/my-maven.git'
	}
	stage('Compile-Package'){
	sh 'mvn package'
	}
        stage('Build') {
        sh 'mvn -B -DskipTests clean package'
        }
        stage('Test') {
        sh 'mvn test'
	}
}
