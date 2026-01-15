pipeline {
  agent any
  stages {
    stage('Inicio') {
      steps {
        echo 'INICIO'
        bat 'echo Inicio: %DATE% %TIME%'
      }
    }

    stage('Logs') {
      parallel {
        stage('p1') {
          steps {
            echo 'P1 - Generando log 1'
          }
        }

        stage('p2') {
          steps {
            echo 'P2 - Generando log 2'
          }
        }

      }
    }

    stage('Fin') {
      steps {
        echo 'FIN - Verificando resultados'
      }
    }

  }
}