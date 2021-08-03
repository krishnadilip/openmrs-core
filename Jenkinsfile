node('ubuntunodeforgol') {
    stage('openmrsbuild') {
        git 'https://github.com/krishnadilip/openmrs-core.git'
    }
    stage('build') {
        sh 'mvn clean package'
    }
    stage('postbuild') {
        junit '**/TEST-*.xml'
        archive '**/*.war'
    }
}
