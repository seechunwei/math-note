### Learning Outcomes

- Identify the equation of a parabola in standard form with given focus and directrix
- Identify the equation of an ellipse in standard form with given foci
- Identify the equation of a hyperbola in standard form with given foci

## Parabolas

A parabola is generated when a plane intersects a cone parallel to the generating line. In this case, the plane intersects only one of the nappes. A parabola can also be defined in terms of distances.

### Definition

---

> [!definition]
> A parabola is the set of all points whose distance from a fixed point, called the **focus**, is equal to the distance from a fixed line, called the **directrix**. The point halfway between the focus and the directrix is called the **vertex** of the parabola.

A graph of a typical parabola appears in Figure 3. Using this diagram in conjunction with the distance formula, we can derive an equation for a parabola. Recall the distance formula: Given point *P* with coordinates $\left(x_{1} , y_{1}\right)$ and point *Q* with coordinates $\left(x_{2} , \text{y}_{2}\right)$, the distance between them is given by the formula

 $d \left(P , Q\right) = \sqrt{\left(x_{2} - x_{1}\right)^{2} + \left(y_{2} - y_{1}\right)^{2}}$.

Then from the definition of a parabola and Figure 3, we get

 $\begin{aligned}d \left(F , P\right) & = & d \left(P , Q\right) \\ \sqrt{\left(0 - x\right)^{2} + \left(p - y\right)^{2}} & = & \sqrt{\left(x - x\right)^{2} + \left(- p - y\right)^{2}} .\end{aligned}$

Squaring both sides and simplifying yields

 $\begin{aligned}x^{2} + \left(p - y\right)^{2} & = & 0^{2} + \left(- p - y\right)^{2} \\ x^{2} + p^{2} - 2 p y + y^{2} & = & p^{2} + 2 p y + y^{2} \\ x^{2} - 2 p y & = & 2 p y \\ x^{2} & = & 4 p y .\end{aligned}$![A parabola is drawn with vertex at the origin and opening up. A focus is drawn as F at (0, p). A point P is marked on the line at coordinates (x, y), and the distance from the focus to P is marked d. A line marked the directrix is drawn, and it is y = − p. The distance from P to the directrix at (x, −p) is marked d.](https://s3-us-west-2.amazonaws.com/courses-images/wp-content/uploads/sites/4175/2019/04/09225330/CNX_Calc_Figure_11_05_003.jpg)

Figure 3. A typical parabola in which the distance from the focus to the vertex is represented by the variable $p$.

### Recall: Transformations of graphs

Given a function $y = f \left(x\right)$, the graph of $y = f \left(x - h\right) + k$ is shifted vertically by $k$ units and horizontally by $h$ units.

- If $k$ is positive, the graph is shifted up. If $k$ is negative, the graph is shifted down.
- If $h$ is positive, the graph is shifted right. If $h$ is negative, the graph is shifted left.

Note that the equation $y = f \left(x - h\right) + k$ is equivalent to $y - k = f \left(x - h\right)$.

In other words, if $y$ is replaced by $y - k$ and $x$ is replaced by $x - h$ in an equation, the graph shifts according to the rules above.

Now suppose we want to relocate the vertex. We use the variables $\left(h , k\right)$ to denote the coordinates of the vertex. Then if the focus is directly above the vertex, it has coordinates $\left(h , k + p\right)$ and the directrix has the equation $y = k - p$. Going through the same derivation yields the formula $\left(x - h\right)^{2} = 4 p \left(y - k\right)$. Solving this equation for *y* leads to the following theorem.

### theorem: Equations for Parabolas

---

> [!theorem]
> Given a parabola opening upward with vertex located at $\left(h , k\right)$ and focus located at $\left(h , k + p\right)$, where *p* is a constant, the equation for the parabola is given by
> 
>  $y = \frac{1}{4 p} \left(x - h\right)^{2} + k$.
> 
> This is the **standard form** of a parabola.

We can also study the cases when the parabola opens down or to the left or the right. The equation for each of these cases can also be written in standard form as shown in the following graphs.

![This figure has four figures, each a parabola facing a different way. In the first figure, a parabola is drawn opening up with equation y = (1/(4p))(x − h)2 + k. The vertex is given as (h, k), the focus is drawn at (h, k + p), and the directrix is drawn as y = k − p. In the second figure, a parabola is drawn opening down with equation y = −(1/(4p))(x − h)2 + k. The vertex is given as (h, k), the focus is drawn at (h, k − p), and the directrix is drawn as y = k + p. In the third figure, a parabola is drawn opening to the right with equation x = (1/(4p))(y − k)2 + h. The vertex is given as (h, k), the focus is drawn at (h + p, k), and the directrix is drawn as x = h − p. In the fourth figure, a parabola is drawn opening left with equation x = −(1/(4p))(y − k)2 + h. The vertex is given as (h, k), the focus is drawn at (h – p, k), and the directrix is drawn as x = h + p.](https://s3-us-west-2.amazonaws.com/courses-images/wp-content/uploads/sites/4175/2019/04/09225333/CNX_Calc_Figure_11_05_004.jpg)

Figure 4. Four parabolas, opening in various directions, along with their equations in standard form.

In addition, the equation of a parabola can be written in the **general form**, though in this form the values of *h*, *k*, and *p* are not immediately recognizable. The general form of a parabola is written as

 $a x^{2} + b x + c y + d = 0 \text{or} a y^{2} + b x + c y + d = 0$.

The first equation represents a parabola that opens either up or down. The second equation represents a parabola that opens either to the left or to the right. To put the equation into standard form, use the method of completing the square.

### Example: Converting the Equation of a Parabola from General into Standard Form

> [!question]
> Put the equation $x^{2} - 4 x - 8 y + 12 = 0$ into standard form and graph the resulting parabola.
> 
> Show Solution

Since *y* is not squared in this equation, we know that the parabola opens either upward or downward. Therefore we need to solve this equation for *y,* which will put the equation into standard form. To do that, first add $8 y$ to both sides of the equation:

$8 y = x^{2} - 4 x + 12$.

The next step is to complete the square on the right-hand side. Start by grouping the first two terms on the right-hand side using parentheses:

$8 y = \left(x^{2} - 4 x\right) + 12$.

Next determine the constant that, when added inside the parentheses, makes the quantity inside the parentheses a perfect square trinomial. To do this, take half the coefficient of *x* and square it. This gives $\left(\frac{- 4}{2}\right)^{2} = 4$. Add 4 inside the parentheses and subtract 4 outside the parentheses, so the value of the equation is not changed:

$8 y = \left(x^{2} - 4 x + 4\right) + 12 - 4$.

Now combine like terms and factor the quantity inside the parentheses:

$8 y = \left(x - 2\right)^{2} + 8$.

Finally, divide by 8:

$y = \frac{1}{8} \left(x - 2\right)^{2} + 1$.

This equation is now in standard form. Comparing this to equations for parabolas gives $h = 2$, $k = 1$, and $p = 2$. The parabola opens up, with vertex at $\left(2 , 1\right)$, focus at $\left(2 , 3\right)$, and directrix $y = - 1$. The graph of this parabola appears as follows.

![A parabola is drawn with vertex at (2, 1) and opening up with equation x2 – 4x – 8y + 12 = 0. The focus is drawn at (1, 3). The directrix is drawn at y = − 1.](https://s3-us-west-2.amazonaws.com/courses-images/wp-content/uploads/sites/4175/2019/04/09225336/CNX_Calc_Figure_11_05_005.jpg)

Figure 5. The parabola in \[link\].

Watch the following video to see the worked solution to Example: Converting the Equation of a Parabola from General into Standard Form.

![](https://www.youtube.com/watch?v=AF_0mpKk4-Y)

For closed captioning, open the video on its original page by clicking the Youtube logo in the lower right-hand corner of the video display. In YouTube, the video will begin at the same starting point as this clip, but will continue playing until the very end.

You can view the [transcript for this segmented clip of “7.5 Conic Sections” here (opens in new window)](https://oerfiles.s3.us-west-2.amazonaws.com/Calculus+II/Transcripts/7.5ConicSections255to490_transcript.html).

The axis of symmetry of a vertical (opening up or down) parabola is a vertical line passing through the vertex. The parabola has an interesting reflective property. Suppose we have a satellite dish with a parabolic cross section. If a beam of electromagnetic waves, such as light or radio waves, comes into the dish in a straight line from a satellite (parallel to the axis of symmetry), then the waves reflect off the dish and collect at the focus of the parabola as shown.

![A parabola is drawn with vertex at the origin and opening up. Two parallel lines are drawn that strike the parabola and reflect to the focus.](https://s3-us-west-2.amazonaws.com/courses-images/wp-content/uploads/sites/4175/2019/04/09225340/CNX_Calc_Figure_11_05_007.jpg)

Figure 7.

Consider a parabolic dish designed to collect signals from a satellite in space. The dish is aimed directly at the satellite, and a receiver is located at the focus of the parabola. Radio waves coming in from the satellite are reflected off the surface of the parabola to the receiver, which collects and decodes the digital signals. This allows a small receiver to gather signals from a wide angle of sky. Flashlights and headlights in a car work on the same principle, but in reverse: the source of the light (that is, the light bulb) is located at the focus and the reflecting surface on the parabolic mirror focuses the beam straight ahead. This allows a small light bulb to illuminate a wide angle of space in front of the flashlight or car.

## Ellipses

An ellipse can also be defined in terms of distances. In the case of an ellipse, there are two foci (plural of focus), and two directrices (plural of directrix). We look at the directrices in more detail later in this section.

### Definition

---

An **ellipse** is the set of all points for which the sum of their distances from two fixed points (the foci) is constant.

![An ellipse is drawn with center at the origin O, focal point F’ being (−c, 0) and focal point F being (c, 0). The ellipse has points P and P’ on the x-axis and points Q and Q’ on the y axis. There are lines drawn from F’ to Q and F to Q. There are also lines drawn from F’ and F to a point A on the ellipse marked (x, y). The distance from O to Q and O to Q’ is marked b, and the distance from P to O and O to P’ is marked a.](https://s3-us-west-2.amazonaws.com/courses-images/wp-content/uploads/sites/4175/2019/04/09225343/CNX_Calc_Figure_11_05_008.jpg)

Figure 8. A typical ellipse in which the sum of the distances from any point on the ellipse to the foci is constant.

A graph of a typical ellipse is shown in Figure 8. In this figure the foci are labeled as $F$ and $F^{′}$. Both are the same fixed distance from the origin, and this distance is represented by the variable *c*. Therefore the coordinates of $F$ are $\left(c , 0\right)$ and the coordinates of $F^{′}$ are $\left(- c , 0\right)$. The points $P$ and $P^{′}$ are located at the ends of the major axis of the ellipse, and have coordinates $\left(a , 0\right)$ and $\left(- a , 0\right)$, respectively. The major axis is always the longest distance across the ellipse, and can be horizontal or vertical. Thus, the length of the major axis in this ellipse is 2 *a.* Furthermore, $P$ and $P^{′}$ are called the vertices of the ellipse. The points $Q$ and $Q^{′}$ are located at the ends of the minor axis of the ellipse, and have coordinates $\left(0 , b\right)$ and $\left(0 , - b\right)$, respectively. The minor axis is the shortest distance across the ellipse. The minor axis is perpendicular to the major axis.

According to the definition of the ellipse, we can choose any point on the ellipse and the sum of the distances from this point to the two foci is constant. Suppose we choose the point *P.* Since the coordinates of point *P* are $\left(a , 0\right)$, the sum of the distances is

$d \left(P , F\right) + d \left(P , F^{′}\right) = \left(a - c\right) + \left(a + c\right) = 2 a$.

Therefore the sum of the distances from an arbitrary point *A* with coordinates $\left(x , y\right)$ is also equal to $2 a$ *.* Using the distance formula, we get

 $\begin{aligned}d \left(A , F\right) + d \left(A , F^{′}\right) & = & 2 a \\ \sqrt{\left(x - c\right)^{2} + y^{2}} + \sqrt{\left(x + c\right)^{2} + y^{2}} & = & 2 a .\end{aligned}$

Subtract the second radical from both sides and square both sides:

 $\begin{aligned}\sqrt{\left(x - c\right)^{2} + y^{2}} & = & 2 a - \sqrt{\left(x + c\right)^{2} + y^{2}} \\ \left(x - c\right)^{2} + y^{2} & = & 4 a^{2} - 4 a \sqrt{\left(x + c\right)^{2} + y^{2}} + \left(x + c\right)^{2} + y^{2} \\ x^{2} - 2 c x + c^{2} + y^{2} & = & 4 a^{2} - 4 a \sqrt{\left(x + c\right)^{2} + y^{2}} + x^{2} + 2 c x + c^{2} + y^{2} \\ - 2 c x & = & 4 a^{2} - 4 a \sqrt{\left(x + c\right)^{2} + y^{2}} + 2 c x .\end{aligned}$

Now isolate the radical on the right-hand side and square again:

 $\begin{aligned}- 2 c x & = & 4 a^{2} - 4 a \sqrt{\left(x + c\right)^{2} + y^{2}} + 2 c x \\ 4 a \sqrt{\left(x + c\right)^{2} + y^{2}} & = & 4 a^{2} + 4 c x \\ \sqrt{\left(x + c\right)^{2} + y^{2}} & = & a + \frac{c x}{a} \\ \left(x + c\right)^{2} + y^{2} & = & a^{2} + 2 c x + \frac{c^{2} x^{2}}{a^{2}} \\ x^{2} + 2 c x + c^{2} + y^{2} & = & a^{2} + 2 c x + \frac{c^{2} x^{2}}{a^{2}} \\ x^{2} + c^{2} + y^{2} & = & a^{2} + \frac{c^{2} x^{2}}{a^{2}} .\end{aligned}$

Isolate the variables on the left-hand side of the equation and the constants on the right-hand side:

 $\begin{aligned}x^{2} - \frac{c^{2} x^{2}}{a^{2}} + y^{2} & = & a^{2} - c^{2} \\ \frac{\left(a^{2} - c^{2}\right) x^{2}}{a^{2}} + y^{2} & = & a^{2} - c^{2} .\end{aligned}$

Divide both sides by $a^{2} - c^{2}$. This gives the equation

$\frac{x^{2}}{a^{2}} + \frac{y^{2}}{a^{2} - c^{2}} = 1$.

If we refer back to Figure 8, then the length of each of the two green line segments is equal to *a*. This is true because the sum of the distances from the point *Q* to the foci $F \text{and} F^{′}$ is equal to 2 *a*, and the lengths of these two line segments are equal. This line segment forms a right triangle with hypotenuse length *a* and leg lengths *b* and *c*. From the Pythagorean theorem, $a^{2} + b^{2} = c^{2}$ and $b^{2} = a^{2} - c^{2}$. Therefore the equation of the ellipse becomes

$\frac{x^{2}}{a^{2}} + \frac{y^{2}}{b^{2}} = 1$.

Finally, if the center of the ellipse is moved from the origin to a point $\left(h , k\right)$, we have the following standard form of an ellipse.

### theorem: Equation of an Ellipse in Standard Form

---

Consider the ellipse with center $\left(h , k\right)$, a horizontal major axis with length $2 a$, and a vertical minor axis with length $2 b$. Then the equation of this ellipse in standard form is

 $\frac{\left(x - h\right)^{2}}{a^{2}} + \frac{\left(y - k\right)^{2}}{b^{2}} = 1$

and the foci are located at $\left(h \pm c , k\right)$, where $c^{2} = a^{2} - b^{2}$. The equations of the directrices are $x = h \pm \frac{a^{2}}{c}$.

If the major axis is vertical, then the equation of the ellipse becomes

 $\frac{\left(x - h\right)^{2}}{b^{2}} + \frac{\left(y - k\right)^{2}}{a^{2}} = 1$

and the foci are located at $\left(h , k \pm c\right)$, where $c^{2} = a^{2} - b^{2}$. The equations of the directrices in this case are $y = k \pm \frac{a^{2}}{c}$.

If the major axis is horizontal, then the ellipse is called horizontal, and if the major axis is vertical, then the ellipse is called vertical. The equation of an ellipse is in general form if it is in the form $A x^{2} + B y^{2} + C x + D y + E = 0$, where *A* and *B* are either both positive or both negative. To convert the equation from general to standard form, use the method of completing the square.

### Example: Finding the Standard Form of an Ellipse

> [!question]
> Put the equation $9 x^{2} + 4 y^{2} - 36 x + 24 y + 36 = 0$ into standard form and graph the resulting ellipse.
> 
> Show Solution

First subtract 36 from both sides of the equation:

$9 x^{2} + 4 y^{2} - 36 x + 24 y = - 36$.

Next group the *x* terms together and the *y* terms together, and factor out the common factor:

 $\begin{aligned}\left(9 x^{2} - 36 x\right) + \left(4 y^{2} + 24 y\right) & = & - 36 \\ 9 \left(x^{2} - 4 x\right) + 4 \left(y^{2} + 6 y\right) & = & - 36.\end{aligned}$

We need to determine the constant that, when added inside each set of parentheses, results in a perfect square. In the first set of parentheses, take half the coefficient of *x* and square it. This gives $\left(\frac{- 4}{2}\right)^{2} = 4$. In the second set of parentheses, take half the coefficient of *y* and square it. This gives $\left(\frac{6}{2}\right)^{2} = 9$. Add these inside each pair of parentheses. Since the first set of parentheses has a 9 in front, we are actually adding 36 to the left-hand side. Similarly, we are adding 36 to the second set as well. Therefore the equation becomes

 $\begin{matrix}9 \left(x^{2} - 4 x + 4\right) + 4 \left(y^{2} + 6 y + 9\right) = - 36 + 36 + 36 \\ 9 \left(x^{2} - 4 x + 4\right) + 4 \left(y^{2} + 6 y + 9\right) = 36.\end{matrix}$

Now factor both sets of parentheses and divide by 36:

 $\begin{aligned}9 \left(x - 2\right)^{2} + 4 \left(y + 3\right)^{2} & = & 36 \\ \frac{9 \left(x - 2\right)^{2}}{36} + \frac{4 \left(y + 3\right)^{2}}{36} & = & 1 \\ \frac{\left(x - 2\right)^{2}}{4} + \frac{\left(y + 3\right)^{2}}{9} & = & 1.\end{aligned}$

The equation is now in standard form. Comparing this to the theorem equation gives $h = 2$, $k = - 3$, $a = 3$, and $b = 2$. This is a vertical ellipse with center at $\left(2 , - 3\right)$, major axis 6, and minor axis 4. The graph of this ellipse appears as follows.

![An ellipse is drawn with equation 9x2 + 4y2 – 36x + 24y + 36 = 0. It has center at (2, −3), touches the x-axis at (2, 0), and touches the y-axis at (0, −3).](https://s3-us-west-2.amazonaws.com/courses-images/wp-content/uploads/sites/4175/2019/04/09225345/CNX_Calc_Figure_11_05_009.jpg)

Figure 9. The ellipse in \[link\].

Watch the following video to see the worked solution to Example: Finding the Standard Form of an Ellipse.

![](https://www.youtube.com/watch?v=AF_0mpKk4-Y)

For closed captioning, open the video on its original page by clicking the Youtube logo in the lower right-hand corner of the video display. In YouTube, the video will begin at the same starting point as this clip, but will continue playing until the very end.

You can view the [transcript for this segmented clip of “7.5 Conic Sections” here (opens in new window)](https://oerfiles.s3.us-west-2.amazonaws.com/Calculus+II/Transcripts/7.5ConicSections671to953_transcript.html).

According to Kepler’s first law of planetary motion, the orbit of a planet around the Sun is an ellipse with the Sun at one of the foci as shown in Figure 11 (a). Because Earth’s orbit is an ellipse, the distance from the Sun varies throughout the year. A commonly held misconception is that Earth is closer to the Sun in the summer. In fact, in summer for the northern hemisphere, Earth is farther from the Sun than during winter. The difference in season is caused by the tilt of Earth’s axis in the orbital plane. Comets that orbit the Sun, such as Halley’s Comet, also have elliptical orbits, as do moons orbiting the planets and satellites orbiting Earth.

Ellipses also have interesting reflective properties: A light ray emanating from one focus passes through the other focus after mirror reflection in the ellipse. The same thing occurs with a sound wave as well. The National Statuary Hall in the U.S. Capitol in Washington, DC, is a famous room in an elliptical shape as shown in Figure 11 (b). This hall served as the meeting place for the U.S. House of Representatives for almost fifty years. The location of the two foci of this semi-elliptical room are clearly identified by marks on the floor, and even if the room is full of visitors, when two people stand on these spots and speak to each other, they can hear each other much more clearly than they can hear someone standing close by. Legend has it that John Quincy Adams had his desk located on one of the foci and was able to eavesdrop on everyone else in the House without ever needing to stand. Although this makes a good story, it is unlikely to be true, because the original ceiling produced so many echoes that the entire room had to be hung with carpets to dampen the noise. The ceiling was rebuilt in 1902 and only then did the now-famous whispering effect emerge. Another famous whispering gallery—the site of many marriage proposals—is in Grand Central Station in New York City.

![There are two figures labeled a and b. In figure a, the earth is drawn orbiting the sun, with January and July marked. The distance from the sun to the earth marked January is 147 million km, while the distance from the sun to the earth marked July is 152 million miles. In figure b, a room is shown with curved walls.](https://s3-us-west-2.amazonaws.com/courses-images/wp-content/uploads/sites/4175/2019/04/09225351/CNX_Calc_Figure_11_05_011.jpg)

Figure 11. (a) Earth’s orbit around the Sun is an ellipse with the Sun at one focus. (b) Statuary Hall in the U.S. Capitol is a whispering gallery with an elliptical cross section.

## Hyperbolas

A hyperbola can also be defined in terms of distances. In the case of a hyperbola, there are two foci and two directrices. Hyperbolas also have two asymptotes.

### Definition

---

> [!definition]
> A **hyperbola** is the set of all points where the difference between their distances from two fixed points (the foci) is constant.

A graph of a typical hyperbola appears as follows.

![A hyperbola is drawn with center at the origin. The vertices are at (a, 0) and (−a, 0); the foci are labeled F1 and F2 and are at (c, 0) and (−c, 0). The asymptotes are drawn, and lines are drawn from the vertices to the asymptotes; the intersections of these lines are connected by other lines to make a rectangle; the shorter axis is called the conjugate axis and the larger axis is called the transverse axis. The distance from the x-axis to either line forming the rectangle is b.](https://s3-us-west-2.amazonaws.com/courses-images/wp-content/uploads/sites/4175/2019/04/09225354/CNX_Calc_Figure_11_05_012.jpg)

Figure 12. A typical hyperbola in which the difference of the distances from any point on the ellipse to the foci is constant. The transverse axis is also called the major axis, and the conjugate axis is also called the minor axis.

The derivation of the equation of a hyperbola in standard form is virtually identical to that of an ellipse. One slight hitch lies in the definition: The difference between two numbers is always positive. Let *P* be a point on the hyperbola with coordinates $\left(x , y\right)$. Then the definition of the hyperbola gives $\left|d \left(P , F_{1}\right) - d \left(P , F_{2}\right)\right| = \text{constant}$. To simplify the derivation, assume that *P* is on the right branch of the hyperbola, so the absolute value bars drop. If it is on the left branch, then the subtraction is reversed. The vertex of the right branch has coordinates $\left(a , 0\right)$, so

$d \left(P , F_{1}\right) - d \left(P , F_{2}\right) = \left(c + a\right) - \left(c - a\right) = 2 a$.

This equation is therefore true for any point on the hyperbola. Returning to the coordinates $\left(x , y\right)$ for *P*:

 $\begin{aligned}d \left(P , F_{1}\right) - d \left(P , F_{2}\right) & = & 2 a \\ \sqrt{\left(x + c\right)^{2} + y^{2}} - \sqrt{\left(x - c\right)^{2} + y^{2}} & = & 2 a .\end{aligned}$

Add the second radical from both sides and square both sides:

 $\begin{aligned}\sqrt{\left(x - c\right)^{2} + y^{2}} & = & 2 a + \sqrt{\left(x + c\right)^{2} + y^{2}} \\ \left(x - c\right)^{2} + y^{2} & = & 4 a^{2} + 4 a \sqrt{\left(x + c\right)^{2} + y^{2}} + \left(x + c\right)^{2} + y^{2} \\ x^{2} - 2 c x + c^{2} + y^{2} & = & 4 a^{2} + 4 a \sqrt{\left(x + c\right)^{2} + y^{2}} + x^{2} + 2 c x + c^{2} + y^{2} \\ - 2 c x & = & 4 a^{2} + 4 a \sqrt{\left(x + c\right)^{2} + y^{2}} + 2 c x .\end{aligned}$

Now isolate the radical on the right-hand side and square again:

 $\begin{aligned}- 2 c x & = & 4 a^{2} + 4 a \sqrt{\left(x + c\right)^{2} + y^{2}} + 2 c x \\ 4 a \sqrt{\left(x + c\right)^{2} + y^{2}} & = & - 4 a^{2} - 4 c x \\ \sqrt{\left(x + c\right)^{2} + y^{2}} & = & - a - \frac{c x}{a} \\ \left(x + c\right)^{2} + y^{2} & = & a^{2} + 2 c x + \frac{c^{2} x^{2}}{a^{2}} \\ x^{2} + 2 c x + c^{2} + y^{2} & = & a^{2} + 2 c x + \frac{c^{2} x^{2}}{a^{2}} \\ x^{2} + c^{2} + y^{2} & = & a^{2} + \frac{c^{2} x^{2}}{a^{2}} .\end{aligned}$

Isolate the variables on the left-hand side of the equation and the constants on the right-hand side:

 $\begin{aligned}x^{2} - \frac{c^{2} x^{2}}{a^{2}} + y^{2} & = & a^{2} - c^{2} \\ \frac{\left(a^{2} - c^{2}\right) x^{2}}{a^{2}} + y^{2} & = & a^{2} - c^{2} .\end{aligned}$

Finally, divide both sides by $a^{2} - c^{2}$. This gives the equation

$\frac{x^{2}}{a^{2}} + \frac{y^{2}}{a^{2} - c^{2}} = 1$.

We now define *b* so that $b^{2} = c^{2} - a^{2}$. This is possible because $c > a$. Therefore the equation of the ellipse becomes

$\frac{x^{2}}{a^{2}} - \frac{y^{2}}{b^{2}} = 1$.

Finally, if the center of the hyperbola is moved from the origin to the point $\left(h , k\right)$, we have the following standard form of a hyperbola.

### theorem: Equation of a Hyperbola in Standard Form

---

Consider the hyperbola with center $\left(h , k\right)$, a horizontal major axis, and a vertical minor axis. Then the equation of this ellipse is

 $\frac{\left(x - h\right)^{2}}{a^{2}} - \frac{\left(y - k\right)^{2}}{b^{2}} = 1$

and the foci are located at $\left(h \pm c , k\right)$, where $c^{2} = a^{2} + b^{2}$. The equations of the asymptotes are given by $y = k \pm \frac{b}{a} \left(x - h\right)$. The equations of the directrices are

$x = k \pm \frac{a^{2}}{\sqrt{a^{2} + b^{2}}} = h \pm \frac{a^{2}}{c}$.

If the major axis is vertical, then the equation of the hyperbola becomes

 $\frac{\left(y - k\right)^{2}}{a^{2}} - \frac{\left(x - h\right)^{2}}{b^{2}} = 1$

and the foci are located at $\left(h , k \pm c\right)$, where $c^{2} = a^{2} + b^{2}$. The equations of the asymptotes are given by $y = k \pm \frac{a}{b} \left(x - h\right)$. The equations of the directrices are

$y = k \pm \frac{a^{2}}{\sqrt{a^{2} + b^{2}}} = k \pm \frac{a^{2}}{c}$.

If the major axis (transverse axis) is horizontal, then the hyperbola is called horizontal, and if the major axis is vertical then the hyperbola is called vertical. The equation of a hyperbola is in general form if it is in the form $A x^{2} + B y^{2} + C x + D y + E = 0$, where $A$ and $B$ have opposite signs. In order to convert the equation from general to standard form, use the method of completing the square.

### Example: Finding the Standard Form of a Hyperbola

Put the equation $9 x^{2} - 16 y^{2} + 36 x + 32 y - 124 = 0$ into standard form and graph the resulting hyperbola. What are the equations of the asymptotes?

Show Solution

First add $124$ to both sides of the equation:

$9 x^{2} - 16 y^{2} + 36 x + 32 y = 124$.

Next group the *x* terms together and the *y* terms together, then factor out the common factors:

 $\begin{aligned}\left(9 x^{2} + 36 x\right) - \left(16 y^{2} - 32 y\right) & = & 124 \\ 9 \left(x^{2} + 4 x\right) - 16 \left(y^{2} - 2 y\right) & = & 124.\end{aligned}$

We need to determine the constant that, when added inside each set of parentheses, results in a perfect square. In the first set of parentheses, take half the coefficient of $x$ and square it. This gives $\left(\frac{4}{2}\right)^{2} = 4$. In the second set of parentheses, take half the coefficient of *y* and square it. This gives $\left(\frac{- 2}{2}\right)^{2} = 1$. Add these inside each pair of parentheses. Since the first set of parentheses has a 9 in front, we are actually adding 36 to the left-hand side. Similarly, we are subtracting 16 from the second set of parentheses. Therefore the equation becomes

 $\begin{matrix}9 \left(x^{2} + 4 x + 4\right) - 16 \left(y^{2} - 2 y + 1\right) = 124 + 36 - 16 \\ 9 \left(x^{2} + 4 x + 4\right) - 16 \left(y^{2} - 2 y + 1\right) = 144.\end{matrix}$

Next factor both sets of parentheses and divide by 144:

 $\begin{aligned}9 \left(x + 2\right)^{2} - 16 \left(y - 1\right)^{2} & = & 144 \\ \frac{9 \left(x + 2\right)^{2}}{144} - \frac{16 \left(y - 1\right)^{2}}{144} & = & 1 \\ \frac{\left(x + 2\right)^{2}}{16} - \frac{\left(y - 1\right)^{2}}{9} & = & 1.\end{aligned}$

The equation is now in standard form. Comparing this to the theorem gives $h = - 2$, $k = 1$, $a = 4$, and $b = 3$. This is a horizontal hyperbola with center at $\left(- 2 , 1\right)$ and asymptotes given by the equations $y = 1 \pm \frac{3}{4} \left(x + 2\right)$. The graph of this hyperbola appears in the following figure.

![A hyperbola is drawn with equation 9x2 + 16y2 + 36x + 32y – 124 = 0. It has center at (−2, 1), and the hyperbolas are open to the left and right.](https://s3-us-west-2.amazonaws.com/courses-images/wp-content/uploads/sites/4175/2019/04/09225356/CNX_Calc_Figure_11_05_013.jpg)

Figure 13. Graph of the hyperbola in \[link\].

Watch the following video to see the worked solution to Example: Finding the Standard Form of a Hyperbola.

![](https://www.youtube.com/watch?v=AF_0mpKk4-Y)

For closed captioning, open the video on its original page by clicking the Youtube logo in the lower right-hand corner of the video display. In YouTube, the video will begin at the same starting point as this clip, but will continue playing until the very end.

You can view the [transcript for this segmented clip of “7.5 Conic Sections” here (opens in new window)](https://oerfiles.s3.us-west-2.amazonaws.com/Calculus+II/Transcripts/7.5ConicSections1076to1381_transcript.html).

Hyperbolas also have interesting reflective properties. A ray directed toward one focus of a hyperbola is reflected by a hyperbolic mirror toward the other focus. This concept is illustrated in the following figure.

![A hyperbola is drawn that is open to the right and left. There is a ray pointing to a point on the right hyperbola marked](https://s3-us-west-2.amazonaws.com/courses-images/wp-content/uploads/sites/4175/2019/04/09225402/CNX_Calc_Figure_11_05_015.jpg)

Figure 15. A hyperbolic mirror used to collect light from distant stars.

This property of the hyperbola has important applications. It is used in radio direction finding (since the difference in signals from two towers is constant along hyperbolas), and in the construction of mirrors inside telescopes (to reflect light coming from the parabolic mirror to the eyepiece). Another interesting fact about hyperbolas is that for a comet entering the solar system, if the speed is great enough to escape the Sun’s gravitational pull, then the path that the comet takes as it passes through the solar system is hyperbolic.

### Candela Citations

- 7.5 Conic Sections. **Authored by**: Ryan Melton. **License**: *[CC BY: Attribution](https://creativecommons.org/licenses/by/4.0/)*
- Calculus Volume 2. **Authored by**: Gilbert Strang, Edwin (Jed) Herman. **Provided by**: OpenStax. **Located at**: [https://openstax.org/books/calculus-volume-2/pages/1-introduction](https://openstax.org/books/calculus-volume-2/pages/1-introduction). **License**: *[CC BY-NC-SA: Attribution-NonCommercial-ShareAlike](https://creativecommons.org/licenses/by-nc-sa/4.0/)*. **License Terms**: Access for free at https://openstax.org/books/calculus-volume-2/pages/1-introduction