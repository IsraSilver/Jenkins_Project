# Jenkins_Project
Project for Jenkins end Git

Brief description of the script:

pipeline {                                                                                      #This is a pipeline script
    agent any                                                                                   #running on any nodes.
    parameters {                                                                                #The project includes several parameters.
        choice(
            name: 'MyLang',                                                                     #name of variable
            choices: "All\nBash\nPython\nC",                                                    #All parameters.
            description: 'Chose the language you mostly dislike')
    }
    stages {
        stage('Python') {                                                                       #Stage of Pyton parameter
            when {
                expression { params.MyLang == 'Python' || params.MyLang == 'All'}               #If parameter "Pyton" or choice from GitHub
            }
            steps {
                echo 'Python'                                                                   #screen "Pyton"
            }
        }
        stage('Bash') {                                                                         #Stage of Bash parameter
            when {
                expression { params.MyLang == 'Bash' || params.MyLang == 'All'}                 #If parameter "Bash" or choice from GitHub
            }
            steps {
                echo 'Bash'                                                                     #screen "Bash"
            }
        }
        stage('C') {                                                                            #Stage of C parameter
            when {
                expression { params.MyLang == 'C' || params.MyLang == 'All'}                    #If parameter "C" or choice from GitHub
            }
            steps {
                echo 'C'                                                                        #screen "C"
            }
        }
  
    }
}
111
