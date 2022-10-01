pipeline {
	agent any 
	stages{
		stage('parallel-stage'){
			parallel{
				stage('parallel-job1'){
					steps{
						echo "action1"
					}
				}
				stage('parallel-job2'){
					steps{
						echo "action2"
					}
				}
			}
		}
		stage('parallel-stage2'){
			parallel{
				stage('parallel-job3'){
					steps{
						echo "action3"
					}
				}
				stage('parallel-job4'){
					steps{
						echo "action4"
					}
				}
			}
		}
		stage('code-build'){
			steps{
				sh 'cat /etc/os-release'
			}
		}
	}
}
