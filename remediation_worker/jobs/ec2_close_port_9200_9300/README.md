# Close Port 9200, 9300 for all Security Groups associated with an EC2 Instance

This job blocks public access to port 9200, 9300 for both IPv4 and IPv6 for all security groups associated with an EC2 instance by removing all the ingress security group rules containing port 9200, 9300 in the port range and source as "0.0.0.0/0" or "::/0".

### Applicable Rule

##### Rule ID:
04700175-adbe-49e1-bc7a-bc9605597ce2

##### Rule Name:
EC2 instance should restrict public access to Elasticsearch ports (9200 and 9300)

## Getting Started

### Prerequisites

The provided AWS credential must have access to `ec2:DescribeInstances`, `ec2:RevokeSecurityGroupIngress`, `ec2:DescribeSecurityGroupRules`.

You may find the latest example policy file [here](minimum_policy.json)

### Running the script

You may run this script using following commands:
```shell script
  pip install -r ../../requirements.txt
  python3 ec2_close_port_9200_9300.py
```

## Running the tests
You may run test using following command under vss-remediation-worker-job-code-python directory:
```shell script
    python3 -m pytest
```

## Contributing
The Secure State team welcomes welcomes contributions from the community. If you wish to contribute code and you have not signed our contributor license agreement (CLA), our bot will update the issue when you open a Pull Request. For any questions about the CLA process, please refer to our [FAQ](https://cla.vmware.com/faq).
All contributions to this repository must be signed as described on that page. Your signature certifies that you wrote the patch or have the right to pass it on as an open-source patch.

For more detailed information, refer to [CONTRIBUTING.md](../../../CONTRIBUTING.md).

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/vmware-samples/secure-state-remediation-jobs/tags).

## Authors

* **VMware Secure State** - *Initial work*

See also the list of [contributors](https://github.com/vmware-samples/secure-state-remediation-jobs/contributors) who participated in this project.

## License

This project is licensed under the Apache License - see the [LICENSE](https://github.com/vmware-samples/secure-state-remediation-jobs/blob/master/LICENSE.txt) file for details
