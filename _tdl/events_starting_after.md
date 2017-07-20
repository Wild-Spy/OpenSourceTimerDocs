---
title: Events&#58; starting after
position: 1.91
right_code: |
  ##### Between Condition Example 1
  ~~~ javascript 
  WaterPlants: enable channel 1 for 1 hour starting 30 minutes after event moistureSensorDetectLow
  ~~~
  {: title="Rules" }
  {: class="codefirst" }
  !CODE_START!
    <img src="!SITE_URL!/images/TDL/event_after.png" alt="Event After">
  !CODE_END!
  {: title="Schedule" }
---
Events can also have a delay built into them.  In case you want to start a rule a fixed amount of time after some event
fires.

Syntax:
<pre>
<span style="color: #0000aa;">[rule name]</span>: <span style="color: #0000aa;">[action]</span> <span style="color: #0000aa;">[condition]</span> <span style="color: #aa0000;">starting</span> <span style="color: #aaaa00;">[period]</span> <span style="color: #aa0000;">after event</span> <span style="color: #aaaa00;">[event name]</span>
<span style="color: #0000aa;">A</span>: <span style="color: #0000aa;">enable channel 1</span> <span style="color: #0000aa;">for 1 hour</span> <span style="color: #aa0000;">starting</span> <span style="color: #aaaa00;">30 minutes</span> <span style="color: #aa0000;">after event</span>  <span style="color: #aaaa00;">moistureSensorDetectorLow</span>
</pre>

Strange things can happen if events with delays overlap.  This needs more looking into.
{: .error }