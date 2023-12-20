pipeline{
	agent any 
	stages{
		stage('1-action1'){
			steps{
				checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'jenkins-access', url: 'https://github.com/ArmandTeam8/jenkins2.git']])
			}
		}
		stage('2-action2'){
			steps{
				sh 'df -h'
			}
		}
		stage('3-action3'){
			steps{
				sh 'lsblk'
			}
		}
		stage('4-action4'){
			steps{
				sh 'lscpu'
			}
		}
        stage('5-welcome message'){
            steps{
                echo 'welcome to Etech team8 jenkins'
            }
        }
        stage('6-securitycheck'){
            steps{
                sh "bash -x /var/lib/jenkins/workspace/jenkins-demo3/script.sh"
            }
        }
	}
}