pipeline {
	agent any 
	stages{
		stage('git-clone'){
			steps{
				checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'Kinge-Service', url: 'https://github.com/Kinge-Service/jenkins-parallel-job.git']]])
			}
		}
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
				sh 'lscpu'
			}
		}
	}
}
