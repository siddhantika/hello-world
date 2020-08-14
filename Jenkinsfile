node {

 def mvnhome
        stage('SCM Checkout'){
          git 'https://github.com/siddhantika/hello-world.git' //checkout
          
        }
        stage('Compile Stage') {
            
            
                mvnhome = tool 'M2_HOME'/bin/mvn
                echo mvnhome
                echo 'hello' 
             
}
}
