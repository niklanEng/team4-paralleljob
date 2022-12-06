pipeline{
	agent {
		label 'slave1'
	}
	stages{
		stage('1-clonecode'){
			steps{
				sh 'action1'
			}
		}
		stage('2-codebuild'){
			agent {
				label 'slave2'
			}
			steps{
				sh 'action2'
			}
		}
		stage('3-unittest'){
			steps{
				sh 'mvn test'
			}
		}
		stage('4-mutationtest'){
			agent {
				label 'slave3'
			}
			steps{
				sh 'mvn pit:test'
			}
		}
	}
}
