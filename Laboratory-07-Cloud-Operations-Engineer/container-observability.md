# Container Observability

## Application Logs 
The 404 error line from the log: 172.17.0.1 - - [13/Oct/2026:03:52:04 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"

Application logs are vital for troubleshooting because they record exactly what was requested, when, and how the server responded, which lets an engineer pinpoint the precise cause of a failure instead of guessing. Without logs, there would be no way to tell whether an error was caused by a missing page, a misconfigured server, or a user mistake.

## Real-Time Metrics 
At the time of the screenshot, the client-website container was using:
- CPU: ("0.00%")
- Memory Usage: (e.g., "2.906MiB / 1.859iB")

# Container metrics 
<img width="705" height="48" alt="container-metrics" src="https://github.com/user-attachments/assets/dd5b2ab2-3cd2-403e-afcb-79f38e427e5e" />
