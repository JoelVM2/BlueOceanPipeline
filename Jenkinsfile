pipeline {
  agent any
  stages {
    stage('Inicio') {
      steps {
        echo 'INICIO'
        bat 'echo Empezando pipeline'
      }
    }

    stage('Sistema') {
      steps {
        echo 'SISTEMA'
        bat 'echo %DATE% %TIME%'
      }
    }

    stage('Aprobacion') {
      steps {
        input(message: '¿Continuar a FIN?', ok: 'Continuar')
      }
    }

    stage('Fin') {
      steps {
        echo 'FIN'
        bat '''echo FIN: empezando 
                    FIN: fecha y hora -> %DATE% %TIME%  
                    FIN: terminado'''
      }
    }

  }
}