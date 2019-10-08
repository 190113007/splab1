## splab1 - shell scripting

###### \[deadline is week07-08 labtime, October 07-18, 2019\]

### Aim
- To master basic and not-so-basic UNIX/Linux shell commands and scripting.

### Task

You are to write shell-script that will process an [access log file](http://vseloved.github.io/spos/log.txt.zip) of Apacher web-server and output some information to the console (depends on your [variant](./variants)). Your script should use only standard command line tools like `cut`, `paste`, `head`, `tail`,`cat`, `tac`, `wc`, `join`, `grep`, `sort`, `sed`, `uniq`, `awk`, `expr`, et cetera, and should not use other programming languages like `C`, `Perl`, `Python` etc. The file consists of records. Each line has only one record. A record has the following format:

```
<client host> - - [<timestamp with timezone>] <HTTP-request line (type, URL, version)> <Code of HTTP-response> <Number of sent bytes or '-', if the response is empty> <Referer string ('-'  means direct request without referer)> <Client info (browser, application)>
```

Example of a record:
```
host-24-225-218-245.patmedia.net - - [01/Oct/2006:06:33:45 -0700] "GET /example/example.atom HTTP/1.1" 304 - "-" "NetNewsWire/2.0b37 (Mac OS X; Lite; http://ranchero.com/netnewswire/)"
```
Interpretation of the above record:
* On **01/Oct/2006:06:33:45 -0700** from the host **host-24-225-218-245.patmedia.net** via **HTTP/1.1** protocol
was issued a **GET** request to get the resource at **/example/example.atom**. Response code from server is **304**. Such a response has 0 sent bytes (**-**). Referrer is empty. Client used **NetNewsWire/2.0b37** and client OS was **Mac OS X**.

### Your Solution

Your solution should be stored in file [./solution/top](./solution/top). To run the solution make it executable by `chmod +x top10` command. Your solution will typically include 2-7 lines of commmands. A one liner solution is also possible but probably it will look ugly (my subjective point of view).

Your solution will be crossvalidated on sub-chunks of the `log.txt` file provided above. You can split your `log.txt` into chunks using `split` command. Our testing script will run your solution and compare its output with our "correct" outputs by `diff` command. Thus your solution will be judged.

_Best of luck!_

##### Credits
* The task was adopted and adapted from http://vseloved.github.io/spos. All credits go to Vsevolod Dyomkin.
* Variants in Russian can be found [there](http://vseloved.github.io/pdf/var-sh-ru.pdf)
