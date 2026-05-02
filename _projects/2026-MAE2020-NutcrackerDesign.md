---
layout: project
title: MAE 2020 Nutcracker Design
description: Designing a nutcracker to be able to crack macadamia nuts
image: /assets/images/MacadamiaNutsPhoto.jpg
---
<br>

### Problem Statement and Objective

In this design project I was tasked with designing a simple lever nut cracker that is able to crack a macadamia nut. 

### Constraints and Input Parameters

In this design I aimed for a target force at the nut of around 2.2 kN which I pulled from a study about monkeys cracking nuts [1]. For the average size of the nuts I aimed for around 15 mm diameter based on a study about the mechanics of breaking macadamia nut shells [2]. Finally for the force a human can exert we used a force of 250N based on a survey of human grip strength [3]. 

### Approach to the Problem

First I calculated the mechanical advantage that the nut cracker would need to provide. This was a simple calcuation of the force at the nut divided by the force at the handles. This gave a value of  2200N/250N = 8.8. For simplicities sake I decided to round this up to 9. This means that since our design is a simple lever we must have the handles 9 times farther away from the pivot point than the contact point of the nut. I decided that since the nut is about 15mm in diameter that the contact point should be around 2 cm away from the pivot meaning that the handles would have to be 18 cm away from the pivot point. Finally at the contact patch with the nut I added a sort of indent. This was done to ensure that while cracking the force on the nut would be only crushing it and not trying to force it out of the nut cracker. 

### Diagram of the Nut Cracker Design
<img src="/portfolio-victorguimbretiere/assets/images/Nutcracker.png" width="90%">

### Discussion on Usability of Design

This nutcracker is while usable probably a little big. In order to get the needed mechanical advantage the nutcracker ends up being quite big and somewhat unwieldy. A design that uses some sort of mechanism to further amplify the input force would probably allow for the design to be made more compact and less unwieldy

### Investigation of Handle Deflection
The handles on this nutcracker can be modeled as two straight bars that are pinned at the point at which they intersect and on rollers at the point at which the macadamia nut touches the bars (See diagram)
<img src="/portfolio-victorguimbretiere/assets/images/Deflectioncrack.png" width="90%">
Looking at the diagram we can see that the bars will be fixed at the pin and at the roller and thus we know that the maximum deflection of the bars will be at the end of the bars where the force is being applied. 

### Designing to Mitigate Deflection
To design the handles so that the deflection is less than 2% of the length of the handles the first step is to calculate the formulas for the deflection of the beam given the supports we are modeling the system with.
We can model the declection of the beam using the equation $$ y(x) = \frac{1}{EI}(\frac{Fx^3}{6} + \frac{0.09Fx^2}{2}+0.091Fx) $$   
I decided to use titanium because of its high Young's modulus and its low density to make the nutcracker as mass efficent as possible. Pluging in our value for F and x=0.18 (The end of the beam) as well as our maximum deflection which is $$0.18*0.02 = 0.0036$$ or $$3.6mm$$ and Youngs modulus for titanium which is 115 GPa[4] we can solve for the needed moment of inertia. 
$$ 0.0036 = \frac{1}{115GPaI}(\frac{250\cdot0.18^3}{6} + \frac{0.09\cdot250\cdot0.18^2}{2}+0.091\cdot250\cdot0.18) $$    
$$I=1.13587\times10^{-8}$$    
In order to make the nutcracker ergonomic and also resistant to bending I decided to use an elipese with the high being 2 times the width as the profile of the handle. Knowing that the moment of inertia about the height is $$I=\frac{\pi wh^3}{64}$$ and knowing that $$w=\frac{h}{2}$$ we can find that    
$$1.13587\times10^{-8}=\frac{\pi h^4}{128}$$     
$$h=26mm$$        
$$b=13mm$$     
This information combined allows us to have the following rough model of the nutcracker:      
<img src="/portfolio-victorguimbretiere/assets/images/nutcreackerrender.PNG" width="90%">

### Citations

[1] Schrauf et al. Do capuchin monkeys use weight to select hammer tools, Anim Cogn 11, 413–422 (2008). https://doi.org/10.1007/s10071-007-0131-2  
[2] Sesana, R., Delprete, C., & Sangermano, M. (2019). Mechanical behavior of Macadamia nutshells. Procedia Structural Integrity, 24, 829–836. https://doi.org/10.1016/j.prostr.2020.02.088   
[3] Bardo, A., Kivell, T. L., Town, K., Donati, G., Ballieux, H., Stamate, C., Edginton, T., & Forrester, G. S. (2021b). Get A grip: Variation in human hand grip strength and implications for human evolution. Symmetry, 13(7), 1142. https://doi.org/10.3390/sym13071142
[4]Beer, F. P., Johnston, E. R., DeWolf, J. T., & Mazurek, D. F. (2021). Statics and mechanics of materials. McGraw-Hill Education. 



