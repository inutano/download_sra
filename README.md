# Download SRA

[![DOI](https://zenodo.org/badge/136470994.svg)](https://zenodo.org/badge/latestdoi/136470994)

A simple download tool to download `.sra` file from a repository of [INSDC](http://insdc.org) members.

## Why not `prefetch`?

Because we are living far away from Maryland. `download-sra` can choose a repository to be used.

## Prerequisites

- `wget`
- `curl`
- [`jq`](https://stedolan.github.io/jq/)

## Usage

```
$ download-sra SRR000001
$ download-sra SRR000001 NCBI
$ download-sra SRR000001 EBI
$ download-sra SRR000001 DDBJ
```

## Docker Container

Available on [Quay.io](https://quay.io/repository/inutano/download-sra)

```
$ docker run --rm -it -v $(pwd):/work -w /work quay.io/inutano/download-sra:0.1.2 download-sra "DRR000001" "NCBI"
$ docker run --rm -it -v $(pwd):/work -w /work quay.io/inutano/download-sra:0.1.2 download-sra "DRR000001" "EBI"
$ docker run --rm -it -v $(pwd):/work -w /work quay.io/inutano/download-sra:0.1.2 download-sra "DRR000001" "DDBJ"
```
