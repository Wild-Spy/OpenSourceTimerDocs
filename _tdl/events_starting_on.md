---
title: Events&#58; starting on
position: 1.9
right_code: |
  ##### Starting On Event Example 1
  ~~~ javascript 
  WaterPlants: enable channel 1 for 1 hour starting on event moistureSensorDetectLow
  ~~~
  {: title="Rules" }
  {: class="codefirst" }
  !CODE_START!
    <img src="!SITE_URL!/images/TDL/event_on.png" alt="Event On">
  !CODE_END!
  {: title="Schedule" }
  
  ##### Starting On Event Example 2
  ~~~ javascript 
  Align: enable channel 1 for 1 hour every 2 hours starting on event reedSwitch
  ~~~
  {: title="Rules" }
  {: class="codefirst" }
  !CODE_START!
    <img src="!SITE_URL!/images/TDL/event_on_reset.png" alt="Event On Reset">
  !CODE_END!
  {: title="Schedule" }
---
Timer Description Language supports events.  Events can be triggered from different inputs
such as a reed switch, light sensor or just a pin level changing.  For example, you could 
attach a water moisture sensor which triggers an event on the Open Source Timer if moisture 
drops below some level.  When the Open Source Timer receives this event it could activate
a sprinkler for 1 hour.

Syntax:
<pre>
<span style="color: #0000aa;">[rule name]</span>: <span style="color: #0000aa;">[action]</span> <span style="color: #0000aa;">[condition]</span> <span style="color: #aa0000;">starting on event</span> <span style="color: #aaaa00;">[event name]</span>
<span style="color: #0000aa;">A</span>: <span style="color: #0000aa;">enable channel 1</span> <span style="color: #0000aa;">for 1 hour</span> <span style="color: #aa0000;">starting on event</span> <span style="color: #aaaa00;">moistureSensorDetectorLow</span>
</pre>

The first example rule on the right shows the situation described above.  The markers in the graph
which look like this ![marker]({{ site.baseurl }}/images/TDL/marker.png), show when events occurred.

Note that rules starting on an event don't have to be [one-shot rules]({{ site.baseurl }}/#one_shot_rules).
For an example see _Starting On Event Example 2_ on the right.  Notice how every time the event is triggered
the rule 'resets'.
{: .warning }