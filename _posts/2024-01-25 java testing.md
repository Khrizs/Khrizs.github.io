---
layout: post
title: Java Testing
categories: testing
tags: [testing]
---

# omg java

sphere data from just a radius?? no way impossible!
~~~java
import javax.swing.*;
import java.text.*;
class Main {
  public static void main(String[] args) {
    double sphereRadius,sphereDiameter,sphereCircumference,sphereSurfaceArea,sphereVolume; 
    String sphereRadiusInput = JOptionPane.showInputDialog(null,"What is the radius of the sphere?:");
    sphereRadius = Double.parseDouble(sphereRadiusInput);

    sphereDiameter = sphereRadius * 2;
    sphereCircumference = Math.PI * sphereDiameter;
    sphereSurfaceArea = 4 * Math.PI * Math.pow(sphereRadius, 2);
    sphereVolume = (4f/3f) * Math.PI * Math.pow(sphereRadius, 3);

    JOptionPane.showMessageDialog(null, "There sphere has a diameter of "+sphereDiameter+" units, a circumference of "+sphereCircumference+" units, a surface area of "+sphereSurfaceArea+" square units, and a volume of "+sphereVolume+" cubed units!");
    
  }
}
~~~

wowie
