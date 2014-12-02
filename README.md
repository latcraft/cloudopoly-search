W00t?
==================

This repository contains description of the first Cloudopoly challenge.

Problem definition
==================

Publish a simple web service that accepts 3 keywords as a search criteria. 

Web service must respond with the most popular book (with the highest average rating) for each keywoard on the following Amazon websites:

 * amazon.co.uk
 * amazon.fr
 * amazon.de

Expected input: 

        http://<ip address>/search?query=Time+Coder+Delivery

Expected JSON response:

```
[
  "Brief History of Time",
  "Clean Coder",
  "Continuous Delivery"
]
```

# Requirements

 - Service must be deployed on AWS Free Tier.
 - IP address must be sent to contest@latcraft.lv before 06.01.2015 16:00.

# Winner election

Web services, which return the expected result faster, will win.

### Good luck!
