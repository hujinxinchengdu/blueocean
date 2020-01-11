pipeline{
	agent any
	stages{
		stage('Upload to AWS') {
			steps {
				withAWS(region:'us-west-1', credentials:'71f35cb7-d728-4b26-bc2c-fec02864e34f'){
					sh 'echo "Hello World with AWS"'
					s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html',bucket:'blueoceantestingweb')
				}
			}
		}
	}
}