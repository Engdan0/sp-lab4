pipeline {
	agent any

	stages {
		stage('Checkout') {
			steps {
				git url: 'https://github.com/Engdan0/sp-lab4.git', credentialsId: 'credentialsId'
			}
		}
		stage('Build') {
			steps {
				script {
					bat '"D:\\Programming\\VS studio\\MSBuild\\Current\\Bin\\MSBuild.exe" vovchenko-test.sln /p:Configuration=Debug /p:Platform=x64 /m'
				}
			}
		}
		stage('Test') {
			steps {
				script {
					bat '"E:\\Study\\kursova\\lab4\\vovchenko-test\\x64\\Debug\\vovchenko-test.exe"'
				}
			}
		}
	}
	post {
		always {
			cleanWs()
		}
	}
}