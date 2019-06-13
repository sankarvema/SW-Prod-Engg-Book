


## Progressive Web Apps

### thru AppCache
### ServiceWorkers and Caching

Can perform
- Caching assets and API calls
- Push Notifications (Push & Notification API)
- Background data sync/preload
- Used in progressive web apps



## Host it right
### Nginx vs Apache Tomcat
  - Nginx can handle more requests per second consistently while apache performance dies out as concurrent connections increases
  - Nginx memory usage is stable while apache memory usage increases with concurrent connections. Nginx is event-based it doesn’t need to spawn new processes or threads for each request, so its memory usage is very low

![](./nginx-apache-memory.png)

![](./nginx-apache-reqs-sec.png)
- Netflix tech stack optimization, from Java to Nodejs
  - Netflix reduced startup time from 40 min to sub 1 min
  - Reduced Ec2 instances by 75% for same number of subscribers at lower latency
- Paypal doubled the number of requests per second and reduced response time by 35%
- Groupon reduced page load time by 50%
