# Multi-Tier Architecture Overview

## 1. Web/Application Tier

This is the front part of the app that you see and interact with. It receives your clicks and requests from your browser, handles the app's rules (business logic), and builds the screens you look at. When it needs information, it sends a message to the database, gets the data back, and displays it for you.


## 2. Database Tier

This is the safe storage room in the back. It holds all the permanent data, such as your username, password, profile settings, and app content. Its only job is to organize this information, keep it safe, and quickly find or save data whenever the app tier asks for it.


## 3. Why Separate Into Independent Containers?

By separating the two, you can easily scale for example, the application. Once your application got busy, you can add more container without having the hassle to duplicate the database. Also, you can fix, update, or restart your web app without taking down the database or losing any saved data.

