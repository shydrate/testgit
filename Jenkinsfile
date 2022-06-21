node('master'){
    environment {
    FULL_PATH_BRANCH = "${sh(script:'git name-rev --name-only HEAD', returnStdout: true)}"
    GIT_BRANCH = FULL_PATH_BRANCH.substring(FULL_PATH_BRANCH.lastIndexOf('/') + 1, FULL_PATH_BRANCH.length())
    }
    
    stage('Git pull'){
        //clone into current directory so we can run jenkins script
        git(
          url: "git@github.com:shydrate/testgit.git",
          //credentialsId: 'wardanceferret_github',
          branch: env.GIT_BRANCH
        )
    }
    
    stage('List'){
        sh 'ls -la; pwd'
    }
}
