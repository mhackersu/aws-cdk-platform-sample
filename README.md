# Sample AWS Platform with CDK

Completed:

- [x] CDK Bootstrap & Init
- [x] [Infra Strategy](https://github.com/aws-samples/aws-cdk-examples/tree/master/typescript/ecs/fargate-service-with-local-image) (Fargate, ECS)
- [x] Project Refinements (Organizing code blocks)

Next steps
- [ ] [Docker Image Build & Publish (*This makes most sense to do from a CI platform with either a hosted build agent or the CI env itself if it's an adhoc CI env.)]

https://aws.amazon.com/blogs/containers/building-container-images-on-amazon-ecs-on-aws-fargate/)

Buiid Notes:
- For AWS ECR things, we will have to deal with creds.
- For a S3 route, we will have to build locally first; We'll need to pass along metadata.
- Might lean here to use an hosted build agent for reasons related to signed provenance.
