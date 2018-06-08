# SelKubF

Prepare kubernetes config files for SeleniumGrid deployment.

Please find https://github.com/SeleniumHQ/docker-selenium for additional info.

Grid should consist of 1 hub node and 2 Filefox nodes.

Kubernetes related info:

 - namespace: selenium-grid;
 
 - memory limitation: 8Gb RAM.
 ______________________________________________________

Deploy Selenium Grid Hub:

    kubectl create --filename=selenium-hub-rc.yaml
 
Deploy Firefox  Nodes:

Now that the Hub is up, we can deploy workers.

2 Firefox nodes to match.

    kubectl create --file=examples/selenium/selenium-node-firefox-rc.yaml

Once the pods start, you will see them show up in the Selenium Hub interface.


