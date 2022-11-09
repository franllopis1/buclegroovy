pipeline {
  agent any
  stages {
    stage('practica') {
      steps {
        script {
          //Creo variable para almacenar el archivo
          def archivo = 'release.yaml'
          //crear variable que contiene el archivo
          def bucle = readYaml (file: 'release.yaml')

          println archivo
          println bucle
          //Determina que tipo de datos es, en este caso es un Map
          println bucle.getClass().getName()
          //Determino que archivo editar y donde esta la informacion
          writeYaml file: archivo, data: bucle
          assert bucle.0 == '1'
          bucle.each{key,value->
            println "La version de " + key + " es " + value
          }
        }
      }
    }
  }
}