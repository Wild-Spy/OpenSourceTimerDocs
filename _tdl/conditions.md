---
title: Conditions
position: 1.5
right_code: |
  ~~~ javascript 
  A: enable channel 1 for 30 minutes every 2 hours
  ~~~
  {: title="Rules" }
  {: class="codefirst" }
  !CODE_START!
    <img src="!SITE_URL!/images/TDL/en_ch1_30min_every_2hours.png" alt="...">
  !CODE_END!
  {: title="Schedule" }
---
A condition is the meat of a rule.  It describes when the rule should change states.
<pre>
<span style="color: #aa0000;">[rule name]</span>: <span style="color: #0000aa;">[action]</span> <span style="color: #aaaa00;">[condition]</span>
<span style="color: #aa0000;">A</span>: <span style="color: #0000aa;">enable channel 1</span> <span style="color: #aaaa00;">for 30 minutes every 2 hours</span>
</pre>

The condition is broken up into three parts:

<pre>
<span style="color: #aa0000;">[interval]</span> <span style="color: #0000aa;">[period]</span> <span style="color: #aaaa00;">[(optional) starting]</span>
<span style="color: #aa0000;">for 30 minutes</span> <span style="color: #0000aa;">every 2 hours</span> <span style="color: #aaaa00;">starting at 1pm on 1/1/2018</span>
</pre>

The first part is the interval. There are three different types of intervals.
1. [for intervals]({{ site.baseurl }}/#tdlconditions_for) eg. `for 1 minute`
2. [between intervals]({{ site.baseurl }}/#tdlconditions_between) eg. `between 9am and 5pm`
3. [on intervals]({{ site.baseurl }}/#tdlconditions_on) eg. `on the 1st, 5th, 10th`

Intervals describe when the rule should be 'on' during each `period`.

The second part is the period.  It describes the period over which the rule should be repeated.  For example the period could be `one day`, `2 weeks`, `1 day and 3 hours`, etc.

<div>
<h4 id="one_shot_rules">One Shot Rules</h4>
The period can be omitted for one-shot rules.  For example, the condition `for 6 minutes` will run for 6 minutes then never be activated again.
</div>
{: .info }
<br/>
The last part is the starting part.  It describes when the rule should begin.

TODO: write more about starting part and events
{: .error }
