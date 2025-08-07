# Ansible Role: minio-docker

![Ansible Galaxy](https://img.shields.io/badge/Ansible--Galaxy-minio-blue?style=flat-square)


## Description

This Ansible role installs **MinIO** on Docker container.

---

## Features

- Install MinIO server on Docker container
- Automatically create bucket list

---

## Supported Platforms

- Ubuntu 20.04+
- Debian 11+

---

## Example Usage

```yaml
- hosts: all
  become: true
  roles:
    - role: evertonagilar.docker-tls
    - role: evertonagilar.minio-docker
      vars:
        minio_image: minio/minio:latest
        minio_user: minioadmin
        minio_password: minioadmin
        bucket_list:
          - mybucket
          - mybucket2
```