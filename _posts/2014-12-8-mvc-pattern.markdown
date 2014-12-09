---
layout: post
title:  "ELI5 MVC, MVP & MVVM"
date:   2014-12-8 10:56:08
categories: jekyll update
---
### Model View Controller

Usually called MVC or MCV design pattern. This can be kinda confusing but I'm going to do my best to explain it you like I would explain it to myself (like i'm 5.)

Using a MVC design pattern means splitting different part of your code into different files according to their role. This is a way to make your code more readable and more easily maintained. The MVC pattern is a User Interaction presentation pattern that focuses on separating the UI (View) from its business layer (Model.)

The three components are: View is responsible for the UI elements, the Controller responsible for determining which View is displayed in response to any action including when the application loads and the Model is responsible for business behaviors and state management(). All three components interact with each other.

In MVC, every action in the View correlates with a call to a Controller along with an action. In the web each action involves a call to a URL on the other side of which there is a Controller who responds. Once that Controller has completed its processing, it will return the correct View.

What is business logic/ behaviors?

From Wikipedia: "In computer software, business logic or domain logic is the part of the program that encodes the real-world business rules that determine how data can be created, displayed, stored, and changed. It is contrasted with the remainder of the software which might be concerned with lower-level details of managing a database or displaying the user interface, system infrastructure, or generally connecting various parts of the program."

This is how the interactions look:
![MVC pattern](../images/mvc.png)

### Model View Presenter

Usually called MVP design pattern.

The MVP pattern is a UI presentation pattern based on the concepts of the MVC pattern. The pattern separates responsibilities across four components: the Presenter contains the UI business logic for the View. All invocations from the View delegate directly to Presenter. The Presenter is also decoupled directly from the View and talks to it through an interface.

For example, when someone clicks the "Save" button, the event handler delegates to the Presenter's "OnSave" method. Once the save is completed, the Presenter will then call back the View through its interface so that the View can display that the save has completed.

This is how the interactions look:
![MVP pattern](../images/mvp.png)

##### Key Differences Between MVC and MVP Patterns:

In MVP the view draws data from the presenter which draws and prepares/normalizes data from the model while in MVC the controller draws data from the model

MVP Pattern

* View is more loosely coupled to the model. The presenter is responsible for binding the model to the view.

* Easier to unit test because interaction with the view is through an interface.

* Usually view to presenter map one to one. Complex views may have multi presenters.

MVC Pattern

* Controller are based on behaviors and can be shared across views.

* Can be responsible for determining which view to display.
