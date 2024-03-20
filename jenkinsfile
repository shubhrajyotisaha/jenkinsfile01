pipeline{
    tools
    {
        maven 'mymaven'
    }
    agent any
    stages
   {
       stage('clone_code')
       {
           steps{
               git 'https://github.com/shubhrajyotisaha/DevOpsCodeDemo.git'
               }
       }
       stage('compile_code')
       {
           steps
           {
               sh 'mvn compile'
           }
       }
       stage('code_review')
       {
           steps
           {
               sh 'mvn pmd:pmd'
           }
       }
       stage('test_code')
       {
           steps
           {
               sh 'mvn test'
           }
       }
              stage('build_code')
       {
           steps
           {
               sh 'mvn package'
           }
       }
   }
}
