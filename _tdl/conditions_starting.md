---
title: Conditions&#58; starting
position: 1.9
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
To the right you'll see a very simple rule in Timer Description Language.  Click on the 'Schedule' tab to see the output from the rule.

Notice that this simple rule is made up of a number of parts.
<pre>
<span style="color: #aa0000;">[rule name]</span>: <span style="color: #0000aa;">[action]</span> <span style="color: #aaaa00;">[condition]</span>
<span style="color: #aa0000;">A</span>: <span style="color: #0000aa;">enable channel 1</span> <span style="color: #aaaa00;">for 30 minutes every 2 hours</span>
</pre>
There are three different types of intervals.
1. [for intervals]({{ site.baseurl }}/#tdlconditions_for)
2. [between intervals]({{ site.baseurl }}/#tdlconditions_between)
3. [on intervals]({{ site.baseurl }}/#tdlconditions_on)
There are different recipes that can be followed in TDL but each of them follows this basic syntax of `rule name`, `action`, `condition`.
