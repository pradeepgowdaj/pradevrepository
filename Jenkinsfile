node
{
    stage "1. update the system/machine"
    sh "sudo yum update -y"
    
    stage "2. Install java on mentioned machine"
    sh "sudo yum install -y java"
    
    stage "3. create a folder"
    sh "mkdir -p marketing"
    
    stage "4. create file"
    sh "touch index.html"
    
    stage "5. add the content to the file"
    writeFile file:"marketing/output.txt", text:"this is the outputfile created"
    
    stage "6. show the status"
    echo "show the status of the files"
    
    stage "7. view date and time and uptime"
    sh "date"
    sh "uptime"
    sh "free -m"
    sh "df -h"
    sh "ls -al"
}
