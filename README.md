# GAME_PROGRAM-EX--4

# Attach Rifle with character mesh and implementation bullet spawn from Rifle

# AIM
To create an aiming system (attach and aim a rifle with a character) in Unreal Engine,you’re using a third-person character and a rifle skeletal mesh.

# Procedure
# 1.Attach the Rifle to the Character
Import the Rifle Skeletal Mesh into Unreal Engine. Open your Character Blueprint (e.g., BP_ThirdPersonCharacter). In the Components tab: Add a Skeletal Mesh or Static Mesh component (name it Rifle). Set its Skeletal Mesh to your rifle asset.

# 2.Attach the Rifle to a socket on the character’s skeleton:
In the Rifle component, set the Parent Socket to something like hand_r (right hand socket).

manually attach in Event Graph:

Rifle->AttachToComponent(Mesh, FAttachmentTransformRules::SnapToTargetNotIncludingScale, "hand_rSocket");

# 3. Add Aiming Mechanism
Create a Boolean variable called IsAiming. Set up Input in Project Settings: Go to Edit > Project Settings > Input. Add an Action Mapping named Aim (e.g., Right Mouse Button).

# 4. Adjust Camera When Aiming
Add a Camera Boom and Follow Camera.
In Event Graph:
When IsAiming = true, zoom the camera in (FOV) and slightly shift it over the shoulder.

# Output

<img width="560" height="450" alt="515038630-8c8cd3e2-d7a5-41f7-b21f-5b959c962420" src="https://github.com/user-attachments/assets/8935750b-30d0-40f5-974d-dc7a7f4d52e8" />

<img width="565" height="427" alt="515038852-f846411d-7ea1-4086-a9ae-6bd128931d24" src="https://github.com/user-attachments/assets/160a3a4a-6f58-409b-a8d4-fb33f33f934e" />

# Result

Attach Rifle with character mesh and implementation bullet spawn from Rifle is successfully done.


