# ArthrexAR_Assignment
This is a Augmented Reality (AR) Image tracking app which demonstrates creating particle effects overlay on top of an image. The app tracks an image in the scene and projects particles which inherit image characteristics like shape and colours. Here we can use any any sample image of our choice for image tracking. And then Projected interactive art with particles which inherit image characteristics. 

I have used the beautiful kingfisher bird image for this project.

![andrew-pons-lylCw4zcA7I-unsplash](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/58f281d0-f047-4149-a1b9-0bf76466e2d2)

## Unity Version:
- Unity Editor 2021.3.14f1
* UnityHub 3.5.0
## Dependencies & External Tools:
Make sure you have all the below dependencies setup with this project.
- Java JDK 
- Android SDK
- Android NDK

![External Tools](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/9e48d140-be3b-4703-afdd-77599d20a5de)

##  This project depends on below Unity packages:
- [AR Foundation] (https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@5.1/manual/index.html) . For this project, AR Foundation Version 4.2.8
* [Google ARCore XR Plug-in on Android] https://docs.unity3d.com/Packages/com.unity.xr.arcore@5.1/manual/index.html. For this project Version 4.2.8

## How to use this AR Project
- Connect your android device to the system.

- You can build this project directly to any Android device. Once you build and run this app, ArthreX1.0 app will be installed on your device.

- You can test this app by opening the ArthreX1.0 app from your Andoid device. The app start running and opens an AR camera view, just show it to the kingfisher bird picture used and it will project the particle effects as shown below.
  
  ![image](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/83a9b4d8-fc2b-4093-8f11-1db26e4b7efa)


## To build to device, follow the steps below:

- Install Unity 2021.3.14f1 and download this repository.

- Open the Unity project at the root of this repository.

- Connect your android device.

- Make sure you enable the debugging option enabled on your android device.

- Enable the Developer option enabled.

- Build and run on device

As with any other Unity project, go to Build Settings, select your target platform to Android, and build and run this project. Make sure that, you have all the above dependencies setup before doing this step.

![image](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/562e7c3e-13ae-4a41-95cc-732e8b314de4)

## Image Tracking using AR Approach - Use any image of choice for image tracking.
Created an empty sample scene, then added the Add the AR session and AR session Origin components in your scene. It contains a Camera and any GameObject s created from detected features, such as planes or point clouds.

In AR session Origin, Added the ARTrackedIMageManager script. The tracked image manager is a type of trackable manager and performs 2D image tracking.
The tracked image manager creates GameObjects for each detected image in the environment. Before an image can be detected, the manager must be instructed to look for a set of reference images compiled into a reference image library. It only detects images in this library.

In Assets, Created a Folder called MyReferenceLibrary, inside the folder create a Reference image library. The tracked image will be inserted here.
![image](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/30a65714-5940-40cc-8cc5-d08e1a98a8db)

Go to AR session Origin and in the ARTrackedIMageManager, add the referenceImage (sparrow)
![image](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/35954fb8-4087-4c27-9f60-d4c3e2667b68)

Also add the sparrow image to that ReferenceimageOject.
![image](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/baab5a0d-310e-45c4-b7e2-9bfc4a50a870)          

GIve the name to the added image to sparrow. And specify the physical size and check the keep the texture at run time.
![image](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/353b9dc5-2591-4165-8fb4-0fa2134bb1f4)

## Project interactive art with particles which inherit image shape - Approach

There are various approaches we can follow in order to create the particles which inherit image charachterstics. 
For Example, create particles using below techniques and reuse that as a prefab. 

- Particle effects with Texture sheet animation technique , 

- Particle effects with the sprite renderer.
  
- Particle effects with Mesh renderer.
  
For this project, i have used the particles sprite renderer. 

Now to create sprite, 
- First i took the bird image as a reference to create the particle effects.
- Imported the bird image into the scene. and the convert the image to sprite. Actually we can convert the image to sprite in unity itself.

#### Importing an image into Unity.

I would like to import only the bird without any background. To eliminate the background colours from the image, using photoshop i removed the RGB value and saved it in a png format and them imported to Unity.

![image](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/d21468db-0fdc-4215-98ce-54b894b05fc7)

In Unity, I Creted an empty game object and added a sprite renderer to that empty game object, in the project files i named it as sparrow game object.
![image](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/ede54efa-b63c-418f-948e-93a3d07e37c3)

#### Coverting image into sprite in Unity.

I have selected the imported sparrow.png file in unity and converted into sprite.
![image](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/c0b42ea8-f2fd-4033-b671-2417d1c57710)

#### Create particle effects that inherits from image characterstics

In Unity, Project hierarchy - create a new particle system.
Now play with the particle properties to achieve the particle colours similar to image characterstics.

![image](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/ce723f39-8783-4534-91e5-e4f80264882c)

- Set emission properties:

![image](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/b9a86b34-dcec-4374-b3c4-6cb37684c4db)

- Set shape properties:
 
To achieve particles with the bird shape. I changed the shape to sprite renderer and added the sparrow game object.

![image](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/6f035709-a146-4424-a862-6d9d0d6a7ff1)

- Now, Play with particle colours:

![1](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/0cc4cd96-d906-4e55-8934-24e96269c765)

![2](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/94a95aa9-2cd5-489c-9dad-8a3e6d6f604d)

![3](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/bf68ce6f-9845-43e8-92f7-97af43f4b928)

![4](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/b1dfa46a-6bb0-4346-858a-c6b4ee242e3e)

- The Output Result:

To generate the particle colours along with the bird shape, just unselct/un-check the game object from inspector pane and this will provide the result with bird shape below.

![image](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/ec127266-1861-4ba9-8b9e-e29a9cf4b920)

Now we can reuse this particle system as a prefab and attach that prefab to the ARTrackedIMageManager scriptscript, so that particle effects will be generated that inherits from image characterstics.

Hoever, using a Sprite Renderer for particles in Unity may not provide the best result. Particle systems typically use textures as their source, not Sprite Renderers directly. Here's how we can achieve the effect like to track an image and generate particles that inherit the characteristics of the tracked image. :

## Image Tracking with Particles which inherit image characteristics - Approach
To achieve a particle system that inherits a characterstics of an image, 
you can use a technique called "Sprite-based Particle Emission." This approach involves using a grayscale image as an alpha map to determine where particles should be emitted in the particle system, creating a shape that matches the image. Here's how we can do it.

- You can test this app by installing the Arthrex_ParticleImageTracking.apk​ availabe in the ImageTrackingPaticle directory. The app start running and opens an AR camera view, just show it to the kingfisher bird picture used and it will project the particle effects as shown below.
- ![20230825_2343127379](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/8f607fd8-a01f-4b88-87ab-e8a517d7968a)
- Here is the steps i have followed to achieve the desired output: 

#### Prepare Your Grayscale Image:

- You'll need a grayscale image where the white areas represent where particles should be emitted and the black areas represent where particles shouldn't be emitted. You can create this image using graphic design software or obtain it from other sources.
Create a Particle System:

- Create a new GameObject or use an existing one to host the particle system.
Add a Particle System component to the GameObject.
#### Set the Material:

- Create a material for your particle system that uses the grayscale image as its alpha map. Here's how:
In your Project panel, create a new Material asset.
Select the material and in the Inspector panel, set the Shader to "Particles/Standard Surface."
In the Albedo section, assign the grayscale image to the Texture field.
#### Configure Particle System:

- In the Particle System component's Renderer settings, assign the material you created to the "Material" field.
#### Use the Alpha Map for Emission:

- In the Particle System component, go to the Emission module.
Set the Rate over Time to control the number of particles emitted per second.
Enable the "Use Meshes" checkbox.
In the "Mesh" dropdown, select "Sprite" to use the sprite's shape for emission.
Drag and drop the grayscale image into the "Texture" field. Unity will use this texture as an alpha map to determine where particles are emitted.
#### Adjust Particle System Settings:

- Adjust other particle system settings (such as size, speed, lifetime) to achieve the desired particle effect.
![image](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/581c218d-16e2-4181-8275-5a0304a771b8)

#### Create a Particle System Prefab:

- With your particle system GameObject selected, drag and drop it into the Assets panel to create a prefab.
Now, when you instantiate this prefab in your scenes, the Particle System will emit particles based on the shape of the grayscale image. The white areas of the image will emit particles, creating a particle system that inherits its shape from the image.

- Keep in mind that this technique provides a static shape for the particle emission. If you need more dynamic or complex shapes, you might need to use more advanced techniques or shaders. Additionally, experiment with the particle system settings to achieve the desired visual effect.
  
#### Here is the desired output we want to achieve, Mobile screenshots provided below:
![WhatsApp Image 2023-08-22 at 04 59 31](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/4180ef40-5811-4666-abd1-d07fefec15d7)
![20230825_2343127379](https://github.com/Feerojkumar/ArthrexAR_Assignment/assets/140662095/8f607fd8-a01f-4b88-87ab-e8a517d7968a)

## User interaction to move particle around and rebound back to original positions for static image. - Approach
Now let us move the particle around and make them to rebounce back to its origianl positions.
Using user input events along with physics forces and scripting. 

This combination will allow us to achieve the desired effect of moving particles around and having them rebound back to their original positions.
