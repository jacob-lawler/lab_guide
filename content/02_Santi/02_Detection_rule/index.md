## Application Detection Rule API

1. Open  <a href="https://www.dynatrace.com/support/help/dynatrace-api/configuration-api/rum/application-detection-configuration/post-rule" target="_blank">Application detection rule API</a> documentation

2. Go back to terminal and run dt api kit:

    ```javascript
    node index.js
    ```

3. Choose *Create a app detection rule*

4. ```
   Choose an application for the detection rule: Sockshop (Production)
   Do you want to match Domain or URL? URL
   Choose one rule: CONTAINS
   What does the "URL" should match "CONTAINS"?: <your Sockshop front-end external IP saved before>   

    ```
   If you don't have the URL, go to the bastion terminal and run: 

   ```
   kubectl get services -o wide --namespace production
   ```
   
   And copy front-end url adding HTTP://<your external-ip>:8080

    ![appDetect](../../assets/images/appDetect.png)

5. Go to history.log and verify your deployment