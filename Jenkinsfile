node {

 def mvnhome
        stage('SCM Checkout'){
          git 'https://github.com/siddhantika/hello-world.git' //checkout
          
        }
        stage('Compile Stage') {

                mvnhome = tool 'M2_HOME'
                echo mvnhome
         
               withMaven(maven: 'M2_HOME') {
                sh "'${mvnhome}/bin/mvn' clean package install"
                
         }
        }
 stage('deployment'){
  sshPublisher(publishers: [sshPublisherDesc(configName: 'jenkins-deploy-tomat', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: '', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '', remoteDirectorySDF: false, removePrefix: '/webapp/target', sourceFiles: '**/*.war')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
 }
             
}

