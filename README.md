# BUMP - AI

![](https://github.com/Abusayid693/Hack-PSU/blob/main/BUMP%20AI%20Logo.JPG)

# Brief

**It's becoming harder for drivers to slow their speed with over 90% admitting that they drive over the speed limit, putting children's lives, who are not as road smart as adults in danger. Bump AI is the solution to this problem.**

---
![Logo](https://i.imgur.com/KSrMMFg.jpg )
---
Today, roads have become more dangerous with drivers being able to be distracted very easily through phones, loud children, and music. This means that school zones and areas children tend to spend their free time in are becoming a danger zone putting their lives at risk. In 2011, it was reported that over 2,000 children died or were severely injured from road accidents in the UK - **this needs to come to an end.** We desperately need to find a way to slow down driver's down.


# What is Bump AI
---
**Bump AI** is an automated speed controlling system that allows drivers to slow down via tracking their speed and raising speed _bumps_ out of the ground if they are driving over the limit of the area. We use computer vision to analyze an object's speed and times.

#Creation Process
---
###Detection

Our methods use the motion of a vehicle to separate it from a fixed background image. This method can be divided into three categories 
- The method of using background subtraction
- The method of using continuous video frame difference.
- The method of using optical flow.

---
 Using the video frame difference method, the variance is calculated according to the pixel values of two or three consecutive video frames. Moreover, the moving foreground region is separated by the threshold . By using this method and suppressing noise, the stopping of the vehicle can also be detected . When the background image in the video is fixed, the background information is used to establish the background model. Then, each frame image is compared with the background model, and the moving object can also be segmented.

 A video is a set of frames stacked together in the right sequence. So, when we see an object moving in a video, it means that the object is at a different location at every consecutive frame, the pixel difference of the current frame from the previous frame will highlight the pixels of the moving object, each pixel in grayscale image are assigned one of the two values representing black and white colors based on a threshold.

![Haar Cascade](https://i.imgur.com/u3cul0B.jpg)

---
###Speed Estimation

To estimate the speed timestamps of a vehicle are collected at waypoints ABC or CBA. From there, our speed = distance / time equation is put to use to calculate 2 speeds among the 3 waypoints. Speeds are averaged together and converted to km/hr and miles/hr. In order to get the distance we compare two consecutive frames in terms of pixel difference (approximate ). 

![](https://i.imgur.com/jAC0KrK.png)
---
**The following equations represent our algorithm:**

![](https://i.imgur.com/EST0CLJ.png)
---

# Step-by-Step
---
**1.** A car will drive past our system

![Cars](https://i.imgur.com/dMPvsx1.jpg)
---
**2.** The system will detect the object

![Detection](https://i.imgur.com/fI0lqoW.jpg)
---
**3.** Speed will be logged

![speed detected](https://i.imgur.com/oAnpwUT.png)
---
**4.** If the colour is green then the vehicle is within the speed limit 

![Good Cars](https://i.imgur.com/4N5E1MH.jpg)
---
**5.** If the colour is red then the car is speeding and a **speed bump is activated**

![Bad Cars](https://i.imgur.com/xtEydxZ.jpg)
---
**6.** Speed bump being activated shown below

![Bump](https://i.imgur.com/t9cFO4e.jpg)
---
![Bump](https://i.imgur.com/XKV878t.jpg)

# Our Key Takeaways
---
###Technologies that we used :

![technologies used](https://i.imgur.com/8Tr9LSu.png)

### Accomplishments that we're proud of
---
We are happy that we were able to complete this project within the limited time-space without running into too many problems as our previous items have. We are also proud of this project because we really believe it has big potential to make huge social changes in society. We hope that our AI-powered system will be able to reduce the number of adolescent fatalities as well as allowing school to be a safer place for children to commute to - without having to fear the roads.

### What we learned
---	
Over the past few hours, we have learned how to communicate effectively as well as using deep learning to develop our product.

### What's next for Bump AI
---
Our system has a lot of versatility but to even start effectively in the future, we plan to implement our system physically onto roads and test them out within school areas to see if they have a useful effect on student's safety and driver's speed. We’ve all experienced unsafe, fast-moving vehicles operated by inattentive drivers that nearly mow us down. We feel almost powerless. These drivers disregard speed limits, crosswalk areas, school zones, and “children at play” signs altogether, they speed up almost as if they are trying to catch some air.

##References
---
https://www.analyticsvidhya.com/blog/2020/04/vehicle-detection-opencv-python/
https://www.pyimagesearch.com/2019/12/02/opencv-vehicle-detection-tracking-and-speed-estimation/

---
