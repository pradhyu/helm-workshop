# Helm Workshop: Microsoft Reactor, 2018

The purpose of this workshop is to learn how to build new Helm 2 charts.

## Workshop Format

This workshop is split into numbered sections outlined below:
1. [Getting Started](01-getting-started/)
1. [Charts](02-charts/)
1. [Subcharts](03-subcharts/)
1. [Templating](04-templating/)

## Goal

Our goal for this workshop is to create a Helm chart that takes Docker's popular [voting app demo](https://github.com/dockersamples/example-voting-app) and installs it in a Kubernetes cluster.

We will start with a simple chart, and then add from there.

Our application will have five parts:

1. A front-end for users to vote
1. A back-end that tallies votes
1. An admin interface to see the results
1. A Redis cache
1. A PostgreSQL database

### Quick Reference

In this guide, we will be building a chart based on a sample voting app. Here are the images you will need:

- `redis:alpine` - The Redis server for a work queue
- `postgres:9.4` - The persistent data storage
- `dockersamples/examplevotingapp_result:before` - The admin viewer
- `dockersamples/examplevotingapp_vote:before` - The voting frontend
- `dockersamples/examplevotingapp_worker` - The queue worker
