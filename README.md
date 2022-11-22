# Notes-of-3D-imaging-course

# Stereo triangulation 
If you have two cameras fixed at known positions (three parameters) and orientations (another three parameters), and take one photo of one same object or scene through each camera, you can know depth information of the object or scene, on another harsh and demanding condition: known correspondence between the two images, namely, the how to find the corresponding pixel at one camera given any pixel at another camera. Triangulation relation can be simply applied for such depth detection task and simplifying any camera as pinholes and employing basic geometry can deduce the formula for distances. Having two cameras means stereo and triangulation is the basic principle, so stereo triangulation is named.

The correspondence is a very challenging task for computer vision and there are several ways to address or bypass it.
1. Observing a point source

In this case, the correspondence relation is not a problem at all. The application can be the distance measurement of stars in the universe. The error of stereo trangulation (formula?) is inversely proportional to the distance between two cameras and proportional to the distance/depth to be measured. Therefore, we want to have large camera distance if we are to measure distance of object far away. People make use of earth and sun orbit to have very large camera distance and measure stars ?? how far away?

for very long distance, triangulation becomes invalid, even though sub orbit is used. In that spectrum, standard candles start functioning. People somehow know the intensity of these candles (physical model and validation through triangulation inrelatively smaller distance) and the attenuation reflects the distance. 

Application: measure distances in the universe, triangulation (make use of earth orbit and sun orbit) and standard candles(RR-Lyrea, sepheid star, supernova)
The error of trangulation (formula?) is inversely proportional to the distance between two cameras and proportional to the distance/depth to be measured. Therefore, for very long distance, triangulation becomes invalid, even though sub orbit is used. In that spectrum, standard candles start functioning. People somehow know the intensity of these candles (physical model and validation through triangulation inrelatively smaller distance) and the attenuation reflects the distance. 

1. shape from silhouettes and shadowgrams

2. space carving


3. stereo vision



