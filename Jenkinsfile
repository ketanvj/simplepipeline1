pipeline {
   agent any
   
   environment {
       DEMO='1.6'
   }

   stages {
      stage('build') {
         steps {
            echo "This is build number $BUILD_NUMBER of demo $DEMO"
            sh '''
               echo "Using a multi-line shell step"
               chmod +x build.sh
               ./build.sh
            '''
         }
      }
         stage('test') {
         steps {
            echo "This is build number $BUILD_NUMBER of demo $DEMO"
            sh '''
               echo "Using a multi-line shell step"
               chmod +x test.sh
               ./test.sh
            '''
         }   
      }
   }
}
