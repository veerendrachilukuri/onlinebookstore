node{
    stage('clone'){
        git branch: 'feature/2026.10.14', credentialsId: 'jenkinscredentials', url: 'https://github.com/veerendrachilukuri/onlinebookstore.git'
    }
    stage('build'){
        bat 'mvn install'
    }
    stage('generate artifacts'){
        archiveArtifacts artifacts: 'target/*.war', followSymlinks: false
    }
}