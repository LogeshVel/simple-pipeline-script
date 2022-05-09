pipeline {
    agent {
        label "ubuntu"
    }
    environment {
            def myString = "Hello World"
            def myNumber = 10
            def myBool = true
        }
    stages{
        stage("Node Info") {
            steps {
                echo "Node name $NODE_NAME and the labels: $NODE_LABELS"
            }
        }
        stage("Basic shell cmds") {
            steps {
                executeBasicShellCmds()
            }
        }
        stage("Variables") {
            steps {
                echo "myString: ${myString}"
                echo "myNumber: ${myNumber}"
                echo "myBool: ${myBool}"
            }
            
        }
        stage("Simple function"){
            steps{
                func2("Printing some stuffs")
            }
        }
    }
}

def executeBasicShellCmds(){
    sh """
    pwd
    ls -a
    uname
    whoami
    
    """
}

def func2(String text){
    echo "${text}"
}
