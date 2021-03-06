# Change Log

## 3.1.7

* Ignored `ebs_block_device` changes on workers.  This is to preserve backwards compatibility for swarms that were built without the EBS swap space.
* Increased limits to support Elasticsearch Docker images in [production mode](https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html#docker-cli-run-prod-mode) by default.  Also set the requirements for the [file descriptors](https://www.elastic.co/guide/en/elasticsearch/reference/current/file-descriptors.html).
* simple example exposes only one EIP.

## 3.1.6

* Ignored `ebs_block_device` changes on managers.

## 3.1.5

* Use Amazon DNS server
* Allow outbound traffic from Docker security group to other hosts on the VPC

## 3.1.4

* Use an EBS volume to hold the swap rather than a swap file.

## 3.1.2 (2019-09-03)

* Add support to have different instance types for workers and managers.
* Documented how to change the docker version being used.
* Added `aws_s3_bucket_public_access_block` to prevent public access.
* Added `create_daemon_certificate_request` variable to control whether CSRs should be created.

## 3.1.1 (2019-09-02)

* Use amazon-extras for epel.

## 3.1.0 (2019-09-02)

* Add support for putting in a symlink for the key and certificate files for the `daemon_private_key_pems`, `daemon_cert_pems` and `daemon_ca_cert_pem`.

## 3.0.0 (2019-07-13)

* Migrated to Terraform 0.12
