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
