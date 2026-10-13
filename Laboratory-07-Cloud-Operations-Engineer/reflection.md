# Mission Reflection

## Why is it important to check the host server's resources even if your containers are running perfectly? 

Checking the host server's resources is important even when containers are running perfectly, because containers share the underlying host's CPU, memory, and disk. A container can be healthy on its own, but if the host itself runs low on memory or disk space, every container on it can slow down or crash together. Host-level monitoring catches problems that container-level checks alone would miss.

## If a user complains that they cannot log into a web application, how would the docker logs command help you solve the problem? 

If a user complains that they cannot log into a web application, the docker logs command would let me see every request the application received, including the exact timestamp, the endpoint the user tried to reach, and the HTTP status code returned. This could reveal whether the login request even reached the server, whether it failed with an error like a 401, 404, or 500, and roughly when the failure happened, which narrows down whether the issue is the application, the network, or user error.

## What is the difference between monitoring logs (Checkpoint 4) and monitoring metrics (Checkpoint 5)? 

Monitoring logs and monitoring metrics serve different purposes. Logs are a historical, event-by-event record of what happened, such as individual requests and their outcomes, which is useful for investigating a specific incident after the fact. Metrics are real-time, numerical measurements, such as CPU percentage and memory usage, which show the current state and trend of resource consumption. Logs answer "what happened," while metrics answer "how is the system performing right now."

## How do you think large enterprise companies monitor thousands of containers at the same time? (Hint:Refer to Chapter 7 concepts like Prometheus or Grafana).

I think large enterprise companies monitor thousands of containers using centralized tools like Prometheus and Grafana rather than running docker stats manually. Prometheus can collect metrics from many containers and hosts automatically, and Grafana turns that data into dashboards and alerts, so engineers can see the health of an entire fleet at a glance and get notified automatically when something goes wrong, instead of checking each container one by one.

## How has your ability to troubleshoot Linux environments improved? 

My ability to troubleshoot Linux environments has improved noticeably across these missions. I am now more comfortable navigating the terminal, reading command output, and connecting what I see, like a 404 in a log or a CPU spike in docker stats, to a specific cause, rather than treating the terminal as unfamiliar or intimidating.
