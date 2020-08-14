node {

 def mvnhome
        stage('SCM Checkout'){
          git 'https://github.com/siddhantika/hello-world.git' //checkout
          
        }
        stage('Compile Stage') {

                mvnhome = tool 'M2_HOME'
                echo mvnhome
         
               withMaven(maven: 'M2_HOME') {
                sh "'${mvnhome}bin/mvn' clean package install"
         }
        }
             
}
}
