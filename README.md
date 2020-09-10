# Iovio Challenge

## Task 1



## Task 4.1

filesize: 1.9GB (1.915.176.884 bytes)  
The text file is an edge list from a graph with 134.217.728 edges. 

### .zip
real time: 2m2.209s  
71% savings  
(in=1915176884) (out=562711360)  
This means it reduced the size of the file with an average of 11.066.824 bytes per second = 11.07MB/s

### .7z
real time: 21m25.612s  
76% savings  
out=455021733  
This means it reduced the size of the file with an average of 1.135.767 bytes per second = 1.14MB/s

### .lz
real time: 25m8.673s  
76.40% saved  
1915176884 in, 452044114 out.  
This means it reduced the size of the file with an average of 969.814 bytes per second = 0.97MB/s

### .gz
real time: 1m25.997s  
70.6% savings  
out=562711389  
This means it reduced the size of the file with an average of 15.726.891 bytes per second = 15.73MB/s

### .zstd
real	0m17.912s  
66.54% savings  
1915176884 => 640736568 bytes  
This means it reduced the size of the file with an average of 71.150.084 bytes per second = 71.15MB/s  

We can conclude that .zstd offers the most optimal time/compression ratio. 


## Task 4.2

To instatiate a computer in the Cloud I chose to use Terraform.  
This is a cloud automation and orchestration platform, that is particularly convenient if you are managing a large structure of cloud instances, load balancers etc.  

Setting up Terraform is quite easy. The website, [https://www.terraform.io](https://www.terraform.io), guides you right through it, and even has support for Windows. You download the file, set the path, and are ready for execution. 

If you want to create a EC2 instance in AWS from a image AMI, you create a .tf file, which contains with your AWS credentials, the type of instance you want to create and the AMI. The .tf file to create a resource with the name "example" could look something like this: 

```
provider "aws" {
  access_key = "ACCESS_KEY"
  secret_key = "SECRET_KEY"
  region     = "eu-west-1"
}

resource "aws_instance" "example" {
  ami           = "ami-08935252a36e25f85"
  instance_type = "t2.micro"
}
```

To start terraform in your directory you type `terraform init` and to apply the .tf code you just wrote you type `terraform apply` in your terminal. After that we have succesfully launched the aws instance. I used Terraform v0.11.13 + provider.aws v2.7.0.

