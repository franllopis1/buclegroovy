pipeline {
  agent any
  stages {
    stage('practica') {
      steps {
        script {
          //crear variable que contiene el archivo
          def bucle = readYaml (file: 'release.yaml')
          //Determina que tipo de datos es, en este caso es un Map
          println bucle.getClass().getName()
          //Determino que archivo editar y donde esta la informacion
          bucle.setProperty("APP_JAVA_INT","1.1.5")
          bucle.each{key,value->
            println "La version de " + key + " es " + value
          }
        }
      }
    }
  }
}