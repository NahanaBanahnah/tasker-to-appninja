# Tasker To AppNinja
Tasker Setup for Instant TP on Coping Cords. 

### Part 1 - The Task
* Under Tasks Click the + Button to start a new task
* Give it a name
* In **Task Edit** Again Click + Button to add an Action

#### Action 1 - Variable Set
* Set **Name** to %clip
* Set **To** to %CLIP

![Step One](/img/1.png)

#### Action 2 - Variable Split
* Set **Name** to %clip
* Set **Spliter** to ,

![Step Two](/img/2.png)

#### Action 3 - Send Intent
* Set **Action** to theappninjas.gpsjoystick.TELEPORT
* Set **Extra** to lat: %clip1
* Set **Extra** to lng: %clip2
* Set **Target** to Serive
* Under **If** Click + to Add an If
 * Set the first empty line to %clip
 * Click the **~** and select **Matches Regex** from the Popup **~** should change to **~R**
 * Set the second empy to line ^[-+]?([1-8]?\d(.\d+)?|90(.0+)?),\s*[-+]?(180(.0+)?|((1[0-7]\d)|([1-9]?\d))(.\d+)?)$
 
![Step Three](/img/3-1.png)
![Step Three](/img/3-2.png)

#### Action 4 - Flash - Optional
This will flash the cords on the screen to ensure they were received. You can skip if you'd  like
* Set **Text** To %clip
* Repeat the steps in **Action 3** for setting the If

![Step Four](/img/4.png)


**Full Task**

![Full Task](/img/full_task.png)


### Part 2 - The Profile
* Under Profiles Click + Button to add a profile
* Give it a name
* Select **Event**
* Use **Variable Set**
 * In the Edit Event for Variable Set set **Variable** to %CLIP
* Attach the Process to the Task created above 

### Taking It Further - PC To Phone Clipboard
This will allow you to copy cords on your PC and send, then instant teleport on your phone.
* [Add To Chrome](https://chrome.google.com/webstore/detail/clipbrd-beta/febnkhppinonnjgfjdigiipdajophkkk)
* Then [Get On The PlayStore](https://play.google.com/store/apps/details?id=com.clipbrd&hl=en_US)

### Taking It EVEN Further - Mirror & Control Android on PC
* [Download From scrcpy Git](https://github.com/Genymobile/scrcpy)










