pipeline {
    agent any

    stages {
        stage('Get') {
            steps {
                git 'https://github.com/Unsam98/Jenkins.git'
            }
        }
        stage('Compile') {
            steps {
               bat '''
               javac -cp "C:\\Users\\UncleSam\\.m2\\repository\\junit\\junit\\4.12\\junit-4.12.jar";"C:\\Users\\UncleSam\\.m2\\repository\\org\\hamcrest\\hamcrest-core\\1.3\\hamcrest-core-1.3.jar";. "Student.java" "studentTest.java"
               '''
            }
        }
        stage('Test') {
            steps {
               bat '''
               java -cp "C:\\Users\\UncleSam\\.m2\\repository\\junit\\junit\\4.12\\junit-4.12.jar";"C:\\Users\\UncleSam\\.m2\\repository\\org\\hamcrest\\hamcrest-core\\1.3\\hamcrest-core-1.3.jar";. org.junit.runner.JUnitCore "studentTest"
               '''
            }
        }
    }
}