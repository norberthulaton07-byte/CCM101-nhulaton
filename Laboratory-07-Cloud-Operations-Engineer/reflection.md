# Mission Reflection

Before this lab, I assumed that a running container meant everything was fine. Checking the host server first taught me otherwise, because every container shares the same RAM, CPU, and disk. If the host runs out of memory or storage, every container suffers, even the ones that look healthy. Setting a baseline showed me what normal looks like before a traffic surge.

If a user cannot log into a web application, I would run `docker logs` first. The logs record each request and the status code returned, so a 500 error points to a server problem, while a 404 suggests a missing page or a wrong URL. Seeing my own 404 line in this lab showed me how logs let me follow evidence instead of guessing.

Logs and metrics are different tools. Logs are a diary of events that explain what happened and why, while metrics from `docker stats` are numbers like CPU and memory that show current health. Logs help me find the cause, and metrics help me spot trouble early.

Large companies cannot watch thousands of containers by hand, so I think they rely on automated tools. Prometheus collects metrics from every container on a schedule and stores them, and Grafana turns that data into dashboards and alerts that notify engineers when something crosses a limit. Logs are probably gathered into one central place too, so nobody has to log into each container.

My Linux troubleshooting has improved a lot. I now know where to look first: `free -h` and `df -h` for resources, `docker logs` for errors, and `docker stats` for usage. I am also more comfortable reading terminal output instead of feeling lost, and the Killercoda resets taught me to document my work as I go.
