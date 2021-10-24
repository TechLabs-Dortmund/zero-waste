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

#This plots the data into a bar and a pie chart (Python Code)
```python
@app.route('/dashboard')
def index():
	df = pd.DataFrame({
		'Fruit': ['Apples', 'Oranges', 'Bananas', 'Apples', 'Oranges', 'Bananas'],
        'Amount': [4, 1, 2, 2, 4, 5],
        'City': ['SF', 'SF', 'SF', 'Montreal', 'Montreal', 'Montreal']
        })
	fig = px.bar(df, x='Fruit', y='Amount', color='City',    barmode='group')
	graphJSON = json.dumps(fig, cls=plotly.utils.PlotlyJSONEncoder)
	fig_pie = px.pie(df, values='Amount', names='City', title='')
	graphJSON2 = json.dumps(fig_pie, cls=plotly.utils.PlotlyJSONEncoder)
	return render_template('index.html', graphJSON=graphJSON, graphJSON2=graphJSON2)
```
#Add this at the bottom of the html doc
```java
  <script src='https://cdn.plot.ly/plotly-latest.min.js'></script>
    <script type='text/javascript'>
      var graphs = {{graphJSON | safe}};
      Plotly.plot('chart-area',graphs,{});
      var graphs_pie = {{graphJSON2 | safe}};
      Plotly.plot('chart-pie',graphs_pie,{});
    </script>
```
#And those two lines at the part where you want the plots to be
```html
<div class="chart-pie pt-4 pb-2" id="chart-pie"></div>
<div class="chart-area" id="chart-area"></div>
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
- [@Ali](https://github.com/AliTabesh)

 ##Our Project 

[ZeroWaste-TechLabs.zip](https://github.com/TechLabs-Dortmund/zero-waste/files/7406261/ZeroWaste-TechLabs.zip)
