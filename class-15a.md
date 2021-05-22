# Learn to Code Advanced HTML & CSS

## Transforms

#### The **transform** property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.


## Transform Syntax

#### The actual syntax for the **transform** property is quite simple, including the transform property followed by the value. The value specifies the transform type followed by a specific amount inside parentheses.

## 2D Transforms

        #two-dimensional-transforms

#### Elements may be distorted, or transformed, on both a two-dimensional plane or a three-dimensional plane. Two-dimensional transforms work on the x and y axes, known as horizontal and vertical axes. Three-dimensional transforms work on both the x and y axes, as well as the z axis. These three-dimensional transforms help define not only the length and width of an element, but also the depth. We’ll start by discussing how to transform elements on a two-dimensional plane, and then work our way into three-dimensional transforms.

## 2D Rotate

#### The **transform** property accepts a handful of different values. The rotate value provides the ability to rotate an element from 0 to 360 degrees. Using a positive value will rotate an element clockwise, and using a negative value will rotate the element counterclockwise. The default point of rotation is the center of the element, 50% 50%, both horizontally and vertically. Later we will discuss how you can change this default point of rotation

> HTML

            <figure class="box-1">Box 1</figure>
            <figure class="box-2">Box 2</figure>

              
> CSS

            .box-1 {
            transform: rotate(20deg);
            }
            .box-2 {
            transform: rotate(-55deg);
            }

You can see result from her: [RESULT](https://codepen.io/shayhowe/embed/AKDIp?default-tab=result&slug-hash=AKDIp&theme-id=5990&user=shayhowe&name=cp_embed_1#result-box)

##### The gray box behind the rotated element symbolizes the original position of the element. Additionally, upon hover the box will rotate 360 degrees horizontally. As the lesson progresses, keep an eye out for the gray box within each demonstration as a reference to the element’s original position and the horizontal rotation to help demonstrate an elements alteration and depth.

## 2D Scale
#### Using the scale value within the transform property allows you to change the appeared size of an element. The default scale value is 1, therefore any value between .99 and .01 makes an element appear smaller while any value greater than or equal to 1.01 makes an element appear larger.

> HTML

            <figure class="box-1">Box 1</figure>
            <figure class="box-2">Box 2</figure>

              
> CSS

            .box-1 {
            transform: scale(.75);
            }
            .box-2 {
            transform: scale(1.25);
            }

You can see result from her: [RESULT](https://codepen.io/shayhowe/embed/khtnm?default-tab=result&slug-hash=khtnm&theme-id=5990&user=shayhowe&name=cp_embed_2#result-box)


## 2D Translate
#### The translate value works a bit like that of relative positioning, pushing and pulling an element in different directions without interrupting the normal flow of the document. Using the translateX value will change the position of an element on the horizontal axis while using the translateY value will change the position of an element on the vertical axis.

#### As with the scale value, to set both the x and y axis values at once, use the translate value and declare the x axis value first, followed by a comma, and then the y axis value.

#### The distance values used within the translate value may be any general length measurement, most commonly pixels or percentages. Positive values will push an element down and to the right of its default position while negative values will pull an element up and to the left of its default position.

> HTML

        <figure class="box-1">Box 1</figure>
        <figure class="box-2">Box 2</figure>
        <figure class="box-3">Box 3</figure>

              
> CSS

        .box-1 {
        transform: translateX(-10px);
        }
        .box-2 {
        transform: translateY(25%);
        }
        .box-3 {
        transform: translate(-10px, 25%);
        }


You can see result from her: [RESULT](https://codepen.io/shayhowe/embed/LqHwt?default-tab=result&slug-hash=LqHwt&theme-id=5990&user=shayhowe&name=cp_embed_4#result-box)

## 2D Skew
#### The last transform value in the group, skew, is used to distort elements on the horizontal axis, vertical axis, or both. The syntax is very similar to that of the scale and translate values. Using the skewX value distorts an element on the horizontal axis while the skewY value distorts an element on the vertical axis. To distort an element on both axes the skew value is used, declaring the x axis value first, followed by a comma, and then the y axis value.%p

> HTML

        <figure class="box-1">Box 1</figure>
        <figure class="box-2">Box 2</figure>
        <figure class="box-3">Box 3</figure>

              
> CSS

        .box-1 {
        transform: skewX(5deg);
        }
        .box-2 {
        transform: skewY(-20deg);
        }
        .box-3 {
        transform: skew(5deg, -20deg);
        }

You can see result from her: [RESULT](https://codepen.io/shayhowe/embed/GHwCK?default-tab=result&slug-hash=GHwCK&theme-id=5990&user=shayhowe&name=cp_embed_5#result-box)

## Transform Origin
#### As previously mentioned, the default transform origin is the dead center of an element, both 50% horizontally and 50% vertically. To change this default origin position the transform-origin property may be used.
#### The transform-origin property can accept one or two values. When only one value is specified, that value is used for both the horizontal and vertical axes. If two values are specified, the first is used for the horizontal axis and the second is used for the vertical axis.

#### Individually the values are treated like that of a background image position, using either a length or keyword value. That said, 0 0 is the same value as top left, and 100% 100% is the same value as bottom right. More specific values can also be set, for example 20px 50px would set the origin to 20 pixels across and 50 pixels down the element.

> HTML

        <figure class="box-1">Box 1</figure>
        <figure class="box-2">Box 2</figure>
        <figure class="box-3">Box 3</figure>
        <figure class="box-4">Box 3</figure>

              
> CSS

        .box-1 {
        transform: rotate(15deg);
        transform-origin: 0 0;
        }
        .box-2 {
        transform: scale(.5);
        transform-origin: 100% 100%;
        }
        .box-3 {
        transform: skewX(20deg);
        transform-origin: top left;
        }
        .box-4 {
        transform: scale(.75) translate(-10px, -10px);
        transform-origin: 20px 50px;
        }

You can see result from her: [RESULT](https://codepen.io/shayhowe/embed/uavIn?default-tab=result&slug-hash=uavIn&theme-id=5990&user=shayhowe&name=cp_embed_8#result-box)


## 3D Transforms

#### Working with two-dimensional transforms we are able to alter elements on the horizontal and vertical axes, however there is another axis along which we can transform elements. Using three-dimensional transforms we can change elements on the z axis, giving us control of depth as well as length and width.

## 3D Rotate
#### So far we’ve discussed how to rotate an object either clockwise or counterclockwise on a flat plane. With three-dimensional transforms we can rotate an element around any axes. To do so, we use three new transform values, including rotateX, rotateY, and rotateZ.

> HTML

            <figure class="box-1">Box 1</figure>
            <figure class="box-2">Box 2</figure>
            <figure class="box-3">Box 3</figure>

              
> CSS

            .box-1 {
            transform: perspective(200px) rotateX(45deg);
            }
            .box-2 {
            transform: perspective(200px) rotateY(45deg);
            }
            .box-3 {
            transform: perspective(200px) rotateZ(45deg);
            }


You can see result from her: [RESULT](https://codepen.io/shayhowe/embed/bmayf?default-tab=result&slug-hash=bmayf&theme-id=5990&user=shayhowe&name=cp_embed_13#result-box)


## 3D Scale
#### By using the scaleZ three-dimensional transform elements may be scaled on the z axis. This isn’t extremely exciting when no other three-dimensional transforms are in place, as there is nothing in particular to scale. In the demonstration below the elements are being scaled up and down on the z axis, however the rotateX value is added in order to see the behavior of the scaleZ value. When removing the rotateX in this case, the elements will appear to be unchanged.

> HTML

        <figure class="box-1">Box 1</figure>
        <figure class="box-2">Box 2</figure>

              
> CSS

        .box-1 {
        transform: perspective(200px) scaleZ(1.75) rotateX(45deg);
        }
        .box-2 {
        transform: perspective(200px) scaleZ(.25) rotateX(45deg);
        }

You can see result from her: [RESULT](https://codepen.io/shayhowe/embed/DIlFd?default-tab=result&slug-hash=DIlFd&theme-id=5990&user=shayhowe&name=cp_embed_14#result-box)

# Transform Style

#### On occasion three-dimensional transforms will be applied on an element that is nested within a parent element which is also being transformed. In this event, the nested, transformed elements will not appear in their own three-dimensional space. To allow nested elements to transform in their own three-dimensional plane use the transform-style property with the preserve-3d value.

#### The transform-style property needs to be placed on the parent element, above any nested transforms. The preserve-3d value allows the transformed children elements to appear in their own three-dimensional plane while the flat value forces the transformed children elements to lie flat on the two-dimensional plane.

> HTML

            <div class="rotate three-d">
            <figure class="box">Box 1</figure>
            </div>
            <div class="rotate">
            <figure class="box">Box 2</figure>
            </div>

              
> CSS

            .rotate {
            transform: perspective(200px) rotateY(45deg);
            }
            .three-d {
            transform-style: preserve-3d;
            }
            .box {
            transform: rotateX(15deg) translateZ(20px);
            transform-origin: 0 0;
            }
You can see result from her: [RESULT](https://codepen.io/shayhowe/embed/jBhbk?default-tab=result&slug-hash=jBhbk&theme-id=5990&user=shayhowe&name=cp_embed_16#result-box)



# Transitions & Animations
#### With CSS3 transitions you have the potential to alter the appearance and behavior of an element whenever a state change occurs, such as when it is hovered over, focused on, active, or targeted.

## Transitions

#### an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the `:hover`, `:focus`, `:active`, and `:target` pseudo-classes.

#### There are four transition related properties in total, including 
1. transition-property, 
2. transition-duration, 
3. transition-timing-function, 
4. transition-delay.

                .box {
                background: #2db34a;
                transition-property: background;
                transition-duration: 1s;
                transition-timing-function: linear;
                }
                .box:hover {
                background: #ff7b29;
                }


You can see result from her: [RESULT](https://codepen.io/shayhowe/embed/aCwcK?default-tab=result&slug-hash=aCwcK&theme-id=5990&user=shayhowe&name=cp_embed_1#result-box)


## Transitional Property
#### The transition-property property determines exactly what properties will be altered in conjunction with the other transitional properties. By default, all of the properties within an element’s different states will be altered upon change. However, only the properties identified within the transition-property value will be affected by any transitions.

                .box {
                background: #2db34a;
                border-radius: 6px
                transition-property: background, border-radius;
                transition-duration: 1s;
                transition-timing-function: linear;
                }
                .box:hover {
                background: #ff7b29;
                border-radius: 50%;
                }



You can see result from her: [RESULT](https://codepen.io/shayhowe/embed/HlgxF?default-tab=result&slug-hash=HlgxF&theme-id=5990&user=shayhowe&name=cp_embed_2#result-box)


## Transitional Properties
#### It is important to note, not all properties may be transitioned, only properties that have an identifiable halfway point. Colors, font sizes, and the alike may be transitioned from one value to another as they have recognizable values in-between one another. The display property, for example, may not be transitioned as it does not have any midpoint. A handful of the more popular transitional properties include the following.

* background-color
* background-position
* border-color
* border-width
* border-spacing
* bottom
* clip
* color
* crop
* font-size
* font-weight
* heightleft
* letter-spacing
* line-height
* margin
* max-height
* max-width
* min-height
* min-width
* opacityoutline-color
* outline-offset
* outline-width
* paddingright
* text-indent
* text-shadow
* top
* vertical-align
* visibility
* width
* word-spacing
* z-index

## Transition Duration
#### The duration in which a transition takes place is set using the transition-duration property. The value of this property can be set using general timing values, including seconds (s) and milliseconds (ms). These timing values may also come in fractional measurements, .2s for example.

                .box {
                background: #2db34a;
                border-radius: 6px;
                transition-property: background, border-radius;
                transition-duration: .2s, 1s;
                transition-timing-function: linear;
                }
                .box:hover {
                background: #ff7b29;
                border-radius: 50%;
                }

You can see result from her: [RESULT](https://codepen.io/shayhowe/embed/BGmdv?default-tab=result&slug-hash=BGmdv&theme-id=5990&user=shayhowe&name=cp_embed_3#result-box)

## Transition Timing
#### The transition-timing-function property is used to set the speed in which a transition will move. Knowing the duration from the transition-duration property a transition can have multiple speeds within a single duration. A few of the more popular keyword values for the transition-timing-function property include linear, ease-in, ease-out, and ease-in-out.


                .box {
                background: #2db34a;
                border-radius: 6px;
                transition-property: background, border-radius;
                transition-duration: .2s, 1s;
                transition-timing-function: linear, ease-in;
                }
                .box:hover {
                background: #ff7b29;
                border-radius: 50%;
                }


You can see result from her: [RESULT](https://codepen.io/shayhowe/embed/qzGpr?default-tab=result&slug-hash=qzGpr&theme-id=5990&user=shayhowe&name=cp_embed_4#result-box)



## Transition Delay
#### On top of declaring the transition property, duration, and timing function, you can also set a delay with the transition-delay property. The delay sets a time value, seconds or milliseconds, that determines how long a transition should be stalled before executing. As with all other transition properties, to delay numerous transitions, each delay can be declared as comma separated values.

                .box {
                background: #2db34a;
                border-radius: 6px
                transition-property: background, border-radius;
                transition-duration: .2s, 1s;
                transition-timing-function: linear, ease-in;
                transition-delay: 0s, 1s;
                }
                .box:hover {
                background: #ff7b29;
                border-radius: 50%;
                }

You can see result from her: [RESULT](https://codepen.io/shayhowe/embed/naDEp?default-tab=result&slug-hash=naDEp&theme-id=5990&user=shayhowe&name=cp_embed_5#result-box)

## Shorthand Transitions
#### Declaring every transition property individually can become quite intensive, especially with vendor prefixes. Fortunately there is a shorthand property, transition, capable of supporting all of these different properties and values. Using the transition value alone, you can set every transition value in the order of transition-property, transition-duration, transition-timing-function, and lastly transition-delay. Do not use commas with these values unless you are identifying numerous transitions.


                .box {
                background: #2db34a;
                border-radius: 6px;
                transition: background .2s linear, border-radius 1s ease-in 1s;
                }
                .box:hover {
                color: #ff7b29;
                border-radius: 50%;
                }


You can see result from her: [RESULT](https://codepen.io/shayhowe/embed/bFDyh?default-tab=result&slug-hash=bFDyh&theme-id=5990&user=shayhowe&name=cp_embed_6#result-box)


## Animations
#### Transitions do a great job of building out visual interactions from one state to another, and are perfect for these kinds of single state changes. However, when more control is required, transitions need to have multiple states. In return, this is where animations pick up where transitions leave off.

## Animations Keyframes
#### To set multiple points at which an element should undergo a transition, use the @keyframes rule. The @keyframes rule includes the animation name, any animation breakpoints, and the properties intended to be animated.


                @keyframes slide {
                0% {
                left: 0;
                top: 0;
                }
                50% {
                left: 244px;
                top: 100px;
                }
                100% {
                left: 488px;
                top: 0;
                }
                }
You can see result from her: [RESULT](https://codepen.io/shayhowe/embed/hIpFr?default-tab=result&slug-hash=hIpFr&theme-id=5990&user=shayhowe&name=cp_embed_9#result-box)


## Animation Name
#### Once the keyframes for an animation have been declared they need to be assigned to an element. To do so, the animation-name property is used with the animation name, identified from the @keyframes rule, as the property value. The animation-name declaration is applied to the element in which the animation is to be applied to.

                .stage:hover .ball {
                animation-name: slide;
                }

You can see result from her: [RESULT](https://codepen.io/shayhowe/embed/fochl?default-tab=result&slug-hash=fochl&theme-id=5990&user=shayhowe&name=cp_embed_10#result-box)

## Animation Iteration
#### By default, animations run their cycle once from beginning to end and then stop. To have an animation repeat itself numerous times the animation-iteration-count property may be used. Values for the animation-iteration-count property include either an integer or the infinite keyword. Using an integer will repeat the animation as many times as specified, while the infinite keyword will repeat the animation indefinitely in a never ending fashion.

                .stage:hover .ball {
                animation-name: slide;
                animation-duration: 2s;
                animation-timing-function: ease-in-out;
                animation-delay: .5s;
                animation-iteration-count: infinite;
                }

You can see result from her: [RESULT](https://codepen.io/shayhowe/embed/xvbqF?default-tab=result&slug-hash=xvbqF&theme-id=5990&user=shayhowe&name=cp_embed_11#result-box)


## Animation Play State
#### The animation-play-state property allows an animation to be played or paused using the running and paused keyword values respectively. When you play a paused animation, it will resume running from its current state rather than starting from the very beginning again.

                .stage:hover .ball {
                animation-name: slide;
                animation-duration: 2s;
                animation-timing-function: ease-in-out;
                animation-delay: .5s;
                animation-iteration-count: infinite;
                animation-direction: alternate;
                }
                .stage:active .ball {
                animation-play-state: paused;
                }

You can see result from her: [RESULT](https://codepen.io/shayhowe/embed/ogJjm?default-tab=result&slug-hash=ogJjm&theme-id=5990&user=shayhowe&name=cp_embed_13#result-box)


## Shorthand Animations
#### Fortunately animations, just like transitions, can be written out in a shorthand format. This is accomplished with one animation property, rather than multiple declarations. The order of values within the animation property should be animation-name, animation-duration, animation-timing-function, animation-delay, animation-iteration-count, animation-direction, animation-fill-mode, and lastly animation-play-state.

                .stage:hover .ball {
                animation: slide 2s ease-in-out .5s infinite alternate;
                }
                .stage:active .ball {
                animation-play-state: paused;
                }

You can see result from her: [RESULT](https://codepen.io/shayhowe/embed/gDmka?default-tab=result&slug-hash=gDmka&theme-id=5990&user=shayhowe&name=cp_embed_15#result-box)

---
---


### CSS3 has introduced countless possibilities for UX designers, and the best thing about them is that the coolest parts are really simple to implement.

### Just a couple of lines of code will give you an awesome transition effect that will excite your users, increase engagement and ultimately, when used well, increase your conversions. What’s more, these effects are hardware accelerated, and a progressive enhancement that you can use right now.

### Here are 8 really simple effects that will add life to your UI and smiles to your users’ faces.

### 1. Fade in
##### Having things fade in is a fairly common request from clients. It’s a great way to emphasize functionality or draw attention to a call to action.

##### Fade in effects are coded in two steps: first, you set the initial state; next, you set the change, for example on hover:

                .fade
                {
                        opacity:0.5;
                }
                .fade:hover
                {
                        opacity:1;
                }

### 2. Change color
##### Animating a change of color used to be unbelievably complex, with all kinds of math involved in calculating separate RGB values and then recombining them. Now, we just set the div’s class to “color” and specify the color we want in our CSS:

                .color:hover
                {
                        background:#53a7ea;
                }

### 3. Grow & Shrink
##### To grow an element, you used to have to use its width and height, or its padding. But now we can use CSS3’s transform to enlarge.

##### Set your div’s class to “grow” and then add this code to your style block:

                .grow:hover
                {
                        -webkit-transform: scale(1.3);
                        -ms-transform: scale(1.3);
                        transform: scale(1.3);
                }

##### Shrinking an element is as simple as growing it. To enlarge an element we specify a value greater than 1, to shrink it, we specify a value less than 1:

                .shrink:hover
                {
                        -webkit-transform: scale(0.8);
                        -ms-transform: scale(0.8);
                        transform: scale(0.8);
                }


### 4. Rotate elements
##### CSS transforms have a number of different uses, and one of the best is transforming the rotation of an element. Give your div the class “rotate” and add the following to your CSS:

                .rotate:hover
                {
                        -webkit-transform: rotateZ(-30deg);
                        -ms-transform: rotateZ(-30deg);
                        transform: rotateZ(-30deg);
                }

### 5. Square to circle
##### A really popular effect at the moment is transitioning a square element into a round one, and vice versa. With CSS, it’s a simple effect to achieve, we just transition the border-radius property.

##### Give your div the class “circle” and add this CSS to your styles:

                .circle:hover
                {
                        border-radius:50%;
                }


### 6. 3D shadow
##### 3D shadows were frowned upon for a year or so, because they weren’t seen as compatible with flat design, which is of course nonsense, they work fantastically well to give a user feedback on their interactions and work with flat, or fake 3D interfaces.

##### This effect is achieved by adding a box shadow, and then moving the element on the x axis using the transform and translate properties so that it appears to grow out of the screen.

##### Give your div the class “threed” and then add the following code to your CSS:

                .threed:hover
                {
                        box-shadow:
                                1px 1px #53a7ea,
                                2px 2px #53a7ea,
                                3px 3px #53a7ea;
                        -webkit-transform: translateX(-3px);
                        transform: translateX(-3px);
                }

### 7. Swing
##### Not all elements use the transition property. We can also create highly complex animations using @keyframes, animation and animation-iteration.

##### In this case, we’ll first define a CSS animation in your styles. You’ll notice that due to implementation issues, we need to use @-webkit-keyframes as well as @keyframes (yes, Internet Explorer really is better than Chrome, in this respect at least).

                @-webkit-keyframes swing
                {
                15%
                {
                        -webkit-transform: translateX(5px);
                        transform: translateX(5px);
                }
                30%
                {
                        -webkit-transform: translateX(-5px);
                transform: translateX(-5px);
                } 
                50%
                {
                        -webkit-transform: translateX(3px);
                        transform: translateX(3px);
                }
                65%
                {
                        -webkit-transform: translateX(-3px);
                        transform: translateX(-3px);
                }
                80%
                {
                        -webkit-transform: translateX(2px);
                        transform: translateX(2px);
                }
                100%
                {
                        -webkit-transform: translateX(0);
                        transform: translateX(0);
                }
                }
                @keyframes swing
                {
                15%
                {
                        -webkit-transform: translateX(5px);
                        transform: translateX(5px);
                }
                30%
                {
                        -webkit-transform: translateX(-5px);
                        transform: translateX(-5px);
                }
                50%
                {
                        -webkit-transform: translateX(3px);
                        transform: translateX(3px);
                }
                65%
                {
                        -webkit-transform: translateX(-3px);
                        transform: translateX(-3px);
                }
                80%
                {
                        -webkit-transform: translateX(2px);
                        transform: translateX(2px);
                }
                100%
                {
                        -webkit-transform: translateX(0);
                        transform: translateX(0);
                }
                }

##### This animation simply moves the element left and right, now all we need to do is apply it:

                .swing:hover
                {
                        -webkit-animation: swing 1s ease;
                        animation: swing 1s ease;
                        -webkit-animation-iteration-count: 1;
                        animation-iteration-count: 1;
                }

### 8. Inset border
##### One of the hottest button styles right now is the ghost button; a button with no background and a heavy border. We can of course add a border to an element simply, but that will change the element’s position. We could fix that problem using box sizing, but a far simpler solution is the transition in a border using an inset box shadow.

##### Give your div the class “border” and add the following CSS to your styles:

                .border:hover
                {
                        box-shadow: inset 0 0 0 25px #53a7ea;
                }


You can see the all result from her: [RESULT](https://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users)


---
---


# 6 Buttons animated
#### Buttons are not only good for usability, but also an extremely important design element for your website. For this reason, here is a collection of the best CSS buttons!

#### Whether thick and bold on your homepage or small and discreet in the footer, buttons are a very important design element for the user flow on your website. For a company website, a more discreet design is often used, whereas creative industries use more eye-catching and “weird” CSS buttons. So that all industries are equally served, you will find many different styles and combinations here.

#### I and many other web developers/designers – also set a high value on animations for Hover or Focus, which is why all of the following buttons bring along nice animations. But now we start directly!

You can see the 6 button from her: [RESULT](https://codepen.io/retyui/pen/ByoaXV?editors=1111)


---
---
# CSS3 Keyframes Animation
#### Each keyframe describes how the animated element should render at a given time during the animation sequence. Since the timing of the animation is defined in the CSS style that configures the animation, keyframes use a <percentage> to indicate the time during the animation sequence at which they take place.

You can see the CSS3 Keyframes Animation from her: [RESULT](https://codepen.io/akshaychauhan/pen/oAfae)


---
---
# 404
#### The HTTP 404, 404 Not Found, 404, 404 Error, Page Not Found or File Not Found error message is a Hypertext Transfer Protocol (HTTP) standard response code, in computer network communications, to indicate that the browser was able to communicate with a given server, but the server could not find what was requested.
You can see the **404** from her: [RESULT](https://codepen.io/kieranfivestars/pen/MYdQxX)


---
---
# Pure CSS Bounce Animation
#### Bouncing images at different times: Add element with class bounce, bounce2 and bounce3. The CSS in my snippet has an animation delay for the bounce effect.

You can see the **Pure CSS Bounce Animation** from her: [RESULT](https://codepen.io/dp_lewis/pen/gCfBv)







