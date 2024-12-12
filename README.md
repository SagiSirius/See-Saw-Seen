# See-Saw-Seen
Interactive installation, TouchDesigner, New Media Art, Columbia’s Digital Storytelling Lab, 2024 Fall

An interactive installation that explores the paradoxes of surveillance through three distinct phases: recognition, distortion, and erasure. As participants step into the gaze of a surveillance system, they experience an unsettling progression that questions identity, control, and visibility. 

## **How to Use**

### Starting the Program

1. Open the `.toe` file in TouchDesigner.
2. Ensure the correct webcam is selected in the top-left corner. If not, select your webcam manually.
3. Press the **"Reset"** button next to **"pulse"** to initialize the camera (if necessary).
4. Press the `ESC` key to exit playback mode and return to the editing interface.

### Interaction

1. The program activates when the webcam detects a face.
2. **Phase 1**: Your face appears as a model on the screen, mirroring your movements. 
3. **Phase 2**: After a few seconds, your image becomes clearer but begins to distort with noise, motion, and liquefaction effects.  
4. **Phase 3**: Further distortion intensifies, creating a chaotic and fragmented image.  
5. Step out of the camera\'s view to reset the program to its standby screen.

## **Technical Overview**

### **Face Recognition**

- **Tool**: [MediaPipe TouchDesigner Plugin by Torin Blankensmith](https://github.com/torinmb/mediapipe-touchdesigner)  
- **Purpose**: Detects and tracks facial features using a machine learning model. Controls the interactive face model and triggers transitions between phases.

### **Visual Effects**

- **Shaders**:  
  - [Original Shader by Airtight](https://www.shadertoy.com/view/MtXBDs) 
  - [Distortion Effect by Md2GDw](https://www.shadertoy.com/view/Md2GDw)  
- **Integration**: Custom shaders imported into TouchDesigner to generate real-time noise, blurring, and displacement effects.  

### **Transitions**

- Phase transitions are controlled using **CHOP trigger components** and smoothed with **filters**, ensuring seamless switching between effects.

### **Rendering and Mapping**

- A **Grid structure** enables geometric instancing with UV mapping to project live video footage onto a particle-based effect.
- **Feedback elements** enhance depth and texture, adding to the chaotic and fragmented visuals.

### **Standby Screen**

- Composed of a pre-recorded transparent PNG facial image with added noise and text overlays.
- The system detects a face in the camera feed to trigger the program\'s start.

## **File Structure**

- `see-saw-seen.toe`: The main TouchDesigner project file.
- `documentation.pdf`: Detailed explanation of the technical implementation and project structure.
- `README.md`: Repository overview and usage guide.
