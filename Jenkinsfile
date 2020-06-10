pipeline {
  agent any
  stages {
      stage('npm') {
steps{
script{
    echo %WORKSPACE%
sh 'cd webui'
   sh 'pwd'
sh 'npm install' 
    sh 'ng build --prod --aot=true'
    sh 'cd ..'
}
}
}

      
      
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

  
