# WebSphere Application Server Installation on GCE

WAS on GCE for Ubunts installation notes

## Description
### Ubuntu Setup on GCE
```
gcloud beta compute instances create my-instance \
  --zone us-central1-a \
  --machine-type e2-medium \
  --scopes cloud-platform \
  --tags http-server \
  --image=ubuntu-2004-focal-v20210325 \
  --image-project=ubuntu-os-cloud \
  --boot-disk-size=10GB

gcloud compute firewall-rules create default-allow-http \
  --direction=INGRESS \
  --priority=1000 \
  --network=default \
  --action=ALLOW \
  --rules=tcp:80 \
  --source-ranges=0.0.0.0/0 \
  --target-tags=http-server
```

## Demo

## Features

- feature:1
- feature:2

## Requirement

## Usage

## Installation

## References

## Licence

Released under the [MIT license](https://gist.githubusercontent.com/shinyay/56e54ee4c0e22db8211e05e70a63247e/raw/34c6fdd50d54aa8e23560c296424aeb61599aa71/LICENSE)

## Author

[shinyay](https://github.com/shinyay)
