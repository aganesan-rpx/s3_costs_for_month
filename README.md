# AWS S3 Bucket Size and Cost for month
This Python script fetches metrics for AWS S3 buckets, including size, cost estimation, and file count, and exports the data to a CSV file.

### Installation
1. Install the required Python libraries using pip:
    ```
    pip install boto3
    ```

2. Ensure you have configured AWS credentials properly using AWS CLI or IAM roles.

### Usage
1. Replace the placeholders in the code with your AWS credentials and desired AWS region.
2. Ensure that the necessary permissions are granted to access CloudWatch metrics and S3 buckets.
3. Run the script.
4. After execution, a CSV file named `s3_cost_details.csv` will be generated with the collected metrics data.

### Code Documentation
The provided Python script performs the following tasks:

1. Imports necessary libraries: `boto3`, `botocore`, `datetime`, and `csv`.
2. Initializes AWS clients for S3 and CloudWatch.
3. Lists all S3 buckets in the AWS account.
4. Defines start and end times for fetching metrics (in this case, for February).
5. Iterates over each bucket to retrieve metrics.
6. Queries CloudWatch for bucket size and number of objects metrics.
7. Calculates size in gigabytes,megabytes, cost estimation, and file count.
8. Writes the collected metrics data to a CSV file named `s3_cost_details.csv`.

The script catches exceptions and prints errors if any occur during execution.

### Notes
- Ensure that the AWS credentials used have appropriate permissions to access CloudWatch metrics and S3 buckets.
- This script assumes standard storage for S3 buckets and calculates cost estimation based on it.
- Modify the file name (`s3_cost_details.csv`) or file path as needed.

