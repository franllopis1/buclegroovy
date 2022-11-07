pipeline {
  agent any
  stages {
    stage('practica') {
      steps {
        script {
          //crear variable que contiene el archivo
          def bucle = readYaml (file: 'release.yaml')
          println bucle.getClass().getName()
          bucle.each{k,v->
            println "La version de " + k + " es " + v
          }
        }
      }
    }
  }
}