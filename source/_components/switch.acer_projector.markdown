---
layout: page
title: "Acer Projector Switch"
description: "Instructions on how to integrate Acer Projector switches into Home Assistant."
date: 2016-05-07 07:00
sidebar: true
comments: false
sharing: true
footer: true
logo: acer.png
ha_category: Multimedia
ha_iot_class: "Local Polling"
ha_release: 0.19
---

The `acer_projector` switch platform allows you to control the state of RS232 connected projectors from [Acer](http://www.acer.com).

## {% linkable_title Configuration %}

To use your Acer Projector in your installation, add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry
switch:
  - platform: acer_projector
    filename: /dev/ttyUSB0
```

{% configuration %}
filename:
  description: The pipe where the projector is connected to.
  required: true
  type: string
name:
  description: The name to use when displaying this switch.
  required: false
  type: string
timeout:
  description: Timeout for the connection in seconds.
  required: false
  type: integer
write_timeout:
  description: Write timeout in seconds.
  required: false
  type: integer
{% endconfiguration %}
