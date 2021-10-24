## TODO for the Techies
Please **fill out the following information below**, as soon as possible. It is **required** to have this file completely filled out and up to date at the end of the project phase.
You can of course use this file to manage your project, e.g. as a place to keep your todos and to plan your features. Also, feel free to edit this readme in any kind of way you like, but the required base layout and information should be consistent throughout all techie projects.

**Hint:** The following file is written in `markdown` which is a language to format text with simple characters. If you are unsure on how to use markdown then have a look at [this guide](https://www.markdownguide.org/basic-syntax/)

By the end you should have filled out the following:
1. **Project Title:** The title of the project, including a description which states the motivation/problem of the project and the developed solution.
2. **How to Setup and Run:** The respective commands to install and run the project
3. **Examples:** A brief overview on how to use the main functionalities of your project (does not have to be code)
4. **Roadmap:** The general outline of what you want to do in what order. Please keep this up to date, so that we can follow what you are and will be doing.
5. **Authors:** Please add all of you and link your respective GitHub profile and other information if you want to. This part if completely up to you.
6. If you are done filling out the information below, please **delete this TODO Section** to keep your project readme clean for other people to get to know more about your project.

# Zero Waste

Do you know how much waste you create in a day? Waste disposal has attracted a lot of attention in recent years, but how can we measure the amount of waste we create? Our goal is to design and compile a website that allows users to record the amount of waste they throw away each day and compare it to existing data to see how much waste reduction they should achieve. We first created a prototype design using Figma, and then implemented it through HTML, CSS and Java Script. In addition to the welcome page and login page, our website also has a personalized dashboard for users, where they can log into their accounts, record their daily waste and see how they compare to the exsisting data.



## How to Setup and Run

In order to setup the project, please proceed as follows:

Firstly, set up a virtual environment in anaconda (you would have to download anaconda first):

```bash
  conda create -n env_zerowaste python=3.8 anaconda -c conda-forge
```
This creates an "environment folder" in which you have to add the code files and then run it in VSCode for example.

In a virtual anaconda environment use:

```bash
  conda activate env_zerowaste
```
to activate the environment (Note that in VSCode you should use the command prompt and not windows powershell).

After successful installation and activation use the following command to run the project:

```bash
  python sbadmin2.py
```
## Examples

You can see a brief overview of how to use the main functionality below

```javascript
import Component from 'my-project'

function App() {
  return <Component />
}
```

  
## Roadmap

- Created the basic wireframe in order to structure the process of front-end development
- Started coding the frontend. Began with the html code and added css later on.
- Research, clean and structure the Data regarding the waste production in germany
- Researched possible methods to connect front- and backend -> Decided to use Flask for a simple backend
- Integrated a bootstrap dashboard using python/anaconda to connect front- and backend
- Integrated the data and changed the bootstrap design to fit our wireframe

  
## Authors

- [@Marvin](https://github.com/M-H0ppe)
- [@Amy](https://github.com/Chiaaang)
- [@Samuel](https://github.com/samrmn)
- [@Ali](https://www.github.com/...)

  

