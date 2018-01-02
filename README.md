# Oddball Homework Challenge

This is an open-book test, so Google away, but please don't copy your work from pre-existing solutions you may find or ask others to help you complete the exercises. Solutions should be able to be run on a UNIX command line (Linux/Mac).

## Getting Started

Feel free to fork this repo, and push commits to your fork.

## Getting help

If you get stuck, have a question, or want to clarify any aspect of the homework, you can contact members of our development team by emailing the person who sent you the link to the challenge.

## Submitting your completed homework

To submit your homework, zip up the contents of your git repo in a .zip file. Please remove the .git directory `node_modules` directory, and anything else that might identify you. If you want to include any comments with your submission, add them to the COMMENTS file. If there's anything important for us to know about how to run your code, please include that information in the COMMENTS file. Feel free to include any other information relevant to your submission in the COMMENTS as well. Then email the person who sent you the challenge with that zip file. If it is too large to be sent via email, please send a link to google drive/dropbox/box.com.

## Evaluation process

When we receive your homework, we'll assign it a random number, so that our team does not know whose submission they are reviewing. Your homework will be reviewed by at least three senior engineers on our team.


# EFIN Calculator

The EFIN calculator allows multiple users to enter their household size and their income and see their EFIN appear below.

## Requirements

Ruby, rails, and node installed

To get application running

* `npm install`
* `bundle exec rails s`

## The task(s)

Generally your submission should demonstrate developer best practices. DRY code, keeping things modular etc etc. Show us your understanding and imaginination within the time allotted

## Part 1

Configure Rails to accept web socket requests from the front end and return a response.

Requirements:

* a user can enter their income and household size and it is passed to the backend via websockets

## Part 2

Configure a background worker of your choice that can accept jobs from action cable, and can perform a request to an external service  available at `http://efin.oddball.io` ( you can check its health at `/health`)

The external service is a single url that accepts `JSON` `POST` requests with this structure

```json
{
  "household": 1,
  "income":  20000
}

```

If you pass incorrectly formatted data you will receive an error.
Unfortunately this service is quite slow and can often take 5-10 seconds for a response.
When you do receive a response, update the front end via websockets to show the user their EFIN

Requirements:

* background worker that proxies requests to an external service
* actioncable that takes results from worker and displays them on the screen

## Tips & Guidance

* Do read the docs for action cable carefully
* Do feel free to refactor my js or clean up the front end as much as you want, please no coffee script though.
* Use whichever background worker you want, just make sure to include instructions for how to get it set up
* This is your chance to impress the Oddball engineering team, feel free to write tests/modularize things, clean up the code etc. Treat this like a real project that you would be inheriting.
