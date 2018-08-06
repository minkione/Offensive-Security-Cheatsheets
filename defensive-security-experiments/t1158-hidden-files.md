---
description: 'Defense Evasion, Persistence'
---

# T1158: Hidden Files

## Execution

{% code-tabs %}
{% code-tabs-item title="attacker@victim" %}
```bash
PS C:\experiments> attrib.exe +h .\mantvydas.sdb
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Note how powershell \(or cmd\) says the file does not exist, however you can type out its contents if you know the file exists:

![](../.gitbook/assets/attrib-nofile.png)

Note, that `cmd /a:h` \(attribute: hidden\) reveals files with a "hidden" attribut set:

![](../.gitbook/assets/attrib-reveal.png)

## Observations

As usual, monitoring commandline arguments may be a good idea:

![](../.gitbook/assets/attrib-set.png)

{% embed data="{\"url\":\"https://attack.mitre.org/wiki/Technique/T1158\",\"type\":\"link\",\"title\":\"Hidden Files and Directories - ATT&CK for Enterprise\"}" %}


