node {
    stage 'Stage 1 - scm'
    echo 'Stage 1 - scm'
    checkout scm
    sleep 5
    stage 'Stage 2'
    stage 'Stage archiveArtifacts'
    archiveArtifacts 'TEST-*.xml'
    stage 'Stage test'
    sh 'touch *.xml'
    step([$class: 'JUnitResultArchiver', testResults: 'TEST-*.xml'])
}
