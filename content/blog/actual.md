+++
title = "My first post, actually"
date = 2023-02-19
+++

# Node-Red UI - first impressions


**Hi all,**

my name is *Milan Kochan* and I would like to share my experience with **Node-Red** as I've started to work with this platform for first time in my life.
I don't see myself as an experienced programmer at all, even it is my field of study for last two years. Basic knowledge of programming languages such as *C++*, *PHP* or *HTML* was good starting point for me. 
Initial aim for me was **_to make fully compatible Node-Red user interface page_** which can send commands to external device and recieve data as well.


### So my firts step
Thanks to [Node-Red's official website](https://nodered.org/), installation wasn't anything I had problem with. Instructions were clear, internet connection was stable, so in few minutes I was able to run Node-Red on my localhost address.
After successful installation, I need to install module (nodes) that will add possibility to create dashboard in my flows. 


### Step back
Here I met first problem, as my version of Node-Red wasn't supporting dashboard's version.
So I need to take step back, well, actually two, because as I re-installed version of Node-Red, Node.js didn't support it, so I had to re-install Node.js, too. Fortunately, after these actions I was able to install dashboard succesfully, so I could start make flows that need to be done.

### Node-Red
Official website of Node-Red treats newbies really nice because offers many [tutorials](https://nodered.org/docs/) *"how to make flows"*. My first go-to-flow was, surprisingly, *Hello World!*, as I was curious how I can connect different nodes, so they can communicate between each other, send right information and show it in dashboard.
This was incredibly easy to do, as nodes visually represents part of codes, that you don't have to connect through code manually, but automatically create link between them, so no more coding is required. 
So *voilà*, I can send information from flow to dashboard and actually see it. Nice. Then I made dashboard button that will send information, so after pressing "Hello World!" button message appears. Nice.

### Dashboard
Next step was clear - find a way **to connect dashboard with TCP/IP Slave Simulator**, so they will interact between each other. I installed **_node-red-contrib-modbus node_**, that allow me to create nodes which communicate with simulator through ports. 
There are various types of adresses in simulator, so it is possible to differ your registers based on the type of data you want to use. I used two types, **input** and **holding** registers.


**_Input_** ones were recieving data from simulator, so I had to make nodes, that will be continuously reading adressess and when something change, they will show change in dashboard.


**_Holding_** ones were changing values in simulator, so after pressing button (yes, that's why I try to make button before), value in simulator will change from 0 to 1, or backwards.

After I succesfully connected all nodes, final visual presentation fulfilled my previously specified goal, as I was able to communicate with device through Node-Red's daschboard.

### Conclusion
Whole idea of using nodes is really good way how to make programming more comprehensible, also newcomer like me really appreciate paltform like this, with addition of still-expanding commuinty that will help you with any kind of problem you ran into, I see Node-Red as **_easy-to-use platform_** to work with. 