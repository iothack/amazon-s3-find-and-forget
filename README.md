# Amazon S3 Find and Forget

> Warning: This project is currently in beta and should not be used for
> production purposes.

![Unit Tests](https://github.com/awslabs/amazon-s3-find-and-forget/workflows/Unit%20Tests/badge.svg)

Amazon S3 Find and Forget is a solution to the need to selectively erase records
from data lakes stored on Amazon Simple Storage Service (Amazon S3). This
solution can assist data lake operators to handle data erasure requests, for
example, pursuant to the European General Data Protection Regulation (GDPR).

The Amazon S3 Find and Forget solution can be used with Parquet-format data
stored in Amazon S3 buckets. Your data lake is connected to the solution via an
AWS Glue table and specifying which columns in the table contain user
identifiers.

Once configured, you can queue record identifiers that you want the
corresponding data erased for. You can then run a deletion job to remove the
data corresponding to the records specified from the objects in the data lake. A
report log is provided of all the S3 objects modified.

The solution provides a web user interface, and a REST API to allow you to
integrate it in your own applications.

## Documentation

- [User Guide](docs/USER_GUIDE.md)
- [Deployment](docs/USER_GUIDE.md#deploying-the-solution)
- [Architecture](docs/ARCHITECTURE.md)
- [Troubleshooting](docs/TROUBLESHOOTING.md)
- [Monitoring the Solution](docs/MONITORING.md)
- [Security](docs/SECURITY.md)
- [Cost Overview](docs/COST_OVERVIEW.md)
- [Limits](docs/LIMITS.md)
- [API Specification](docs/api/README.md)
- [Local Development](docs/LOCAL_DEVELOPMENT.md)
- [Change Log](CHANGELOG.md)

## Contributing

Contributions are more than welcome. Please read the
[code of conduct](CODE_OF_CONDUCT.md) and the
[contributing guidelines](CONTRIBUTING.md).

## License Summary

This project is licensed under the Apache-2.0 License.
