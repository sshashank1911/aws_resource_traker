# aws_resource_traker
#shell scripting example project

#!/bin/bash

#########################
#
# Author: Shashank
# Date: 13/05/25
#
# Version: v1
#
# This script will report the AWS resource usage
###########################

set - x

# AWS s3
#  AWS ec2
#  AWS lambda
#  AWS IAM users


# list s3 buckets
echo "print list of s3 buckets"
aws s3 ls

#list ec2 instances
echo "print list of ec2 instances"
aws ec2 describe-instances | jq '.Reservations[].Instances[].InstanceId'

# list lambda
echo "print list of lambda functions"
aws lambda list-functions

#list IAM users
echo "print list of IAM users"
aws iam list-usersws_resource_traker.sh                                   
