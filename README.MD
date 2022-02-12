
  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
# e-commerce-back-end

## Description
This project connecting the back end functionality of a database of products with categories and id's for an e=commerce site by To use this app you will need to run a program like insomnia or postman. The routes posted in the `routes` and `api` folders will need to match the requests in Insomnia like in the walkthrough video linked below..  My motivation for this project was to I wanted to find a way to create all the routes with corresponding links to the Models in the the database.  .
I wanted to solve the problem of the way of linking models to route requests and editing the various `JSON` objects to reflect the information from the request body.  I learned I learned how to carefully write `try` and `catch` methods with the `async` and `await` type promises.  I also furthered my knowledge of constructor classes and learned how they are linked with the sequelize package in node.js. 

# Table of Contents
- [Installation](#Installation)
- [Description](#Description)
- [Usage](#Usage)
- [What-I-learned](#What-I-Learned)
- [Tests](#Tests)
- [Screenshot-of-Application](#Screenshot-of-Application)
- [Links](#Links)
- [Questions?](#Questions?)
- [License](#License)


## Installation
In order to install this project you will need to you will need to run `npm i` in the command line/terminal where this application directory was installed/cloned.  You will need to create a `.env` file to link tyo your database with correct password, user name, and a database called `ecommerce_db`.  Make sure you create this file in your main directory.  Next, you will need to seed the database by running `node index.js` in your directory folder `seeds`.  Then you can navigate back to the root directory and run `node server.js`.  From this point you may follow the routes associated within the routes folder and within the walk-through video. .

## Usage
This Project is used for connecting the back end functionality of a database of products with categories and id's for an e=commerce site. 

## What-I-Learned
I learned how to carefully write `try` and `catch` methods with the `async` and `await` type promises.  I also furthered my knowledge of constructor classes and learned how they are linked with the sequelize package in node.js.  
The please email me were issues in this project.
*Elaborate what you learned and add coding comments here*

    router.get('/:id', async (req, res) => {
    try {
      const tagData = await Tag.findByPk(req.params.id, {
        include: ({ model:Product }),
      });
      res.status(200).json(tagData);
    } catch (err) {
      res.status(500).json(err);
    }


## Screenshot of Application
![screenshot of application](e-commerce-back-end-screenshot.gif)

## Links
[walkthrough video of application in insomnia](https://drive.google.com/file/d/1E5yMGr7fkaRQjJsMQchgpamElAr8eK5u/view?usp=sharing)

[walk-through video part 2](https://drive.google.com/file/d/1pLPBBq0f623fjsLrSANCnvjQXPXs7_zj/view?usp=sharing)

## Questions?
My gitHub user name is byrdbass, and you may email me at byrdbass@gmail.com for Questions.
You may contribute to this project by please email me if you are interested in contributing.

## License
MIT
