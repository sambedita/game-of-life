node('REDHAT'){
    stage('scm'){
        git 'https://github.com/wakaleo/game-of-life.git'
        

    }

    stage('build'){
        sh 'mvn package'

    }

    stage('postbuild'){
        junit 'gameoflife-web/target/surefire-reports/*.xml'
        archiveArtifacts artifacts: 'gameoflife-web/target/*.war'

    }

}
