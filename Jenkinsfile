pipeline{
    agent any
    stages {
        stage('prepare Artifacts') {
            steps {
                sh '''
                zip -r todo.zip *
            '''
            }
        }
        stage('upload Artifacts') {
            steps {
                sh '''
		             	curl -f -v -u admin:kavya --upload-file todo.zip http://172.31.6.66:8081/repository/todo/todo.zip
		       	'''
                }
            }
        }
    }