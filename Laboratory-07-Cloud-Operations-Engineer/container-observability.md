# Container Observability

## Application Logs (Checkpoint 4)
The 404 error line from the log: 172.17.0.1 - - [13/Oct/2026:03:52:04 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"

Application logs are vital for troubleshooting because they record exactly what was requested, when, and how the server responded, which lets an engineer pinpoint the precise cause of a failure instead of guessing. Without logs, there would be no way to tell whether an error was caused by a missing page, a misconfigured server, or a user mistake.
