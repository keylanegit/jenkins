node {
 def remote = [:]
  remote.name = 'clibeal04'
  remote.host = 'clibeal04'
  remote.user = 'bea'
  remote.password = 'leanapps'
  remote.allowAnyHosts = true
  stage('Remote SSH') {
    sshCommand remote: remote, command: "ls -lrt"
    sshCommand remote: remote, command: "for i in {1..5}; do echo -n \"Loop \$i \"; date ; sleep 1; done"
  }
  try {
    stage('checkout') {
    echo "Version 2 start checkout..."
    input message: 'Geef tablenaam', 
    parameters: [string(defaultValue: 'paramWaarde', description: 'Waarde van Param1', name: 'param1', trim: false)]
    }
    stage('prepare') {
      echo "uploading package..."
    }
    stage('compile') {
      echo "nothing to compile for hello.sh..."
    }
    stage('test') {
      echo "uploading package..."
    }
    stage('package') {
       echo "uploading package..."
    }
    stage('publish') {
      echo "uploading package..."
    }
  } finally {
    stage('cleanup') {
      echo "doing some cleanup..."
    }
  }
}
