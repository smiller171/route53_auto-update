route53_auto-update
===================

Automatically update a route53 entry at init.

To make these scripts work for you you need to make a few edits:
First, Add your Hosted_Zone ID in dyndns_route53.py
Then enter the domain name that you want kept up-to-date

I highly suggest storing dyndns_route53.py in S3 or somewhere where your instance can easily download it.

Edit user-data to point at the location of dyndns_route53.py
The contents of this file go in the user-data field when spinning up an instance or setting up an auto-scaling rule.
	
If you are going to be using the IAM role I provided you need to edit it to point at the correct hosted-zone
I will likely expand this role in a future update to grant permissions to the python script in S3. Right now I have that script set as public.
	
Credits for dyndns_route53.py go to @mariocesar His original gist can be found here: https://gist.github.com/mariocesar/4142563
