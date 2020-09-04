# bv2rgb
A simple class for obtaining the colour temperatures of stars, used in my universe simulation.

*Colour temperature is just a simple gradient, right?* Well not exactly, as I found out from this [Stack Overflow post](https://stackoverflow.com/questions/21977786/star-b-v-color-index-to-apparent-rgb-color), mapping a star's B-V index (colour temperature) is way more complicated than I thought. 

I decided to store the colour mappings from the data of [this site](http://www.vendian.org/mncharity/dir3/starcolor/details.html) as a Java class, which also contains a function to retrieve the closest entry given a B-V index. It's quick and dirty, but it works.

## Usage
Initialize a `StarColor` object using:
```java
StarColor sc = new StarColor();
```
To convert B-V index of a hot blue star (bv=-0.4) to RGB, call:
```java
StarColorInfo rgbVals = sc.bv2rgb(-0.4);
print(rgbVals.r); // 155
print(rgbVals.g); // 178
print(rgbVals.b); // 255
```
