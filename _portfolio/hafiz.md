---
title: "Hafiz"
collection: portfolio
created: June-August 2020
order: 1070
---
Hafiz is a website designed to make memorization of the Holy Qur'an easier by offering different types of quizes. The best way to memorize is by repetition, so the quizes are designed with this in mind. There are currently three different types of quizzes available on the website: arranging a Surah ayat-by-ayat, selecting the correct ayat in the sequence, and filling in the blanks of an ayat. 

I made the website using C#, ASP.NET Core, JavaScript, and HTML. The website uses a custom made XML file for the data of the Holy Qur'an. The XML file is deserialized and a Qur'an object is created with the corresponding suwar (plural of Surah) and ayaat. The view controllers in the website use the Qur'an object for generating site data (quizes, etc.).

The site is currently being hosted on Azure. Please [click here](https://quranhafiz.azurewebsites.net/) or copy this link to visit the website: [https://quranhafiz.azurewebsites.net/](https://quranhafiz.azurewebsites.net/)

The source code for the website and the XML Formatter are hosted on GitHub. Please [click here](https://github.com/appzoidinc/Hafiz) or copy this link to visit the GitHub repository: [https://github.com/appzoidinc/Hafiz](https://github.com/appzoidinc/Hafiz)

*Note* the repository for the XML Formatter is under the same user as the Hafiz website repository. 
{: .notice}
