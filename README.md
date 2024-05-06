# terramodule
ec2-instance-creation-module

provider "aws" {
  region = "ap-south-1"
}

module "ec2-instance" {
  source = "https://github.com/shahidkkn/terramodule.git" 
  ami_id = "ami-041d6256ed0f2061c"
  instance_type = "t2.micro"
  vpc_id = "vpc-03fc242a1657c826c"
  port = "80"
  cidr_block = "0.0.0.0/0"
}
