pipeline {
    agent any
    parameters {
        choice(
            name: 'MyLang',
            choices: "All\nBash\nPython\nC",
            description: 'Chose the language you mostly dislike')
    }
    stages {
        stage('Python') {
            when {
                expression { params.MyLang == 'Python' || params.MyLang == 'All'}
            }
            steps {
                echo 'Python'
            }
        }
        stage('Bash') {
            when {
                expression { params.MyLang == 'Bash' || params.MyLang == 'All'}
            }
            steps {
                echo 'Bash'
            }
        }
        stage('C') {
            when {
                expression { params.MyLang == 'C' || params.MyLang == 'All'}
            }
            steps {
                echo 'C'
            }
        }
  
    }
}
