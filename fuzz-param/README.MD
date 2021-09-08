### Crawled parameter fuzz

crawlin parametes and fuzz with my jaeles signatures.

### Instruction:
### crawl and Scan

* Add this function in .bashrc file

First need download and install htmlattribs by tomnomnom from repository

https://github.com/tomnomnom/hacks/tree/master/htmlattribs

```
# Parameter scanner with Jaeles
checkparam(){
for i in $(cat $1); do
        curl -sk "$i" | htmlattribs name input | tee params.txt
        jaeles scan -v -s ~/path_To_Jaeles_Signature/.* -p "dest=Your_Collaborator_Server" -u "$i"
        rm params.txt
done
}

```

* collect urls with your favorite tool. "Burp, gospider, hakrawler"
* check urls which includer "<input> tag" with ffuf

```
ffuf -u FUZZ -w urls.txt -mr "<input" -s | tee crawled.txt
```

* Scan collected urls, command for terminal

```
checkparam crawled.txt
```
