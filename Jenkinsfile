node('GOI'){
    stage('scm'){
        git "https://github.com/kavyasree-ops/spring-petclinic.git"
    }
    stage('build'){
        sh label: '', script: 'mvn clean package'
    }
    stage('postbuild'){
        archiveArtifacts 'spring-petclinc-web/target/*.war'
    }
}