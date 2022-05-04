# Code Pipeline Slack Notifier
```bash
git clone code-pipeline-slack-notifier
cd code-pipeline-slack-notifier
git checkout 057c6af02cd0464092c9f9ddebd7bb968f4e7ae9
```

Edit sar.yaml and update node version to node12.x

$ npm install

$ npm run dist

$ aws cloudformation package --template-file sam.yaml --s3-bucket YOUR_S3_BUCKET --output-template-file target/packaged-template.yaml

$ aws cloudformation deploy --template-file ./target/packaged-template.yaml --stack-name cp-slack-notifier --parameter-overrides SlackUrl=YOUR-INCOMING-WEBHOOK-URL --capabilities CAPABILITY_IAM

