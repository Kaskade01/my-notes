# Node Installation in a linux box
Install dependencies
```
$ sudo apt-get install libssl-dev g++ make
```
### Copy link from [node.org](https://nodejs.org/en/download/current/)
1. Go to [node.org](https://nodejs.org/en/download/current/)
2. Right click on tar file and "copy link address"
3. Inside the linux instance 
```
$ wget [link address to node tar file]
```

## Build Node
1. Unzip tar file
```
$ tar -xvf [tar file]
```
2. `cd` into node directory
3. Run script and the rest
```
$ ./configure && make && sudo make install
```
_python might be needed_
```
$ sudo apt-get install python
```
