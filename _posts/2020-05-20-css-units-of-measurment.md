---
layout: post
title: CSS Units of Measurement
subtitle: From rem📏 to ms⏳
tags: [Sass, CSS]
author: Ephraim Atta-Duncan
comments: True
---

For good and better styling of webpages and apps, good measurment is key. CSS has a whole lot of units for measurment, some are mostly used and some are rarely used. In this post, I'll list out all the known CSS units of measurement and thier respective equivalent in other units.

CSS units are in two forms. They are;

- Absolute Measurement
- Relative Measurment

#### Absolute Measurment Units

Absolute measurment units are units that is fixed. The unit does not changing depending on the any other unit. They remain constant always no matter the device, or width the device is previewed on. Examples are percentage, pixels, points, etc.

#### Relative Measurment Units

Relative measurent units are units that are always changing. They are different depending on the device or the width at which it is being previewed. They are not constant and are always at all times thier value is relative to other units. Examples are rem, em, vh, vw, etc.

### List of Absolute Measurment Units.

1. **% (percentage)** <br> Percentage is a fraction per hundred of a given unit. They do not change and remain constant. For example, if you have a div with equal width and height with a border set making it a square. To get a circle out of the square, you set the border radius to 50%. The 50% will be 50% of whatever width or height you specified and that value will never change.

```css
.profile-head {
  width: 100px;
  height: 100px;
  border: 1px solid #000;
  border-radius: 50%; /* 50px */
}
```

2. **cm (centimeter)** <br> Centimeter on a normal meter rule can also be used in css. It is another absolute unit which the value remains constant, however, it is rarely used.

3. **in (inch)** <br> Inch is another fixed unit. `1in = 2.54cm`

4. **mm (millimeter)** <br> A millimeter is a tenth of a centimeter. `1mm = 0.1cm`. It is also absolute and also rarely used these days.

5. **pc (pica)** <br>
