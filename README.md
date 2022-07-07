# Udacity CloudDevOps Engineering

## CC6-L4-C28: Exercise: Promote to Production

Please reference docs folder for additional documentation.

### Solution Folder Structure

```folder-structure
├── bucket.yml          # Creates a new bucket and bucket policy.       
├── cloudfront.yml      # Creates a Cloudfront Distribution that will connect to the new bucket created above.
├── index.html  
└── .circleci
  └── config.yml
```

### Shell Scripts

From root folder

```shell
aws cloudformation deploy --template-file cloudfront.yml --stack-name production-distro --parameter-overrides PipelineID="mybucketname"
```

### Solution Reference

[udacity/nd9991-c3-hello-world-exercise-solution](https://github.com/udacity/nd9991-c3-hello-world-exercise-solution)
