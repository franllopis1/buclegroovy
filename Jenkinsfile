pipeline {
  agent any
  stages {
    stage('practica') {
      steps {
        script {
          //crear variable que contiene el archivo
          def bucle = readYaml (file: 'release.yaml')
          println bucle.getClass().getName()
          bucle.each{key,value->
            println "La version de " + key + " es " + value
          }
        }
      }
    }
  }
}