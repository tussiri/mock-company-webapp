  /*
   * TODO: Implement pipeline stages/steps
   *   See documentation: https://www.jenkins.io/doc/book/pipeline/syntax/#stages
   */
pipeline {
         agent any

         stages {
             stage('Checkout') {
                 steps {
                     checkout scm
                 }
             }

             stage('Set up JDK') {
                 steps {
                     sh 'java -version'
                 }
             }

             stage('Grant execute permission for gradlew') {
                 steps {
                     sh 'chmod +x gradlew'
                 }
             }

             stage('Build with Gradle') {
                 steps {
                     sh './gradlew assemble'
                 }
             }

             stage('Test with Gradle') {
                 steps {
                     sh './gradlew test'
                 }
             }
         }
     }