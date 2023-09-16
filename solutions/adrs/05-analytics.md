# Traveler Analytics

Analytics used by the Road Warrior app to provide insights to the Road Warrior team.

## Status

Proposed

## Context

Analytics is a key component of the Road Warrior app. It provides insights to the Road Warrior team to help them improve the app and the services they provide.

## Decision

[Amazon SageMaker](https://aws.amazon.com/sagemaker/) will be used to provide analytics for the Road Warrior app.

It can provide the following:

* Data exploration
* Data visualization
* Machine learning
* Model training
* Model deployment

The analytical data gathered by the Road Warrior app will be stored in an [Amazon S3](https://aws.amazon.com/s3/) bucket. The data will be stored in a [Parquet](https://parquet.apache.org/) format.

## Consequences

There would be additional costs for using Amazon SageMaker. However, the insights provided by the analytics will help the Road Warrior team improve the app and the services they provide.
