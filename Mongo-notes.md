# MongoDB

### Installation
1. Install with [brew](https://brew.sh/)
```
$ brew install mongodb
```
2. Become root user
```
$ sudo bash
```
3. Create `/data/db` directory
```
$ mkdir -p /data/db
```
4. Change the permissions
```
$ chmod 777 /data
$ chmod 777 /data/db
```
5. To check the permissions
```
$ ls -ld /data/db
```
6. Go to where mongodb/bin directory is. Then copy its contents to `/usr/local/bin`
```
cp * /usr/local/bin
```
7. Check the path
```
$ which mongod
```
### Importing files to mongo
Example, if you have `events.json` file.
```
$ mongoimport --db mydb --collection events --type json --file events.json --jsonArray
```