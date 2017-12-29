# EFIN Calculator

The EFIN calculator allows a user to enter their age, and their income and see their EFIN appear below

Rails app that allows a user to enter a number, it passes the number to the backend via websockets, the backend passes that number to a background queue that background queue hits an external xml api, process the response and passes that output to the front end via ActionCable