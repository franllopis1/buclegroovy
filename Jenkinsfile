pipeline {
  agent any
  stages {
    stage('practica') {
      steps {
        script {
          //crear variable que contiene el archivo
          def release = readYaml (file: 'release.yaml')
          println release.getClass().getName()
          bucle.each{k,v->
            println "La version de " + k + " es " + v
          }
        }
      }
    }
  }
}