# Docker Mesos Demo

This repository contains all resources for running a simple demonstration of Apache Mesos. 
It contains an Apache Mesos instance, 2 Mesos Agents, a Marathon instance and a Apache Zookeeper instance, that can run docker containers as demo jobs.


## Requirements

You need to have [docker](https://www.docker.com/) installed on your local machine.


## Setup

Clone this repository:
```bash
git clone https://github.com/lorenzhohmann/docker-mesos-demo.git
cd docker-mesos-demo
```

Start all docker containers by running:
```bash
docker compose up -d
```

That's it. The Mesos UI should be available at [http://localhost:5050](http://localhost:5050) and the Marathon UI at [http://localhost:8080](http://localhost:8080).


## Running a job

Open the [Marathon UI](http://localhost:8080) and create a new job. Parse the content from the `demo-job.json` in the JSON view and submit the job.
You can now switch to the [Mesos UI](http://localhost:5000) to see the progress and task distribution in Apache Mesos.
