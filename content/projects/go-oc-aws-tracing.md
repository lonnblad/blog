+++
title = "go-oc-aws-tracing"
date = "2023-09-23"
author = "Fredrik"
description = "go-oc-aws-tracing is a utility package to trace AWS requests and responses with OpenCensus."
+++

To be able to trace requests and responses to AWS services using OpenCensus, I wrote go-oc-aws-tracing.

This package will wrap the standard AWS Session, so it can be used as normal with the AWS SDK.

[Link to the project.](https://github.com/lonnblad/go-oc-aws-tracing)

```go
import aws_trace "github.com/lonnblad/go-oc-aws-tracing"
```

```go
cfg: = aws.NewConfig().WithRegion("us-west-2")
sess: = session.Must(session.NewSession(cfg))
sess = aws_trace.WrapSession(sess)

s3api: = s3.New(sess)
s3api.CreateBucket( & s3.CreateBucketInput {
    Bucket: aws.String("some-bucket-name"),
})
```
