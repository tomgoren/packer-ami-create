# packer-ami-create
Repository for AMI creation with Packer

* Build AMI with: `packer build -var-file=CREDENTIALS.json  nginx-enabled-ami.json`.
* Requires `-var-file` parameter to be specified at runtime, 
  specifically for `aws_access_key` and `aws_secret_key`.
* `m3.medium` instance type was selected due to it being the 
  cheapest and smallest EC2 classic instance available (the modern t2 (micro/nano) series is VPC dependent).
* Provisions `nginx` and `ntp`.

