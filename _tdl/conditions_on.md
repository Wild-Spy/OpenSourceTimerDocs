---
title: Conditions&#58; on
position: 1.8
right_code: |
  ##### On Condition Example 1
  ~~~ javascript 
  A: enable channel 1 on the 1st, 5th, 8th day every month
  ~~~
  {: title="Rules" }
  {: class="codefirst" }
  !CODE_START!
    <img src="!SITE_URL!/images/TDL/on_158day.png" alt="...">
  !CODE_END!
  {: title="Schedule" }

  ##### On Condition Example 2
  ~~~ javascript 
  A: enable channel 1 on minute 8, 29, 55 every hour
  ~~~
  {: title="Rules" }
  {: class="codefirst" }
  !CODE_START!
    <img src="!SITE_URL!/images/TDL/onminute82955.png" alt="...">
  !CODE_END!
  {: title="Schedule" }

  ##### On Condition Example 3
  ~~~ javascript 
  A: enable channel 1 on the 2nd, 4th week every month
  ~~~
  {: title="Rules" }
  {: class="codefirst" }
  <div class="codex" title="Description">
    Enables channel 1 during the 2nd and 4th week of every month
  </div>
  !CODE_START!
    <img src="!SITE_URL!/images/TDL/on24week.png" alt="...">
  !CODE_END!
  {: title="Schedule" }
---
`On` conditions specify a list of intervals during which the rule will be active.

Take a look at the first example on the right (On Condition Example 1) and it's schedule.

In this example the rule is active on the 1st of the month.  That is, it's active from 
midnight on the first of every month until midnight on the 2nd of every month.  It will 
also be active on the 5th of every month.  That is, it will be active from midnight on 
the 4th of every month until midnight on the 5th of every month.  Finally, it will also 
be active on the 8th of every month.

Note that the list must not contain the word `and`.  For 
example `on the 1st, 5th and 8th` will not work.
{: .error }

`On` conditions have one of the following syntaxes:
<pre>
<span style="color: #aa0000;">on</span> <span style="color: #0000aa;">[list of numbers]</span> <span style="color: #555555;">[second/minute/day/etc.] [(optional) of]</span>
<span style="color: #aa0000;">on</span> <span style="color: #555555;">[second/minute/day/etc.]</span> <span style="color: #0000aa;">[list of numbers]</span> 
</pre>

Here are some more examples:

<pre>
<span style="color: #aa0000;">on</span> <span style="color: #555555;">minute</span> <span style="color: #0000aa;">1</span> <span style="color: #dddddd;">every ...</span>
<span style="color: #aa0000;">on</span> <span style="color: #555555;">hour</span> <span style="color: #0000aa;">1, 2, 3, 4, 5</span> <span style="color: #dddddd;">every ...</span>
<span style="color: #aa0000;">on</span> <span style="color: #555555;">month</span> <span style="color: #0000aa;">6, 10</span> <span style="color: #dddddd;">every ... </span>
<span style="color: #aa0000;">on</span> <span style="color: #0000aa;">the 1st, 10th</span> <span style="color: #555555;">day</span> <span style="color: #dddddd;">every ...</span>    ** day is not required, it's implicit here
<span style="color: #aa0000;">on</span> <span style="color: #0000aa;">the 1st, 10th</span><span style="color: #555555;"></span> <span style="color: #dddddd;">every ... </span>       ** same as above
<span style="color: #aa0000;">on</span> <span style="color: #0000aa;">the 3rd</span> <span style="color: #555555;">of</span> <span style="color: #dddddd;">every ...</span>           ** again, day is implicit so we don't need it
<span style="color: #aa0000;">on</span> <span style="color: #0000aa;">the 100th</span> <span style="color: #555555;">second</span> <span style="color: #dddddd;">every ...</span>
<span style="color: #aa0000;">on</span> <span style="color: #0000aa;">the 100th</span> <span style="color: #555555;">second of</span> <span style="color: #dddddd;">every ...</span>
</pre>

TODO: add support for `on the first 5 seconds`, `on the last 10 seconds`.
{: .error }

Weeks is not currently supported.  Eg. `on the 2nd week` will not work.
{: .error }