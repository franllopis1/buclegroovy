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
          def nombre = "APP_JAVA-INT"
          def version = "1.1.5"
          //Determino que archivo editar y donde esta la informacion
          bucle.each{key,value->
            println "La version de " + key + " antes era " + value + " ahora es " version
          }
          bucle.put(nombre, version)
          writeYaml file: 'release.yaml', data: bucle, overwrite: true

        }
      }
    }
  }
}