🚀 Building AMIs on AWS with Packer and Ansible: Streamlining Nginx Deployment! 🌐
I’m excited to share my recent journey of leveraging HashiCorp Packer and Ansible to automate the creation of an Amazon Machine Image (AMI) with Nginx pre-installed. This process not only simplified my deployment workflow but also ensured consistency across environments.

Here’s how I did it:
1. Creating the Packer Template: I started by defining a Packer template in JSON format. This template specifies the base AMI, the provisioning steps, and the necessary configurations.<img width="1440" height="900" alt="Screenshot 2025-09-25 at 23 39 30" src="https://github.com/user-attachments/assets/fbdb5c97-aef8-4d94-91bd-ce62d0d08bb0" />

2. Using Ansible for Nginx Installation: I wrote an Ansible playbook (nginx.yml) that automates the installation and configuration of Nginx. This ensures that the web server is properly set up every time the AMI is built.

   <img width="1439" height="452" alt="Screenshot 2025-09-25 at 23 42 21" src="https://github.com/user-attachments/assets/65462bd2-b031-4e5e-8afe-a60872759aa2" />
   
3. Building the AMI: With the Packer template and Ansible playbook ready, I executed the build command to create the AMI. This process launches an EC2 instance, runs the Ansible playbook, and captures the image.

   packer build nginx.json

   <img width="1419" height="861" alt="Screenshot 2025-09-25 at 22 59 35" src="https://github.com/user-attachments/assets/a964216c-8045-46bb-af1a-d72440a61c63" />
   <img width="1158" height="157" alt="Screenshot 2025-09-25 at 23 01 09" src="https://github.com/user-attachments/assets/7b9296f2-1f6c-403f-8732-26e11cc0e636" />


4. Running the Instance: After successfully creating the AMI, I used the AWS CLI to launch a new instance from the AMI, applying necessary tags for better management.


<img width="1421" height="233" alt="Screenshot 2025-09-25 at 23 26 24" src="https://github.com/user-attachments/assets/40d097bd-831d-420b-ac31-bcb1e7766390" />

<img width="1429" height="602" alt="Screenshot 2025-09-25 at 23 27 00" src="https://github.com/user-attachments/assets/7f3244a1-9141-4ba2-9b82-5722ea9ccdbe" />


This experience has highlighted the power of automation in cloud deployments. By combining Packer and Ansible, I can ensure that my infrastructure is not only reliable but also scalable.

