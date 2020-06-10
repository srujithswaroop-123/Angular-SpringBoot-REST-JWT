pipeline {
  agent any
  stages {
      stage('npm') {
steps{
    script{
sh 'java -jar ./target/app-1.0.0.jar stop'
}
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
sh 'java -jar ./target/app-1.0.0.jar'
}
}
}
}
}

  
