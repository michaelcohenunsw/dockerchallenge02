Example command to run aws cli inside a Docker container:

Change the values of environment variables AWS_DEFAULT_REGION, AWS_ACCESS_KEY_ID, and AWS_SECRET_ACCESS_KEY as required.

docker run --rm -it -e "AWS_DEFAULT_REGION=ap-southeast-2" -e "AWS_ACCESS_KEY_ID=KEYID" -e "AWS_SECRET_ACCESS_KEY=SECRETKEY" amazon/aws-cli:2.0.10 s3 ls

If you are running a Linux operating system you can create an alias to shorten this command:

$ alias aws='docker run --rm -it -e "AWS_DEFAULT_REGION=ap-southeast-2" -e "AWS_ACCESS_KEY_ID=KEYID" -e "AWS_SECRET_ACCESS_KEY=SECRETKEY" amazon/aws-cli:2.0.10'

aws s3 ls
