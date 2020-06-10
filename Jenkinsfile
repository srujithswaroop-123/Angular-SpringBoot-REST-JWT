pipeline {
  agent any
  stages {
      stage('npm') {
steps{
    
    dir('webui'){
        sh 'npm install'
        sh 'ng build --prod --aot=true' 
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
    sh 'sudo lsof -t -i:9119 > result'
    sh 'sudo kill -9 $result'
    sh 'java -jar ./target/app-1.0.0.jar'
}
}
}
}
}

  
