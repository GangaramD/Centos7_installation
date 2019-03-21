pipeline {
    agent any

   stages {
       stage(" Building the Maven Dependecy libraries") 
            {
         steps{
                echo " Hi This a Test mail from Jenkinsfile"   
              }
           }
   }
   post {
        always {

            emailext attachLog: true, body: '''${PROJECT_NAME} - Build # ${BUILD_NUMBER} - ${BUILD_STATUS}.<br/>
<br/>
Check console <a href="${BUILD_URL}">Console Output</a> to view full results.<br/>
If you cannot connect to the build server, check the attached logs.<br/>
<br/>
--<br/>
Following is the last 100 lines of the log.<br/>
<br/>
--LOG-BEGIN--<br/>
<pre style=\'line-height: 22px; display: block; color: #333; font-family: Monaco,Menlo,Consolas,"Courier New",monospace; padding: 10.5px; margin: 0 0 11px; font-size: 13px; word-break: break-all; word-wrap: break-word; white-space: pre-wrap; background-color: #f5f5f5; border: 1px solid #ccc; border: 1px solid rgba(0,0,0,.15); -webkit-border-radius: 4px; -moz-border-radius: 4px; border-radius: 4px;\'>
${BUILD_LOG, maxLines=100, escapeHtml=true}
</pre>
--LOG-END--''', mimeType: 'text/html', subject: '[${BUILD_STATUS}] - ${PROJECT_NAME} - Build # ${BUILD_NUMBER} (${BUILD_ID})', to: 'abc@gmail.com'
        }
      } 
 }
