pipeline {
    agent any

    options {
        timestamps()
        buildDiscarder(logRotator(numToKeepStr: '5', daysToKeepStr: '2', artifactDaysToKeepStr: '', artifactNumToKeepStr: ''))
    }

    parameters {
        string(name: 'rg_name', defaultValue: "", description: "Enter resource group name")
        string(name: 'az_location', defaultValue: "", description: "The location for azure vm")
        string(name: 'vm_name', defaultValue: "", description: "Name of VM")
        string(name: 'vm_admin_username', defaultValue: "", description: "")
        string(name: 'adm_pwd', defaultValue: "", description: "The admin password")
        string(name: 'svc_pwd', defaultValue: "", description: "The password")
        choice(name: 'vm_size', choices: ['DSeriesv2', 'DSeriesv4', 'UAT', 'PROD'], description: 'Passing the Size')
        choice(name: 'vm_image', choices: ['DCWindowsServer2019', 'OpsWindowsServer2019', 'Windows10'], description: 'Passing the Image')
    }

    stages {
        stage(' ') {
            steps {
                script {
                    echo "$rg_name $az_location $vm_size"
                    echo "ls"
                }
            }
        }
    }
}
