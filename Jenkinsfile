pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('mensaje') {
      steps {
        echo 'hola mundo'
      }
    }
    stage('clean') {
      steps {
        sh '''echo "-------------------------------------------------------------------------------"
echo "  CLEAN     ::     Clean the environment"
echo "-------------------------------------------------------------------------------"

echo " ::: .----------------.  .----------------.  .----------------.  .----------------.  .-----------------."
echo " :::| .--------------. || .--------------. || .--------------. || .--------------. || .--------------. |"
echo " :::| |     ______   | || |   _____      | || |  _________   | || |      __      | || | ____  _____  | |"
echo " :::| |   .\' ___  |  | || |  |_   _|     | || | |_   ___  |  | || |     /  \\     | || ||_   \\|_   _| | |"
echo " :::| |  / .\'   \\_|  | || |    | |       | || |   | |_  \\_|  | || |    / /\\ \\    | || |  |   \\ | |   | |"
echo " :::| |  | |         | || |    | |   _   | || |   |  _|  _   | || |   / ____ \\   | || |  | |\\ \\| |   | |"
echo " :::| |  \\  .___. \\  | || |   _| |__/ |  | || |  _| |___/ |  | || | _/ /    \\ \\_ | || | _| |_\\   |_  | |"
echo " :::| |    ._____.   | || |  |________|  | || | |_________|  | || ||____|  |____|| || ||_____|\\____| | |"
echo " :::| |              | || |              | || |              | || |              | || |              | |"
echo " :::| \'--------------\' || \'--------------\' || \'--------------\' || \'--------------\' || \'--------------\' |"
echo " :::\'----------------\'  \'----------------\'  \'----------------\'  \'----------------\'  \'----------------\' "

x=5
while [ $x -gt 0 ]
do
sleep 1s
echo "$x Cleanning DUMP"
x=$(( $x - 1 ))
done    '''
      }
    }
    stage('') {
      steps {
        bat 'clean.cmd'
      }
    }
  }
}