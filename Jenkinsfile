pipeline {
  agent any
  stages {
    stage('maven build') {
      steps {
script{
sh 'mvn clean install'
}
}
}
stage('jar') {
steps{
script{
sh 'java -jar ./target/app-1.0.0.jar'
}
}
}
}
}

  
