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
          //Determina que tipo de datos es, en este caso es un Map
          println bucle.getClass().getName()
          //Determino que archivo editar y donde esta la informacion
          writeYaml overwrite: true, file: archivo, data: bucle
          assert bucle.APP_JAVA-INT == 1.1.5
          println bucle
          bucle.each{key,value->
            println "La version de " + key + " es " + value
          }
        }
      }
    }
  }
}