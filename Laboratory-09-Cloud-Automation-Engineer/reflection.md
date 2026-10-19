# Mission Reflection

When I first started this lab, I thought automation was just a fancy way of saving time. Now I understand it is the only realistic way to manage hundreds of cloud servers. Nobody can log into every machine and repeat the same task by hand without getting tired, skipping a step, or making a typo. A script does the job the same way every time, and a cron job keeps it running at 2:00 AM while everyone is asleep.

However, automation has a dark side. It spreads mistakes just as fast as it spreads good work. If a script with a destructive typo, such as deleting the wrong folder, is scheduled on 1,000 servers, all of them could be damaged before anyone notices. That is why scripts should be tested on something small first, like the dummy app-data folder I used, and why backups and careful reviews matter so much.

Writing a Bash script also felt very different from creating the Docker Compose file in Mission 6. Bash was like giving the computer step-by-step orders: do this, then do that. Docker Compose was more like describing the result I wanted, such as the containers and ports, and letting Docker figure out the steps. Bash felt more flexible but easier to break, while YAML felt cleaner and easier to read.

Looking back at Laboratory 1 to 9, my understanding of cloud computing has changed a lot. At the start of the semester, I thought the cloud was mostly someone else's computer for storing files. Now I see it as a set of connected skills: building infrastructure, comparing providers, working with containers, handling data, deploying applications, and automating the repetitive work. It is less about one tool and more about how everything fits together.

My favorite role was the Cloud Deployment Engineer. I enjoyed seeing something I set up actually run, and it was satisfying when the containers finally worked after I fixed my errors. It felt the most hands-on and closest to real work.
