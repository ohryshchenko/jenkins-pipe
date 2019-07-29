pipeline {
    agent any
    tools {
        maven 'Maven 3.3.9'
        jdk 'jdk8'
    }

    stages {
stage ("initialize") {
steps {
sh '''
echo "PATH = ${PATH}"
echo "M2_HOME = ${M2_HOME}"
'''
      }
                      }
            }

stage ('Clone') {
git url: 'https://github.com/ohryshchenko/spring-boot-master.git'
}

stage ('Test') {
       rtMaven.run pom: 'maven-example/pom.xml', goals: 'clean test'
   }

stage ('Build project') {
steps {
dir("spring-boot-tests/spring-boot-smoke-tests/spring-boot-smoke-test-web-ui/"){
    sh 'mvn clean verify




    }
}
}
}
