User data is data that is supplied by the [[IAM user]] at instance launch in the form of a [[script]].

*   The code is run when the instance starts for the **first time**.
*   Batch and PowerShell scripts can be run on Windows.
*   Limited to 16 KB.
-   User data and [[metadata]] are not encrypted.

## Examples

##### HTML: The Instance ID of this Amazon EC2 instance is: <*correct Instance ID*>
#code #html #bash

The following code,
1. declares, that this code is a bash script,
2. updates the OS with patches,
3. installs a webserver,
4. starts the webserver,
5. configure the service to start when the system boots,
6. finds out the instance ID and record it in the variable `EC2ID`,
7. takes the variable and puts it into some text (HTML Code should show a Text that says "The Instance ID of this Amazon EC2 instance is: *correct Instance ID*"),
8. changes the variable and saves the text to the index.html file.

```bash
#!/bin/bash
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
EC2ID=$(curl -s http://169.254.169.254/latest/meta-data/instance-id)
echo '<center><h1>The Instance ID of this Amazon EC2 instance is: EC2ID </h1></center>' > /var/www/html/index.txt
sed "s/EC2ID/$EC2ID/" /var/www/html/index.txt > /var/www/html/index.html
```

