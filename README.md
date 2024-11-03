# Overview
This project is a practice project to learn openGL, flowing the book (learnopengl.com)[https://learnopengl.com/Introduction]

This is build on WSL 2 plarfrom. Should work on any LINUX platfrom

# How to run this project
Before running, you expected to have Cmake, WLFG >3.3 need to installed. The book guide you to intall your the WLFG from the source. Also it will as you to download the (glad codes)[http://glad.dav1d.de/] file form a website. 

```sh
# if a build folder is there, sometime if you use some IDE that automaticaly build your code
rm -r build

#Build the project - This step create the makefile
cmake -S . -B build

#Build binary
cmake --build build
```

# Issues
```
MESA: error: ZINK: failed to choose pdev
glx: failed to create drisw screen
```
## Solutions
```bash
export GALLIUM_DRIVER=llvmpipe
```
