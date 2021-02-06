node('nodes')
{
    def mavenHome = tool name: "maven3.6.3"
		stage('CheckoutCode')
		{
			git branch: 'development', credentialsId: '4943ad49-0209-4148-b4e6-e5d220fe970f', url: 'https://github.com/rahulnr-1/maven-web-application.git'
		}
		stage('Build')
		{
			sh "${mavenHome}/bin/mvn clean package"
		}
		/*
		stage('ExecuteSonarQubeReport')
		{
		    sh "${mavenHome}/bin/mvn sonar:sonar"
		}
		stage('UploadArtifactIntoNexus')
		{
		    sh "${mavenHome}/bin/mvn deploy"
		}
		stage('DeployApplicationIntoTomcatServer')
		sshagent(['b1e3cbe7-995d-4196-8220-a880bc362e4e']) {
        sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@52.66.119.33:/opt/apache-tomcat-9.0.41/webapps"
}
        stage('SendEmailNotification')
        {
           mail bcc: 'rahulsia362@gmail.com', body: '''Build Over...


Regards.
Rahul NR
DevOps Engineer
8123673106''', cc: 'rahulsia362@gmail.com', from: '', replyTo: '', subject: 'Build over', to: 'rahulsia362@gmail.com' 
        }
	*/
}
