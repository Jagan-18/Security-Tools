
## Trivy:
•	Trivy is an open-source security scanner designed to detect vulnerabilities in containers and other artifacts. It utilizes an internal database known as trivy-db, which houses detailed information about various vulnerabilities.
•	It is developed and maintained by AquaSecurity
•	Trivy not only scans for vulnerabilities but also provides suggestions for resolving the issues and links to detailed information about the vulnerabilities.
•	Trivy can access extensive vulnerability information from various databases and utilizes this data to identify security issues. Among the databases it draws from are the National Vulnerability Database (NVD), Red Hat Security Data, and Alpine SecDB.
•	During a scan, Trivy compares the software packages and libraries in a directory or container image with its vulnerability database. If a match is found, indicating a vulnerability, Trivy reports the issue along with details such as severity level, affected versions, and recommended fixes.
•	Trivy updates its database every six hours. When you initiate a scan, Trivy automatically updates the database, eliminating the need for you to manually track updates



## Trivy shows the risk of vulnerability as critical, high, medium, and low.
  1. Critical – This is the most severe vulnerability which needs to be fixed as soon as possible because it can allow administrative control over the system.
  2. High – It could cause data leakage. 
  3. Medium – It could make the system unavailable for users.
  4. Low – This can be solved during regular maintenance.


# We can use Trivy to scan the following targets:
    1. Container images
    2. Filesystem
    3. Remote Git repositories
    4.Virtual Machine Image
    5. Kubernetes
    6. AWS






### Trivy Install Steps:

# Refel URL : https://aquasecurity.github.io/trivy/v0.18.3/installation/
 ```bash
 - sudo apt-get install wget apt-transport-https gnupg lsb-release
 - wget -qO - https://aquasecurity.github.io/trivy-repo/deb/public.key | sudo apt-key add -
 - echo deb https://aquasecurity.github.io/trivy-repo/deb $(lsb_release -sc) main | sudo tee -a /etc/apt/sources.list.d/trivy.list
 - sudo apt-get update
 - sudo apt-get install trivy -y
 - trivy --version
```
 # To scan the Git Reop
==> trivy repo <github-url>

==> trivy image [image_name]


# To enable only vulnerability scanning, you can specify — scanners vuln.
1. $ trivy image --scanners vuln [image_name]
    Ex: $ docker pull nginx:alpine3.17
# Scan commands:
$ trivy image nginx:alpine3.17


# sample script if you want to automate the scan:
  ```bash
     #!/bin/bash 
     trivy image rabbitmq:3.9 > rabbitmq-results.txt
      trivy image nginx:alpine3.17 > nginx-results.txt
   ```
