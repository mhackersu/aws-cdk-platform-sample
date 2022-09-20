# Sample AWS Platform with CDK

Completed:

- [x] CDK Bootstrap & Init
- [x] [Infra Strategy](https://github.com/aws-samples/aws-cdk-examples/tree/master/typescript/ecs/fargate-service-with-local-image) (Fargate, ECS)
- [x] Project Refinements (Organizing code blocks)

Next steps
- [ ] [Docker Image Build & Publish]
  - **Notes:**
  - [Kaniko](https://aws.amazon.com/blogs/containers/building-container-images-on-amazon-ecs-on-aws-fargate/)
  - **Options:**
  - CI platform with hosted build agent
  - CI env itself (nested Dockerfile) if it's sometime a bit more adhoc.

Buiid Notes:
- For AWS ECR things, we will have to deal with creds.
- For a S3 route, we'll need to pass along metadata.
- For both routes, we'll need to think about naming and prefixes and suffixes.
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
- Running nested Dockerfiles with localcdk
