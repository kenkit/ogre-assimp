# Readme
# Assimp -> Ogre adaptor

This code was originally from OgreAssimp Converter tool which can be found at 


Basic useful feature list:

 * Allows you to import any model into Ogre using Assimp without using any external mesh conversion tools.
 * Imports textures.
 * Imports Skeletons if any.
 * Imports animations.



# Sample Usage

You need to include 
```
#include <importer.h> //Don't forget to add the .cpp files into you project.
```
And also link against Assimp lib and boost filesystem.

```javascript
Importer naruto_mesh;
naruto_mesh.CreateMesh("NarutoMesh", "E:\\programming\\models\\Kakashi\\Kakashi.obj");//Create the mesh with name "NarutoMesh"
obstaclescene = mSceneMgr->getRootSceneNode()->createChildSceneNode("obstaclescene_" );
obstacle = mSceneMgr->createEntity("obstacle_", "NarutoMesh");//Create an entity from the mesh "NarutoMesh"
obstaclescene->attachObject(obstacle);

```

Props to  jacmoe and his [OgreAssimp converter](https://bitbucket.org/ogreaddons/ogreassimp/) and all those who were responsible for making OgreAssimp from which this code is based on.

### Discuss this project on Ogre Forum:

 * [Assimp->Ogre forum](http://www.ogre3d.org/forums/viewtopic.php?f=1&t=93145)

### Lastly:
Any and all improvements made on this code are welcome, we need to also port it over to Ogre 2.1.

Also I assume that we should first port the official OgreAssimp tool then we can work on this code, or whichever you preffer.
### Liscence:
This code use OgreAssimp Converter liscence.