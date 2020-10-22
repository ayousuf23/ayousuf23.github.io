---
layout: archive
title: "Portfolio"
permalink: /portfolio/
author_profile: true
---
This is a collection of the software/code I've made/written in reverse chronological order. I use Microsoft Visual Studio to code C, C++, and C#. I use Visual Studio Code to code Python. I use IntelliJ IDEA to code Java.

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

Below are the projects I've written and made. I hope you like them!

{% include base_path %}

{% assign portfolio = site.portfolio | sort: "order" %}
{% for post in portfolio %}
  {% include archive-single.html %}
{% endfor %}

