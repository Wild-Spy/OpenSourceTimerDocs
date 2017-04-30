---
title: Action Targets
description: Action targets specify what the rule should affect when it changes state.
position: 1.3
right_code: |
  ~~~ javascript 
  a: enable channel 1 for 30 minutes every 2 hours
  B: enable rule a for 1 day every every second day
  ~~~
  {: title="Rule Target Rule" }
  {: class="codefirst" }
  !CODE_START!
    <img src="!SITE_URL!/images/TDL/en_rule_example.png" alt="...">
  !CODE_END!
  {: title="Rule Target Schedule" }

  <div></div>

  ~~~ javascript 
  A: enable channel 1 for 30 minutes every 2 hours
  ~~~
  {: title="Channel Target Rule" }
  {: class="codefirst" }
  !CODE_START!
    <img src="!SITE_URL!/images/TDL/en_ch1_30min_every_2hours.png" alt="...">
  !CODE_END!
  {: title="Channel Target Schedule" }
---
As mentioned in [Actions]({{ site.baseurl}}/#tdlactions), each action has the following format.

~~~
[enable/disable] [target]
~~~

The `target` is what will be affected when this rule changes state. The `target` can be either:
1. a [channel]({{ site.baseurl}}/#tdlchannels), or
2. a [rule]({{ site.baseurl}}/#tdlsimple_example)

To target a channel just use the `channel` keyword followed by the channel id.
{: .success }

In future named channels will be supported.  For now you can use [variables]({{ site.baseurl}}/#tdlvariables).
{: .info }

The ability to target another rule means that multiple rules can be cascaded to form complex patterns.

Here's an example of using a rule as a target.

<!--
Note that rule `a` starts with a lower case letter. This means it's not enabled by default. 
Rule `B` on the other hand starts with an upper case letter, meaning that it is enabled by default.  
{: .success }
-->

~~~ javascript 
a: enable channel 1 for 30 minutes every 2 hours
B: enable rule a for 1 day every every second day
~~~
{: title="Rule Target Rule" }
{: class="codefirst" }

<img src="{{ site.baseurl }}/images/TDL/en_rule_example.png" alt="...">
{: title="Rule Target Schedule" }
{: .codex .custom-scroll-light }
