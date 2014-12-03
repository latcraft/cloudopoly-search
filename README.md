W00t?
==================

This repository contains description of the first Cloudopoly challenge.

Problem definition
==================

Publish a simple web service that accepts 3 keywords as a search criteria. 

Web service must respond with the most popular book (with the highest average rating) for each keyword on the following Amazon websites:

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

# Average book rating calculation

Book rating should be calculated using the following formula:

   R = (R<sub>afr</sub> * N<sub>afr</sub> + R<sub>ade</sub> * N<sub>ade</sub> + R<sub>auk</sub> * N<sub>auk</sub>) / (N<sub>afr</sub> + N<sub>ade</sub> + N<sub>auk</sub>)

- R<sub>afr</sub> - average rating on amazon.fr
- N<sub>afr</sub> - number of ratings on amazon.fr
- R<sub>ade</sub> - average rating on amazon.de
- N<sub>ade</sub>  - number of ratings on amazon.de
- R<sub>auk</sub> - average rating on amazon.co.uk
- N<sub>auk</sub> - number of ratings on amazon.co.uk

# Requirements

- Any programming language, any operating system
- Deploy your service to *AWS* *EC2* (free tier)
- Use smallest instance type (`t2.micro`)
- Send IP address of your service before `06.01.2015 16:00` to contest@latcraft.lv
- At `17:00` we start the test! 

# Winner election

Web services, which return the expected result faster, will win.

### Good luck!
