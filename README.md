# Integrating the Stripe Payment Processing Service

## Overview

This project is a Spring Boot application that integrates the Stripe payment processing service to manage customer data upon user signup. It leverages the Temporal Workflow Engine for orchestrating business logic.

## Setup

1. Clone the repository from GitHub.
2. Navigate to the project directory.
3. Run the setup commands (provide the specific commands here).

## Stripe Integration

This application integrates the Stripe Create Customer API to create a new customer in Stripe upon a new user signup. The Stripe SDK is used for this purpose. The process is managed by a workflow implemented using the Temporal Workflow Engine.

## API Fields

The user model includes a `providerType` field with an enum type with the value `stripe`, and a `providerId` field to store the generated Stripe customer ID. The application controller has been updated to handle these new fields and ensure that the `providerId` is generated and stored correctly during the user signup process.

## API Implementation

A GET /accounts endpoint is implemented to verify the integration and functionality of the changes.

## Testing

Tests have been written for the Stripe integration and the new fields in the user model, as well as integration tests that cover the signup process and the GET /accounts endpoint functionality.
