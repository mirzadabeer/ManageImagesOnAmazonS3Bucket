# Manage Images on Amazon S3 Bucket - Module for ProcessWire 3.x

This module/plugin provides a way to synchronize, serve and backup to Amazon S3 Bucket all the page images uploaded 
through the Admin of ProcessWire.

## Requirements

- ProcessWire 3.x;
- Amazon AWS PHP SDK (included);
- AWS account with S3 services enabled;
- A S3 Bucket and a user with the proper privileges over it: "s3:PutObject", "s3:GetObject", "s3:DeleteObject" and 
"s3:PutObjectAcl";

## Installation 

Put all the files inside /site/modules/ManageImagesOnAmazonS3Bucket/ and go to Admin>Modules>Refresh for New Modules and install. 

You'll need to configure the module by entering your AWS Access and Secret keys and the name of the S3 Bucket you'll 
use to store the images.

## How does it work

The module/plugin uploads the images to S3 immediately as you add them to the pages in the admin of ProcessWire. 
It mimics the PW asset structure inside the S3 Bucket you defined. (/S3BUCKET/PAGE_ID/images).

The deleted files on PW pages are also deleted immediately from S3 but you have the option to create a backup to another
 folder on S3 for backup purposes.

The module can automatically serve the content from Amazon CloudFront if a distribution is created for the S3 bucket used 
with this module. The files URL's are automatically replaced. 

## Issues

This version of the module will only handle new image uploaded after the installation. If you already have images on your 
pages they will not be uploaded to S3 and you can get errors because the files inside PW will not match the files on S3. 

## Notes

THIS PROCESSWIRE MODULE/ PLUGIN IS PROVIDED AS IS AND IT SHOULD ONLY BE USED FOR TEST PURPOSES. USE AT YOUR OWN RISK. 
THE AUTHOR IS NOT RESPONSIBLE FOR ANY DATA LOSSES OR COSTS ASSOCIATED WITH THE USE OF AMAZON AWS.

Copyright 2017 by Mirza Dabeer Hussain [E-mail](mailto:dabeer88@gmail.com)

Built for [ProcessWire](http://processwire.com/)