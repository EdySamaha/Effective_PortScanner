# Effective Penetration Testing tools
A collection of tools that can be used to test for potential security flaws in your systems.

Install dependencies by running `pip install -r requirements.txt` in your console

## Contents
* [Disclaimer](#disclaimer)
* Reconnaissance tools
  * [Port Scanner](#port-scanner)
  * [Web Path Finder](#web-path-finder)
  * [Web Fingerprint](#web-fingerprint)
* Anonymity tools
  * [Traffic Maze](#traffic-maze)
* Exploitation tools
  * [Web Input Tester](#web-input-tester)
* Automation
  * [Automated](#automated)

## Port Scanner
Supports Multi-threading, Windows and Linux OS, user-friendly. Shows open ports in desired range of any hostname/ip inputted

#### Usage:
Run the script in your console by writing `python PortScanner.py`
Then input the required parameters

## Web Path Finder
Extracts all links from a website.

Can also search for hidden paths using `defaultPathWordlist.txt`. However, beware that brute-forcing directories and files names on deployed servers is ILLEGAL and can get you in trouble.

#### Usage:
Run the script in your console by writing `python WebPathFinder.py`
Then input the required parameters

## Web Fingerprint
Work in progress. Finds technologies and headers used in a website.

#### Usage:
Run the script in your console by writing `python WebFingerprint.py`
Then input the required parameters

## Traffic Maze
Work in progress. Masks traffic by going through proxies and mixing headers.

#### Usage:
NOTE: This script is ONLY useful when imported and used in other scripts. And the function called MUST contain "proxy" and "headers" parameters WITHOUT passing them in the "args" or "kwargs" fields, as shown below.

Inside a python script: 
```python
import TrafficMaze, requests

#create the function you want
def tempfunction(url, proxy,headers):
    req=requests.get(url, proxies=proxy,headers=headers)
    print(req.content)
#then call 
TrafficMaze.useTrafficMaze(tempfunction, args=(url))
```

## Web Input Tester
Work in progress. Gets all forms and inputs from a specified url, then tests these inputs with a list of payloads from `WebInput_payloads.txt` for potential vulnerabilities.

#### Usage:
Run the script in your console by writing `python WebInputTest.py`
Then input the required parameters

## Automated
Runs all desired scripts in an automated fashion and generates a report with results acquired. You can modify the Configuration Bools inside the script to select what scripts to run.
You only have to input the target after running `python Automated.py` in console.


# Disclaimer
All information and code available in this repository are for educational purposes only. Use them at your own discretion. The authors of this repository cannot be held responsible for any damages caused or illegal usage of the information given.