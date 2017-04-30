---
title: Conditions&#58; between
position: 1.7
right_code: |
  ##### Between Condition Example 1
  ~~~ javascript 
  A: enable channel 1 between 9am and 5pm every day
  ~~~
  {: title="Rules" }
  {: class="codefirst" }
  !CODE_START!
    <img src="!SITE_URL!/images/TDL/between_9to5_day.png" alt="...">
  !CODE_END!
  {: title="Schedule" }

  ##### Between Condition Example 2
  ~~~ javascript 
  A: enable channel 1 between the 2nd and 4th week every month
  ~~~
  {: title="Rules" }
  {: class="codefirst" }
  !CODE_START!
    <img src="!SITE_URL!/images/TDL/between_2_4_week_month.png" alt="...">
  !CODE_END!
  {: title="Schedule" }

  ##### Between Condition Example 3
  ~~~ javascript 
  A: enable channel 1 between second 3 and 70 every two minutes
  ~~~
  {: title="Rules" }
  {: class="codefirst" }
  !CODE_START!
    <img src="!SITE_URL!/images/TDL/between_3and70_every2.png" alt="...">
  !CODE_END!
  {: title="Schedule" }
---
`Between` conditions specify an active interval for the rule.  This interval is repeated each period.

Take a look at the following `between` rule and it's output schedule.

~~~ ruby
A: enable channel 1 between 9am and 5pm every day
~~~
{: title="Rule" }
{: .codefirst }

![enable channel 1 between 9am and 5pm every day]({{ site.baseurl }}/images/TDL/between_9to5_day.png)
{: title="Schedule" }
{: .codex .custom-scroll-light }

`Between` conditions have one of the following syntaxes:
<pre>
<span style="color: #aa0000;">between</span> <span style="color: #0000aa;">[start time]</span> <span style="color: #aa0000;">and</span> <span style="color: #0000aa;">[stop time]</span>
<span style="color: #aa0000;">between</span> <span style="color: #555555;">[second/minute/day/etc]</span> <span style="color: #0000aa;">[start]</span> <span style="color: #aa0000;">and</span> <span style="color: #0000aa;">[stop]</span>
<span style="color: #aa0000;">between</span> <span style="color: #0000aa;">[start]</span> <span style="color: #aa0000;">and</span> <span style="color: #0000aa;">[stop] <span style="color: #555555;">[seconds/minutes/days/etc]</span></span>
</pre>

<div>
	<p>
		It's important to include an <code>every</code> part in your <code>between condition</code> rule unless you want a one-shot rule.
	</p>
	<p>Here's an example of what not to do.</p>
<pre title="Rule" class="codex codefirst">
A: enable channel 1 between 9am and 5pm
</pre>
	<div title="Schedule" class="codex custom-scroll-light">
        <img src="{{ site.baseurl }}/images/TDL/oneshot_between.png" alt="">
	</div>
</div>
{: .error }
<br>
A number of examples of `between condition` rules are shown in the code bar on the right.
