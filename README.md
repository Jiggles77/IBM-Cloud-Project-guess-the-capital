IBM-Cloud-Project-guess-the-capital

Cloud Computing Course hands-on project

Instructions:

Build Docker image:
cd /home/project/fyidw-guess-the-capital
docker build . -t us.icr.io/${SN_ICR_NAMESPACE}/guess-the-capital


Push the image to IBM Cloud:

docker push us.icr.io/${SN_ICR_NAMESPACE}/guess-the-capital

Deploy the image on IBM CE:

ibmcloud ce application create --name guess-the-capital --image us.icr.io/${SN_ICR_NAMESPACE}/guess-the-capital --registry-secret icr-secret --port 80

Take Cloud URL from the output; which looks something like: https://guess-the-capital.somerandomalphanumeric.us-south.codeengine.appdomain.cloud and open in your browser.

ibmcloud ce application get --name guess-the-capital

Proof of deployment:

https://guess-the-capital.1jkxykhqkt7d.us-south.codeengine.appdomain.cloud/

![image](https://github.com/user-attachments/assets/f58ea8d8-8cf0-4b8e-a3ed-3b30f959da7a)
