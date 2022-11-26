# Notes-of-3D-imaging-course

The goal is to detect 3D information, namely, 3D location of a dot cloud, from images taken in an imagin system consisting of objects/scene, cameras(pinm holes), and illumination. Geometric optics is frequently used.

Connecting one pixel at image plane with the camera pinhole gives one light ray and people want to find the object point along this ray.

# Stereo triangulation 
If you have two cameras fixed at known positions (three parameters) and orientations (another three parameters), and take one photo of one same object or scene through each camera, you can know depth information of the object or scene, on another harsh and demanding condition: known correspondence between the two images, namely, the how to find the corresponding pixel at one camera given any pixel at another camera. Triangulation relation can be simply applied for such depth detection task and simplifying any camera as pinholes and employing basic geometry can deduce the formula for distances. Having two cameras means stereo and triangulation is the basic principle, so stereo triangulation is named.

The correspondence is a very challenging task for computer vision and there are several ways to address or bypass it.
1. Observing a point source

In this case, the correspondence relation is not a problem any more. The application can be the distance measurement of stars in the universe. The error of stereo trangulation (formula?) is inversely proportional to the distance between two cameras and proportional to the distance/depth to be measured. Therefore, we want to have large camera distance if we are to measure the distance of an object far away, for which people make use of earth and sun orbit to measure distances from stars in the universe. However, universe is remarkably immense and the triangulation relation becomes invalid as the distance increases. In that distance spectrum, standard candles are used to as the substitution. People know the core energy of those candles and can measure the their intensity at earth. The intensity attenuation reflects light propagation distance. How do people know the core energy? At first, they somehow build physical models prediction the energy of those candles and saying the energy of the same kind of candles are the same. Then some of the candles are relatively close such that the triangulation relation still works, from which the proposed models can be validated. Three types of candles are RR-Lyrea, sepheid star, supernova.

2. Observing simple objects and focus on outlines: silhouettes and shadowgrams. The image is binary and you get the projection outlines. The light rays from one outline form one visual  hull. In silhouette, many cameras placed at known positions and orientations and create many profile images which forms many visual hulls, constraining the space to the object's 3D outlines. In shadowgram, many point sources are placed at known positions, images are taken and constraints of visual hull are obtained. The hull converges to the object outline.


3. Correspondence dimention reduction: epiploar line. As mentioned before, from one pixel, we can get one light array and the object point candidates are at this line. You have the second camera and you use it to take a photo of all thoes candinates. The photo is a line which is called epipplar line. In stereo, each pixel corresponds to an epipolar line which is totally determined by the imaging setup and not relevant to objects to be detected. Now the correspondence problem becomes an 1D searching.

2. space carving
This technique is between silhouettes and stereo. You put many known cameras in the scene and build constraints from the images to carving the space into the object or scene. 

Illumination coding--another way to search for the right candinate.

A simple case: The illumination is a known plane. The right candinate is the intersection of the candidate line with the illumination plane.

Binary coding: You project a pattern with binay black-white stripes to an object and take one image. You decrease the stripe period and take another image. Repeat this until you have n stripes. The n stripe means n planes about each of which you know two features: the spatial positon and a binary code. For each pixel of the camera, you also get a binary code (identity) and then you know which plane the candidate is at. 

Color coding: Similar to the binary coding. You project stripe pattern with wide spectrum. Each wavelength corresponds one plane.

Sinusoidal fringe patters: encode the illumination plane into phase of the fringte.

Phase measuring deflectometry: You use a camera to see sinusoidal fringt patterns (x and y separately) through a reflective specular surface to be detected. Starting from one pixel of the camera, you get a light ray. Then you use "phase of this pixel" to determine the incident light ray from the pattern to the specular surface, from which you know the normal/local gradient (x and y separately) at this reflection point. From local gradient field, somehow the global depth map can be retrieved. But there is an anbiguity regarding any planes parallel to the specular surface, from which different normals appears. Another camera can solve this and stereo vision appears again.

Space-time stero: a great way to provide correspondence realtion in stereo vision at a cost of temporal resolution. Given an period of unknown illumination and images taken in this period, each pixel of one camera forms a curve of intensity versus time and the corresponding pixel at another camera which has the same curve.  





