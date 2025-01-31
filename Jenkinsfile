pipeline {
    agent any
    environment {
       python="'C:\\Program Files\\python313\\python.exe'"
    }
    stage('Build') {
        steps {
            bat "${python} code.py"
           }
        }
    
    stage('Test') {
        steps {
            dir("CalculatorTests"){
            bat "${dotnet} test"
           }
        }
    }
    stage('Clean') {
        steps {
           dir("Calculator"){
            bat "${dotnet} clean"
           }
            dir("CalculatorTests"){
            bat "${dotnet} clean"
           }
        }
    }
}
    
