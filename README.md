# Meta Eyetracking
This project implements eye tracking using the Meta Quest Pro.

## ✅ Prerequisites (Meta Developer Account)
To run this project, you **must have both a Meta (formerly Oculus) Developer Account and a Meta Quest Pro headset**.  
Quest Pro **Eye Tracking** requires developer-level permissions (app entitlements, device developer mode, App ID, etc.), and it is only supported on **Meta Quest Pro** hardware.

- Check the official **Meta Quest PC requirements**:  
  https://www.meta.com/ko-kr/help/quest/140991407990979/?srsltid=AfmBOoo2CimljJ_bfAZ9zlMjOGFweJjWBO8wnxGYBH0uR2aUTfXBrodk
- Follow the official **Unity setup (Movement SDK) – Getting Started** guide **in order**:  
  https://developers.meta.com/horizon/documentation/unity/move-unity-getting-started


1. Feature Introduction (What this script does)
The EyeGazeController script reads real-time gaze data from the OVREyeGaze component and applies it to another GameObject (here: arrow).
As the user looks around, the arrow rotates to point in the same direction as the user’s eye gaze.

2. Code Flow (How it works)
Start():
Retrieves the OVREyeGaze component attached to the same GameObject.

Update():
Checks if eye tracking is enabled.
Applies the eye gaze rotation (eyeGaze.transform.rotation) to the arrow GameObject.

3. How to Use It
Add the OVRCameraRig prefab to your scene.
Attach the OVREyeGaze component to the head/eye object.
Create an empty GameObject and add the EyeGazeController script.
Drag and drop a visual object (e.g., an arrow mesh) into the arrow field in the Inspector.
Run the app on a Meta Quest Pro with Eye Tracking enabled → the arrow will rotate following your gaze direction.
