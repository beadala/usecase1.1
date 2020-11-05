pipeline {
  agent {label "master"}
stages {  
stage('Test') {
steps {
sh '/usr/local/bin/cfn-lint ./*.yml'
}
}
stage('Deploy') {
steps {
sh 'cd /usr/local/bin/'
sh 'ls'
sh "/usr/local/bin/aws cloudformation create-stack --stack-name StageLambda --template-body file://forgit.yml --region 'ap-southeast-2'"
}
}
}
}