1. transform is the css property that we can give it the value with some 
    predefined functions: 

    
    img {
        // move the element in x direction with 200px;
        transform: translateX(200px);
        // 200px in x direction, 100px in y direction
        transform: translate(200px, 100px)
        // scale the element 1 do nothing anything above it make it bigger
        // and anything less than 1 make it smaller
        transform: scaleX(1);
        // rotate the element along the x axis
        transform: rotateX(30deg)
        // we can chaing all these 
        transform: rotateZ(-90deg) translateY(200px)
    }

[ATTENTION]
2. when we rotate the element, the axis of the object will be rotate too:
    for example this move the y axis in the place of the x axis for the selected 
    object: 
                 transform: rotateZ(-90deg) translateY(200px)

3. Transition is just transite the element from certain STATE to another STATE:

    .circle {
        width: 100px;
        padding: 50px 0;
        line-height: 0;
        margin: 68px auto;
        background: pink;
        color: white;
        border-radius: 50px;
        cursor: pointer;
        //transition: 2s; // just apply to everything change in the .circle
        // the second number is the delay
        // the fourth parameter is type of change
        transition: background 2s, transform 0.3s 1s linear;
    }
    .circle:hover{
        background: salmon;
        transform: rotate(360deg)
    }    

4. Keyframes are just block of codes that control the css animations, in 
    keyframes we go from certain state to another state: 

        @keyframes drive {
            from{
                transfrom: translateX(0);
            }
            to {
                transform: translateX(500px);
            }
        }

    and in the element itself we use this keyframe: 

        .marion {
            animation-name: drive;
            animation-durataion: 3s;
        }

5. We can define the css state after the animation has been done: 

        .mario {
            animation-name: drive;
            animation-duration: 3s;
            animation-fill-mode: forward;   /none: back to the primary state
                                            /forward: the last state
        }

        if we use animation delay, animation will be starts with delay, 
        and if we start the animation not from the 0px, we will have the jump
        to the 200px at first, by using backward this jump will be ok but 
        at the end, the animation will go back, so we can use both to have 
        the forward feature and backward feature at the same time

6. we can repeat the animation with animation-iteration-count: 

        .mario {
            position: absolute;
            top: -40px;
            left: 0px;
            animation-name: drive;
            animation-duration: 3s;
            animation-fill-mode: both;
            animation-iteration-count: 3; // we can use infinite to loop 
                                            // through this
        }

7. we can have animation direction to change the from and to in the 
    keyframe: 
    
    animation-direction: normal; //reverse //alternate//alternate-reverse

8.  we can use animation timing function to control the speed of the animation

    animation-timing-function: ease; start slow, fast in the middle and slow at the end
    linear: constant speed all the way
    ease-in: start slow and get faster
    ease-out: start fast but get slower
    cubic-bezier(,,,) it gets for number it is based on the cubic function

9. There is animation shorthand for this properties: 

      animation: wind 80s linear 0s infinite reverse both;
