[![Build Status](https://travis-ci.org/denis-yuen/icy-blackberry.svg?branch=master)](https://travis-ci.org/denis-yuen/bug-free-potato)

# icy-blackberry
Example for the CFI presentation

## Usage

Use handy [quick start tutorial](https://github.com/ngs-docs/2017-cloud-workflows-misc/blob/master/install-and-run-with-dockstore.md) to setup our dependencies

### Run with cwltool

```
cwltool --non-strict Dockstore.cwl params.cwl.local.json
```

### Run with Cromwell

Download from https://github.com/broadinstitute/cromwell/releases (test with a newer release)

```
java -jar /home/dyuen/.dockstore/libraries/cromwell-0.21.jar run Dockstore.wdl params.wdl.json
```

### Run with Dockstore (consult launch-with)

Setup permissions for file destinations in Dockstore.json 


```
dockstore tool launch --entry quay.io/denis_yuen/icy-blackberry:1.1 --json params.cwl.local.json
dockstore tool launch --entry quay.io/denis_yuen/icy-blackberry:1.1 --json dockstore.cwl.remote.json
```

```
dockstore tool launch --entry quay.io/denis_yuen/icy-blackberry:1.1 --descriptor wdl --json params.wdl.json
dockstore tool launch --entry quay.io/denis_yuen/icy-blackberry:1.1 --descriptor wdl --json params.wdl.json --wdl-output-target s3://oicr.temp
```
