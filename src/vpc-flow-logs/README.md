# Coralogix-VPC-Flow-Logs

This application retrieves **VPC Flow** logs from S3 and sends them to your **Coralogix** account.

It requires the following parameters:
* **S3BucketName** - The name of the `S3` bucket storing the **VPC Flow logs**.
* **ApplicationName** - A mandatory metadata field that is sent with each log and helps to classify it.
* **CoralogixRegion** - Possible values are `Europe`, `Europe2`, `US`, `Singapore` or `India`. Choose `Europe` if your Coralogix account URL ends with `.com`, `US` if it ends with `.us` and `India` if it ends with `.in`. This is a **Coralogix** parameter and does not relate to your to your AWS region.
* **PrivateKey** - Can be found in your **Coralogix** account under `Settings` -> `Send your logs`. It is located in the upper left corner.
* **SubsystemName** - A mandatory metadata field that is sent with each log and helps to classify it.

`S3KeyPrefix` and `S3KeySuffix` should be adjusted based on your configuration.

Do not change the `FunctionMemorySize` and `FunctionTimeout` parameters. The application should be installed in the same AWS region as the S3 archive's bucket.

## License

This project is licensed under the Apache-2.0 License.