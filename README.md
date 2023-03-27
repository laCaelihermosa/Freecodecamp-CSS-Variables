# You are ready to create your first variable. Variable declarations begin with two dashes (-) and are given a name and a value like this: --variable-name: value;
# To use a variable, put the variable name in parentheses with var in front of them like this: var(--variable-name). Whatever value you gave the variable will be applied to whatever property you use it on. This is the main advantage of using variables. You can see how it gets applied everywhere you used the variable.
# There is a value to use as a fallback to backup primary color:  You should add a fallback value to a variable by putting it as the second value of where you use the variable like this: var(--variable-name, fallback-value); ex: background-color: var(--building-color2, green);
# The :root selector. This is the highest level selector in CSS; putting your variables there will make them usable everywhere. Add the :root selector to the top of your stylesheet, and place all your variable declarations there.
# Ex :root  {--building-color1: #aa80ff, --building-color2: #66cc99, --building-color3: #cc6699;}
# With CSS variables you can change values without searching everywhere in the stylesheet.
# You should optimize your code. You can use a comma (,) to separate selectors like this: selector1, selector2. there, effectively applying those styles to both of the elements. ex: .background-buildings, .foreground-buildings { width: 100%; eight: 100%; position: absolute; top: 0; display: flex; align-items: flex-end; justify-content: space-evenly;}
# Gradients in CSS are a way to transition between colors across the distance of an element. They are applied to the background property and the syntax looks like this: gradient-type(color1, color2);
# Gradients can use as many colors as you want like this: gradient-type(color1, color2, color3);
# You can also specify where you want a gradient transition: gradient-type(color1, color2 20%, color3);
# Gradient transitions often gradually change from one color to another. You can make the change a solid line like this:

    linear-gradient(
        var(--first-color) 0%,
        var(--first-color) 40%,
        var(--second-color) 40%,
        var(--second-color) 80%
    );

    background: repeating-linear-gradient(90deg,
        var(--building-color4),
        var(--building-color4) 10%,
        transparent 10%,
        transparent 15%
  );

# So far, all the gradients you created have gone from top to bottom, that's the default direction. You can specify another direction by adding it before your colors like this:

gradient-type(
  direction,  (to right, to left, to bottom, tot op, also degs...45deg, 90deg. etc...)
  color1,
  color2
);

# You can add multiple gradients to an element by separating them with a comma (,) like this:

gradient1(
  colors
),
gradient2(
  colors
);

 background: repeating-linear-gradient(
      90deg,
      var(--building-color4),
      var(--building-color4) 10%,
      transparent 10%,
      transparent 15%
    ),
     repeating-linear-gradient(
      var(--building-color4),
      var(--building-color4) 10%,
      var(--window-color4) 10%,
      var(--window-color4) 90%
    );

# Adding these, you can see how a thick border on an element gives you some angles where two sides meet. You are going to use that bottom border as the top of the building.

    margin: auto;
    width: 5vw;
    height: 5vw;
    border-top: 1vw solid #000;
    border-bottom: 1vw solid #000;
    border-left: 1vw solid #999;
    border-right: 1vw solid #999;

# removing width and height, also changin border left and right to use 5vh instead 1vh. Next, change the two #999 of .bb2a to transparent. This will make the left and right borders invisible. Remove the margin and border-top properties and values from .bb2a to turn it into a triangle for the top of the building.