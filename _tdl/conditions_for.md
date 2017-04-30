---
title: Conditions&#58; for
position: 1.6
right_code: |
  ##### For Condition Example
  ~~~ javascript 
  A: enable channel 1 for 15 minutes every hour
  ~~~
  {: title="Rules" }
  {: class="codefirst" }
  !CODE_START!
    <img src="!SITE_URL!/images/TDL/en_15mins_every_hour.png" alt="...">
  !CODE_END!
  {: title="Schedule" }
---
`For` conditions are the simplest type of conditions. They specify how long the rule should be on for in their period.

Take a look at the following rule and it's output schedule.

~~~ ruby
A: enable channel 1 for 15 minutes every hour
~~~
{: title="Rule" }
{: .codefirst }

![disable channel 1 for 15 minutes every hour]({{ site.baseurl }}/images/TDL/en_15mins_every_hour.png)
{: title="Schedule" }
{: .codex .custom-scroll-light }

`For` conditions are always aligned with the start of each period.  This is demonstrated in the schedule above where the channel is on for
the first 15 minutes of every hour and off for the last 45.
