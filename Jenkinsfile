pipeline
{
  agent any
  stages
  {

    stage('Build')
    {
      steps
      {
        build 'PES2UG21CS030-1' 
        sh 'g++ test.cpp -o output'
      }
    }

    stage('Test')
    {
      steps
      {
        sh './output'
      }
    }
    stage('Deploy')
    {
      steps
      {
        echo 'deploy'
      }
    }
  }

  post
  {
    failure
    {
      error 'Pipeline failed'
    }
  }
}
