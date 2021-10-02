# Responsive CSS

Web is by default responsive. Whenever you find it isn't, it must be something you've done on CSS to cause the issue.

Reference: https://courses.kevinpowell.co/courses/conquering-responsive-layouts/

# Day 1 - using percentages for widths and avoid defining heights

- Percentages vs Fixed widths  
  Always use percentage than defining fixed widths to maintain responsiveness
- Percentages on the child means the relative portion to parent component
- Why it's a good idea to avoid heights  
  This is a general rule. There are times when you want to use height, but for the most part, they cause more issues than they solve. If you really need to use height, use `min-height` instead.
- The only issue with this is, at large screens, things can get too big.  
  That's why we can set `max-width` that can help us out!

# Day 2 - Relative units

Reference

- Em vs rem - https://youtu.be/_-aDOAMmDHI
- Why you shouldn't set font-sizes using em - https://youtu.be/pautqDqa54I

Takeaway

- em takes reference to the parent component. Say A is B's parent component. We set 16px in A component, if we set font size to be 1.5 em in B component, the text will be a font size of 24px.
- For font size, em works as said above. Yet for margin / padding, they take reference to the font size of the current component. Following up the above example, when you have "font-size: 1.5em", and set "margin: 1em", then the margin is 24px.
- Rem takes reference to the root element / html. html has a default font size of 16px. So 1 rem is 16px by default. Some will set "font-size: 62.5%", i.e. 16 \* 0.625, 10px, to set default font size to 10px and thereafter 1rem equals to 10px.
- Rem should be used for font size as they always take reference to the root element / html instead of the parent component which could cause a lot of issues.
- For padding / margin, if you prefer them to be responsive to the font size of the element, you can use em. For example, you set "margin: 1em". When you set a larger font size, say, from 1 rem to 1.5 rem, the respective margin / padding will also increase in size by 1.5

# Day 3 & 4 - More on relative units and solutions to challenge 01

Reference

- vh, vw, vmin, vmax - https://youtu.be/IWFqGsXxJ1E

Takeaway

- vw is viewpoint width while vh is viewpoint height  
  e.g. 1vw means 1% of the viewpoint width
- vw vs percentage ?  
  vw take reference to the existing screen size of user while percentage takes reference to the parent component
- vmin is the shorter of viewpoint height and viewpoint width  
  e.g. height: 600px and width is 800px => 10 vmin means 60px
- vmax is the opposite of vmin  
  following the above example, 10 vmax means 80px
- Cautions when using viewpoint units
  Using them for font-size, and while cool, there are some accessibility issues with doing so, so I wouldn't suggest it unless it's just for a personal project of yours.
