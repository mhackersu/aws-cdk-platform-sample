# Sample AWS Platform with CDK

Completed:

- [x] CDK Bootstrap & Init
- [x] [Infra Strategy](https://github.com/aws-samples/aws-cdk-examples/tree/master/typescript/ecs/fargate-service-with-local-image) (Fargate, ECS)
- [x] Project Refinements (Organizing code blocks)

Next steps
- [ ] [Docker Image Build & Publish]
  - This might make the most sense use a CI platform with either a hosted build agent or the CI env itself if it's sometime a bit more adhoc.

https://aws.amazon.com/blogs/containers/building-container-images-on-amazon-ecs-on-aws-fargate/)

Buiid Notes:
- For AWS ECR things, we will have to deal with creds.
- For a S3 route, we will have to build locally first; We'll need to pass along metadata.
- Might lean here to use an hosted build agent for reasons related to signed provenance.

# Thinking about CDK

### From a DevX Perspective
- Engineering enthusiasm!
- Enabling and empowering the developer!
- Helps with the onboarding process!

### From an Ops Perspective
- How much time will be spent with runtime debugging headaches?
- What ongoing meta-responsibilities will be involved for DevOps?
- How maintainable is the app's CDK code?
- How many programming languages are DevOps engineers expected to know?

# Thinking about AdHoc things
- Handle AWS sandbox account provisioning and deprovisioning
- Building and running Dockerfiles inside Dockerfiles with localcdk
