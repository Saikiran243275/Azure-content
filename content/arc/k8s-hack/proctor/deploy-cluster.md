Ensure that you are in a tenant without a policy restricting the creation of a public IP address

Set a DNS name of the VM based upon `md5sum <<< $RG_ID ~ cut -c1-8`