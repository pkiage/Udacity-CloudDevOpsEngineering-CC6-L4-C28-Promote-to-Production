# Udacity CloudDevOps Engineering

## CC6-L4-C28: Exercise: Promote to Production

Please reference docs folder for additional documentation.

### Task List

- [ ] Create a Public S3 Bucket with a Home Page
- [ ] Create a CloudFront Distribution for the Bucket
- [ ] Modify Home Page
- [ ] Write a Job to Create a New S3 Bucket and Copies Files
- [ ] Write a Job that Gets the Previous Pipeline ID
- [ ] Write a Job that Modifies the CloudFront Distro's Origin Bucket to OUr New Bucket
- [ ] Write a Job that Kills the Old Bucket and Stack
- [ ] Define a Workflow that Puts These Jobs In Order
- [ ] Verify The Modified Home Page is Browsable

### Solution Folder Structure

```folder-structure
├── bucket.yml          # Creates a new bucket and bucket policy.       
├── cloudfront.yml      # Creates a Cloudfront Distribution that will connect to the new bucket created above.
├── index.html  
└── .circleci
  └── config.yml
```

### Make S3 Bucket Public

[How to create public AWS S3 bucket](https://www.simplified.guide/aws/s3/create-public-bucket)

Bucket policy:

```json
{
    "Version":"2012-10-17",
    "Statement":[
     {
       "Sid":"AddPerm",
       "Effect":"Allow",
       "Principal": "*",
       "Action":["s3:GetObject"],
       "Resource":["arn:aws:s3:::mybucketname/*"]
     }
    ]
}
```

### Shell Scripts

From root folder

```shell
aws cloudformation deploy --template-file cloudfront.yml --stack-name production-distro --parameter-overrides PipelineID="mybucketname"
```

### Solution Reference

[udacity/nd9991-c3-hello-world-exercise-solution](https://github.com/udacity/nd9991-c3-hello-world-exercise-solution)
