# Job Scheduler

## Overview
The Job Scheduler is a C++ application designed to manage and allocate jobs to a set of worker nodes based on their resource requirements. It simulates a job scheduling system where jobs are processed based on their resource needs (CPU cores and memory) and tracks the overall performance of the scheduling process.

## Features
- **Job Management**: Allows the addition of jobs with specific resource requirements.
- **Resource Allocation**: Allocates jobs to worker nodes based on available resources (CPU cores and memory).
- **Statistics Tracking**: Tracks the total number of jobs processed, CPU utilization, and memory utilization.
- **CSV Export**: Generates a CSV file containing the statistics of the job scheduling process.

## Components
- **Job Structure**: Represents a job with attributes such as arrival time, cores required, memory required, and execution time. It also includes a method to calculate the gross value of the job.
  
- **WorkerNode Structure**: Represents a worker node with an ID, available cores, and available memory.

- **JobScheduler Class**: Manages the job queue and worker nodes. It includes methods to:
  - Add jobs to the queue.
  - Schedule jobs based on current resource availability.
  - Allocate jobs to worker nodes.
  - Print statistics of the job processing.
  - Generate a CSV file with the statistics.

## Usage
1. **Initialization**: Create an instance of `JobScheduler` with the desired number of worker nodes.
2. **Adding Jobs**: Use the `addJob` method to add jobs to the scheduler.
3. **Scheduling**: Call the `scheduleJobs` method in a loop to process jobs over a specified time period (e.g., hours).
4. **Statistics**: After scheduling, use `printStatistics` to display the performance metrics and `generateCSV` to save the statistics to a file.

## Example
The main function demonstrates how to create a `JobScheduler` with 128 worker nodes, add 128 jobs with varying resource requirements, and schedule them over a 24-hour period. Finally, it prints the statistics and generates a CSV file named `scheduler_stats.csv`.

## Requirements
- C++11 or later
- Standard C++ library

## License
This project is licensed under the MIT License.
