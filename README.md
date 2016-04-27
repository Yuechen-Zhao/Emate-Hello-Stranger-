1. Introduction
This Twitter Map project allows users to select a certain keyword in a dropdown menu, then the geographical coordinates of where the selected keyword has appeared would be shown on the Google Map.

2. Project Main Components
Out project has three main parts. First of all, download the Elasticsearch software from online and keep it running. Then, run our loader-es.py to put the Twitter real-time streaming data onto cloud. These geographical data are stored in JSON format, where one word corresponds to all locations that it has appeared. The second main part of our project is application.py, which renders the html file in the templates folder, extract data from cloud, and transfer data to the html file. The third main part is mainTwitterMap.html file, which is the main html file that displays the Google Map, receive the geographic coordinate data from application.py, and draws the points on map.

3. Project Bugs and Exceptions
Since we have a problem with getting data points from one instance to another, we tried instead running all three main files in a single EC2 instance. Thus if you try to access the public IP address of this instance: http://52.23.195.84:5000, you would be able to see the correct result. However, we also tried to set up through ElasticBeanstalk, but we had a problem transferring data from the putting-data instance to the getting-data instance, you would be able to see the map but not any points if you try to access through: http://flask-env1.bv3ymhtph6.us-west-2.elasticbeanstalk.com/.

4. Important Note
If you could not access through http://52.23.195.84:5000, that means this instance is now terminated or the public IP has changed after we closed the instance, please email us for an in-person demonstration.
