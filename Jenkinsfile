pipeline {
 agent any
parameters{
//these are types of parameters
string(name: 'VERSION',defaultValue:'', description: 'version to deploy on prod')
choice (name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description:'')
booleanParam(name:'executeTests', defaultValue: true, description:'')}
 stages {
 stage('Build') {
 steps {
 echo 'Building..'

 // Here you can define commands for your build
 }
 }
 stage('Test') {
  when {
expression {
params.executeTests
}}
 steps {
 echo 'Testing..'
 // Here you can define commands for your tests
 }
 }
 stage('Deploy') {
 steps {
  
 echo 'Deploying....'
 // Here you can define commands for your deployment
 }
 }
 }
 post {
// the conditions here will execute after the build is done

always {

//this action will happen always regardless of the result of build
echo 'Post build condition running'
}
failure {
//this action will happen only if the build has failed
echo 'Post Action if Build Failed'
}
}
}
