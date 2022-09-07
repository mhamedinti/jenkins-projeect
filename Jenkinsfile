node{
def app 
     
   stage('Clone') {
       checkout scm
   }
   stage('Bluid image') {
       app = docker.build("intissar/nginx")
   }
   stage('Run image') {
       docker.image('intissar/nginx').withRun('-p 83:80') { c ->
       sh 'docker ps'
       sh 'curl localhost'


   } 
   }
}
