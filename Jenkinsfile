node('master'){
    stage('Git pull'){
        //clone into current directory so we can run jenkins script
        git(
          url: "git@github.com:shydrate/testgit.git",
          //credentialsId: 'wardanceferret_github',
          branch: "dev"
        )
    }
    
    stage('List'){
        sh 'ls -la; pwd'
    }
}
