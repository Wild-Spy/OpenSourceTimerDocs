---
title: Actions
description: Actions describe what should happen when a rule changes states.
position: 1.2
right_code: |
  ~~~ javascript 
  A: enable channel 1 for 30 minutes every 2 hours
  ~~~
  {: title="Enable Rule" }
  {: class="codefirst" }
  !CODE_START!
    <img src="!SITE_URL!/images/TDL/en_ch1_30min_every_2hours.png" alt="...">
  !CODE_END!
  {: title="Enable Schedule" }
  <div></div>
  ~~~ javascript 
  A: disable channel 1 for 30 minutes every 2 hours
  ~~~
  {: title="Disable Rule" }
  {: class="codefirst" }
  !CODE_START!
    <img src="!SITE_URL!/images/TDL/dis_ch1_30mins_every_2hours.png" alt="...">
  !CODE_END!
  {: title="Disable Schedule" }
---
Here are two example actions:

~~~ ruby
enable channel 1
disable rule myRule
~~~

Each action follows the format

~~~
[enable/disable] [target]
~~~

The first word must be either `enable` or `disable`.  This determines what the target will do when the rule is 'on'.  For example, have a look at the following rule.

<div class="info">
	Keywords:
	<ul style="margin: 0;">
		<li>enable - channel or rule is on by default</li>
		<li>disable - channel of rule is off by default</li>
	</ul>
</div>
<br>

~~~ ruby
A: enable channel 1 for 30 minutes every 2 hours
~~~
{: title="Rule" }
{: class="codefirst" }
![enable channel 1 for 30 minutes every 2 hours]({{ site.baseurl }}/images/TDL/en_ch1_30min_every_2hours.png)
{: title="Schedule" }
{: class="codex custom-scroll-light"}

This rule turns channel 1 on for 30 minutes every 2 hours.  For the remainder of the two hours the channel will be off.  You can see this rendered on the schedule tab above.

The compliment to the `enable` keyword is the `disable` keyword.  If we replace `enable` in the above rule with `disable` we get the following result.

~~~ ruby
A_bar: disable channel 1 for 30 minutes every 2 hours
~~~
{: title="Rule" }
{: class="codefirst" }
![disable channel 1 for 30 minutes every 2 hours]({{ site.baseurl }}/images/TDL/dis_ch1_30mins_every_2hours.png)
{: title="Schedule" }
{: class="codex custom-scroll-light"}

Now we can see that the channel turns off for 30 minutes out of every 2 hours.  For the remainder of the two hours, the channel is on.
