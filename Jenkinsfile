pipeline {
  agent any 
  stages{
    stage('1.checkout') {
      steps{
        git url: 'https://github.com/Kp29-gitty/Docker', branch:'main'
      }
    }
    stage('2.Build Image') {
      steps{
        bat 'docker build -t Myweb .'
    }
    }
    satge ('3.Stop/Remove old Containers') {
      steps{ 
        bat 'docker stop mycont || exit 0'
        bat 'docker rm mycont|| exit 0'
    
  }
  } 
    stage('4.Run the Image- Containerize') {
      steps {
        bat 'docker run -d -p 50000:80 --name mycont Myweb'
    
  }
} 
  }
}
