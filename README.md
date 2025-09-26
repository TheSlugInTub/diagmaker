# Diagmaker

Diagmaker is a program which lets you create dialogue trees.

I created this program because I wanted to make dialogue for my game, my dialogue is structured like this: there's a dialogue struct with a vector of choices with each having an index of which dialogue to send you to after you select the choice. But creating dialogue like this in the Unity inspector is very confusing and time consuming so I wanted a file format for dialogue that I can easily load in, so I built diagmaker.

You can create a node by pressing middle click, connect two nodes by pressing right click on both of them, and delete a node by pressing delete which having selected a node. You can move nodes around by dragging them with left click, this also selects the node. The inspector will display the selected node and you can edit its two properties, text and event. An event is extra information that can be attached to the node while text is the main content of the node. There is a menu bar at the top where you can save your dialogue tree. It saves it into a lightweight JSON format and you can load this tree. Exporting it will save it into a slightly different format without positions, so you can't load it in. The save format is a .diagsv file while the export format is a .diag file.

The program is built in C with Vulkan.

# Building

You need to install git and cmake if you don't already have them.

```
git clone https://github.com/TheSlugInTub/diagmaker.git
cd diagmaker
mkdir bld
cmake -S . -B bld
cmake --build bld/ --config Release
```
