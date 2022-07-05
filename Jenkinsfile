pipeline
{

agent any
stages

{ 
    stage ('scm checkout')
    {
        steps { git branch: 'master', url: 'https://github.com/Ranvijay7492/Ant-WebProject/' }
    }

    stage ('ant-prepare-target')
    {
        steps { withAnt(installation: 'LocalAnt', jdk: 'local_JDK') 
        {
          sh 'ant prepare'
        }     }
    }

    stage ('ant-init-target')
    {
        steps 
         { withAnt(installation: 'LocalAnt', jdk: 'local_JDK') 
           {
               sh 'ant init'
           }  }
    }

}


}
