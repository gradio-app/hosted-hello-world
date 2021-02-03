# hosted-hello-world
This simple repo shows how easy it is to deploy a Gradio Hosted interface. For more info on Hosted, see our [introduction post](https://gradio.app/introducing-hosted). 

Here's what you need in the repo: 

* A launch file --> `launch.py`
* A `requirements.txt` file

Let's start with the launch file, this is the file that launches the gradio interface. In this case, we're wrapping a simple function: 

```
import gradio

def hello(inp):
  return "Hello {}!".format(inp)

io = gradio.Interface(fn=hello, inputs='text', outputs='text', title='Hello World', 
    description='The simplest Hosted interface.')  
io.launch()
```

If we were to run this file locally, we would see the interface below: 

<img src="https://i.ibb.co/q5XhN8r/hello-world.gif"/>

The second step is to create a `requirements.txt` file with all the requirements that are needed to to run `launch.py`. In this case, the only thing we need is Gradio, so the file is has just on requirement. 

```
gradio
```

Now we can deploy this by giving Gradio Github access through [Hosted](https://gradio.app/hosted), and picking the right repo. 

<img src="https://i.ibb.co/54D8fMs/hosted-hello-world.gif"/>

And here's the live link: https://gradio.app/g/aliabd/hosted-hello-world

Feel free to fork this repo as a starting point for your Hosted project! 
