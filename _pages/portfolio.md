---
layout: archive
title: "Portfolio"
permalink: /portfolio/
author_profile: true
---
This is a collection of the software/code I've made/written in reverse chronological order.

These are the programming langauges I know (from most frequently used to least frequently used):
1. C#
2. C++
3. C
4. Python
5. Java

These are the frameworks I use or have worked with (in no particular order):
- .NET Framework
- .NET Core
- Windows Forms
- Windows Presentation Foundation (WPF)
- Universal Windows Platform (UWP)
- Xamarin
- Mono
- MonoGame (based off of Microsoft XNA Framework)
- ASP.NET Core
- JUnit

I have limited experience working with Swift, UIKit, and SpriteKit for iOS.

Below are the projects I've written and made. I hope you like them!

**Notice**: this list of projects is **not** complete and I still have many projects to add. Most of my projects are hosted on a private git repository. If you want access to the repositories please contact me. 
{: .notice}

{% include base_path %}

{% assign portfolio = site.portfolio | sort: "order" | reverse %}
{% for post in portfolio %}
  {% include archive-single.html %}
{% endfor %}

