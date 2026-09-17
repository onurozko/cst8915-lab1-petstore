# CST8915 Lab 1: Algonquin Pet Store on Azure VM

**Student Name:** Tahir Onur Ozkoral  
**Student ID:** 041122154

**Course:** CST8915 Full-stack Cloud-native Development  
**Semester:** Fall 2026  

---

## Demo Video

[Watch Demo Video](https://www.youtube.com/watch?v=BiwrKWSLmv4)

---
## Technical Explanations

### Order Service (Node.js)

Order Service's purpose here to receive orders from the frontend and send the order information to RabbitMQ. Basically it uses Node.js to provide the backend API for receiving order requests. It is basically a backend but specialized to receive orders. 
If I were to think from my previous experiences, for Python we could have used something like FastAPI or Django, or maybe if we want to use C#/Microsoft stack, something like ASP.NET Core could have worked.
In the microservices architecture, it handles the order-related part of the application separately from the other services.

### Product Service (Rust)

Product Service is responsible for giving the product information to be used by the frontend. It uses Rust to provide the backend API for product information. Again, just like Order Service, this is also a backend, but it is specialized to give product information. So alternatively we could have used something like C#, Java, Python and such.
Its role in the microservices architecture is to handle product data, again separately from the order and frontend services.

### Store Front (Vue.js)

The Store Front is responsible for displaying the products and allowing the user to place orders. It uses Vue.js because it is the frontend framework used to build the user interface. Alternatively we could have used other frontend stack too, like anything from React, Angular, or plain HTML, CSS, JavaScript.
Its role in the architecture is to act as the part of the application that the user interacts with. It gets product data from Product Service and sends order requests to Order Service. It also handles everything separately from other services.

---

## Challenges and Learnings

One of the main challenges for me was working with the Azure VM through VS Code. In the past, when I worked with cloud servers, I mostly connected through CMD/Shell and only did limited work directly on the server. For this lab, I had to connect VS Code to the VM using Remote SSH and make changes to the project files directly from VS Code, which was a different workflow for me.
I also ran into an SSH public key issue while setting up the connection. I have had similar SSH problems before, but this time there was an extra step involving the .pem private key file and making sure VS Code was using the correct key in the SSH configuration.

The main thing I learned from this lab was how useful VS Code Remote SSH can be when working on a cloud VM. I was able to open the project files, edit the Vue configuration, run multiple terminals, and manage the different services directly from VS Code while everything was actually running on the Azure server without bothering with editing them on cmd. It made the remote development process feel much more similar to working on a local project.
