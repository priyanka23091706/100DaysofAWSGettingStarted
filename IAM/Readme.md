https://docs.aws.amazon.com/cli/latest/userguide/cli-services-iam-new-user-group.html

## Create Group
aws iam create-group --group-name MyIamGroup

## Create User 
aws iam create-user --user-name MyUser

## Add user to group 
aws iam add-user-to-group --user-name MyUser --group-name MyIamGroup

## Create User with Power user policy 
export POLICYARN=$(aws iam list-policies --query 'Policies[?PolicyName==`PowerUserAccess`].{ARN:Arn}' --output text)       ~
echo $POLICYARN

## Attach policy to user 
aws iam list-attached-user-policies --user-name MyUser

## Create access keys 
aws iam create-access-key --user-name MyUser

## Delete access keys 
aws iam delete-access-key --user-name MyUser --access-key-id AKIAIOSFODNN7EXAMPLE

## Create policy 
aws iam create-policy --policy-name my-policy --policy-document file://policy

## Attach policy to a group 
aws iam attach-group-policy --policy-arn arn:aws:iam::aws:policy/ReadOnlyAccess --group-name Finance

## Create Role 
aws iam create-role --role-name Test-Role --assume-role-policy-document file://Test-Role-Trust-Policy.json
# find the Trust policy sample file 

## Get user 
aws iam get-user --user-name Paulo

## Add role to instance profile 
aws iam create-instance-profile --instance-profile-name Webserver

aws iam add-role-to-instance-profile --role-name S3Access --instance-profile-name Webserver

aws ec2 associate-iam-instance-profile --instance-id i-123456789abcde123 --iam-instance-profile Name=Webserver

