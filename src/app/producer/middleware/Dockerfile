FROM public.ecr.aws/lambda/nodejs:16 as builder
WORKDIR /usr/src/app/producer/middleware
COPY package.json  ./
RUN npm install
COPY index.ts ./
RUN npm run build-middleware
    
FROM public.ecr.aws/lambda/nodejs:16
WORKDIR ${LAMBDA_TASK_ROOT}
COPY --from=builder /usr/ssrc/app/producer/middleware/dist/* ./
CMD ["index.backend"]
