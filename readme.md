## Overview
Understanding how to build conditional workflows using AWS Step Functions.

## Introduction
The aim of this project is to create an AWS Step Function state machine. This state machine is designed to add two numbers and subsequently initiate distinct branches of workflows depending on whether the resultant sum is even or odd.

## Technologies Used
- AWS Lambda
- Step Function

## Usage
- Automating Workflow Decision-making: The state machine facilitates the automation of decision-making processes within workflows based on specific conditions.
- Data Transformation: Utilizing Lambda functions, the system performs conversions of the resultant sum to alternative formats, enhancing data processing capabilities.
- Workflow Orchestration: By integrating AWS Step Functions, users can orchestrate the execution of multiple tasks and branches of workflows seamlessly, optimizing resource utilization and workflow efficiency.
- Testing and Validation: The state machine enables users to execute test inputs, observe outcomes, and validate the functionality and behaviour of the workflow under various scenarios, facilitating testing and refinement.

## Benefits
- Efficiency: Automating workflow decision-making reduces manual intervention, streamlines processes, and improves overall efficiency.
- Versatility: The ability to convert the resultant sum into different formats enhances data interpretation and analysis, providing versatility in data processing.
- Resource Optimization: Parallel states allow for the concurrent execution of tasks, optimizing resource utilization and reducing processing time.
- Scalability: AWS Step Functions offer scalability, allowing workflows to adapt and scale based on changing requirements and workloads.
- Security and Compliance: Granting appropriate permissions ensures secure interaction with AWS services while maintaining compliance with security policies and regulations.

## Step 1: Creating Lambda Functions
Begin by creating two Lambda functions:
1. Calculate if the result is even or odd.
2. Convert the result to either binary or Roman numerals.

## Step 2: Creating Step Function
- Create a new state machine using a blank template.
- Add Lambda Invoke state to calculate even/odd.
- Add Choice state to determine the next step based on the result.
- Add CopyObject state for even result and Fail state for odd result.

## Step 3: Adding Parallel State
- Add a parallel state to run conversions to binary and Roman numerals simultaneously.
- Configure Pass states to pass parameters to Lambda functions for conversion.

## Step 4: Invoking Lambda Functions
- Invoke Lambda functions for binary and Roman numeral conversions.

## Step 5: Setting Permissions
- Grant full S3 access to IAM role used by Step Function.

## Step 6: Executing State Machine
- Execute the state machine with test inputs to observe outcomes.

Read more: [Part 1](https://teebaba.hashnode.dev/conditional-workflow-state-machine-part-1)  |  [Part 2](https://teebaba.hashnode.dev/conditional-workflow-state-machine-part-2)

------