pipeline {
  agent any
  stages {
    stage('ConstruyendoAPP') {
      steps {
        echo 'Paso1: Construyendo la App'
        sh 'sh run_build_script.sh'
      }
    }

    stage('Prueba Linux') {
      steps {
        echo 'Paso1: Realizando Prueba en Linux'
        sh 'sh run_linux_test.sh'
      }
    }

    stage('Test Manual') {
      steps {
        echo 'Esperando la confirmacion manual'
        input 'Está todo Ok para desplegar'
        timestamps() {
          echo 'Momeno de confirmacion del Ok Mnaual'
        }

      }
    }

    stage('Desplieqgue en Prod') {
      steps {
        echo 'Desplegando en Produccion'
      }
    }

  }
}